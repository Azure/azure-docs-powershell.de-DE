---
title: Azure-Kontexte und -Anmeldeinformationen
description: Hier erfahren Sie, wie Sie Azure-Anmeldeinformationen und andere Informationen in mehreren PowerShell-Sitzungen wiederverwenden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: f14583e7c24d0355d778607bab52c81ae22598b8
ms.sourcegitcommit: eeb720e053939a68873ae3973bc81d5826358c9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2020
ms.locfileid: "80440893"
---
# <a name="azure-powershell-context-objects"></a>Azure PowerShell-Kontextobjekte

Azure PowerShell verwendet _Azure PowerShell-Kontextobjekte_ (Azure-Kontexte), um Abonnement- und Authentifizierungsinformationen zu speichern. Besitzer mehrerer Abonnements können mithilfe von Azure-Kontexten das Abonnement auswählen, für das Azure PowerShell-Cmdlets ausgeführt werden sollen. Azure-Kontexte werden auch verwendet, um Anmeldeinformationen über mehrere PowerShell-Sitzungen hinweg zu speichern und Hintergrundaufgaben auszuführen.

In diesem Artikel wird die Verwaltung von Azure-Kontexten behandelt, nicht die Verwaltung von Abonnements oder Konten. Informationen zur Verwaltung von Benutzern, Abonnements, Mandanten und anderen Kontoinformationen finden Sie in der [Dokumentation zu Azure Active Directory](/azure/active-directory). Informationen zur Verwendung von Kontexten für die Ausführung von Hintergrundaufgaben oder parallelen Aufgaben finden Sie unter [Ausführen von Azure PowerShell-Cmdlets in PowerShell-Aufträgen](using-psjobs.md). Machen Sie sich jedoch zuvor mit Azure-Kontexten vertraut.

## <a name="overview-of-azure-context-objects"></a>Übersicht über Azure-Kontextobjekte

Bei Azure-Kontexten handelt es sich um PowerShell-Objekte, die Ihr aktives Abonnement, für das Befehle ausgeführt werden sollen, sowie die Authentifizierungsinformationen darstellen, die zum Herstellen einer Verbindung mit einer Azure-Cloud erforderlich sind. Mit Azure-Kontexten muss Azure PowerShell Ihr Konto nicht bei jedem Abonnementwechsel erneut authentifizieren. Ein Azure-Kontext umfasst Folgendes:

* Das _Konto_, das für die Anmeldung bei Azure mit [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) verwendet wurde. In Azure-Kontexten werden Benutzer, Anwendungs-IDs und Dienstprinzipale aus Kontosicht gleich behandelt.
* Das aktive _Abonnement_ – ein Servicevertrag mit Microsoft für die Erstellung und Ausführung von Azure-Ressourcen, die einem _Mandanten_ zugeordnet sind. Mandanten werden in der Dokumentation oder im Zusammenhang mit Active Directory häufig als _Organisationen_ bezeichnet.
* Ein Verweis auf einen _Tokencache_ – ein gespeichertes Authentifizierungstoken für den Zugriff auf eine Azure-Cloud. Speicherort und Aufbewahrungsdauer dieses Tokens hängen von den [Einstellungen für die automatische Kontextspeicherung](#save-azure-contexts-across-powershell-sessions) ab.

Weitere Informationen zu diesen Begriffen finden Sie [hier](/azure/active-directory/fundamentals/active-directory-whatis#terminology). Von Azure-Kontexten verwendete Authentifizierungstoken unterscheiden sich nicht von anderen gespeicherten Token einer beständigen Sitzung. 

Wenn Sie sich mit `Connect-AzAccount` anmelden, wird mindestens ein Azure-Kontext für Ihr Standardabonnement erstellt. Bei dem von `Connect-AzAccount` zurückgegebenen Objekt handelt es sich um den Azure-Standardkontext, der für die restliche PowerShell-Sitzung verwendet wird.

## <a name="get-azure-contexts"></a>Abrufen von Azure-Kontexten

Verfügbare Azure-Kontexte werden mithilfe des Cmdlets [Get-AzContext](/powershell/module/az.accounts/get-azcontext) abgerufen. Verwenden Sie `-ListAvailable`, um alle verfügbaren Kontexte aufzulisten:

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

Oder rufen Sie einen Kontext anhand des Namens ab:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

Kontextnamen können sich vom Namen des zugeordneten Abonnements unterscheiden.

> [!IMPORTANT]
> Bei den verfügbaren Azure-Kontexten handelt es sich __nicht__ immer um Ihre verfügbaren Abonnements. Azure-Kontexte stellen nur lokal gespeicherte Informationen dar. Ihre Abonnements können Sie mithilfe des Cmdlets [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) abrufen.

## <a name="create-a-new-azure-context-from-subscription-information"></a>Erstellen eines neuen Azure-Kontexts auf der Grundlage von Abonnementinformationen

Mit dem Cmdlet [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) können Sie neue Azure-Kontexte erstellen und sie als aktiven Kontext festlegen.
Am einfachsten lässt sich ein neuer Azure-Kontext auf der Grundlage vorhandener Abonnementinformationen erstellen. Das Cmdlet akzeptiert das Ausgabeobjekt von `Get-AzSubscription` als weitergeleiteten Wert und konfiguriert einen neuen Azure-Kontext:

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

Bei Bedarf können alternativ auch der Name oder die ID des Abonnements und die Mandanten-ID angegeben werden:

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

Ohne Angabe des Arguments `-Name` werden Name und ID des Abonnements als Kontextname im Format `Subscription Name (subscription-id)` verwendet.

## <a name="change-the-active-azure-context"></a>Ändern des aktiven Azure-Kontexts

Der aktive Azure-Kontext kann sowohl mit `Set-AzContext` als auch mit [Select-AzContext](/powershell/module/az.accounts/set-azcontext) geändert werden. `Set-AzContext` erstellt wie unter [Erstellen eines neuen Azure-Kontexts auf der Grundlage von Abonnementinformationen](#create-a-new-azure-context-from-subscription-information) beschrieben einen neuen Azure-Kontext für ein Abonnement, sofern noch keiner vorhanden ist, und verwendet diesen dann als aktiven Kontext.

`Select-AzContext` ist nur für die Verwendung mit vorhandenen Azure-Kontexten vorgesehen und funktioniert ähnlich wie `Set-AzContext -Context`, ist aber für die Verwendung mit Piping konzipiert:

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

Genau wie viele andere Konto- und Kontextverwaltungsbefehle in Azure PowerShell unterstützen auch `Set-AzContext` und `Select-AzContext` das Argument `-Scope` zum Steuern der Aktivitätsdauer des Kontexts. Mithilfe von `-Scope` können Sie den aktiven Kontext einer einzelnen Sitzung ändern, ohne den Standardkontext zu ändern:

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

Zur Vermeidung des Kontextwechsels für eine gesamte PowerShell-Sitzung können alle Azure PowerShell-Befehle mithilfe des Arguments `-AzContext` für einen bestimmten Kontext ausgeführt werden:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

Der andere Hauptzweck von Kontexten mit Azure PowerShell-Cmdlets ist das Ausführen von Hintergrundbefehlen. Weitere Informationen zum Ausführen von PowerShell-Aufträgen mit Azure PowerShell finden Sie unter [Ausführen von Azure PowerShell-Cmdlets in PowerShell-Aufträgen](using-psjobs.md).

## <a name="save-azure-contexts-across-powershell-sessions"></a>Speichern von Azure-Kontexten zwischen PowerShell-Sitzungen

Azure-Kontexte werden standardmäßig für die Verwendung zwischen PowerShell-Sitzungen gespeichert. Dieses Verhalten kann wie folgt geändert werden:

* Melden Sie sich mithilfe von `Connect-AzAccount` unter Verwendung von `-Scope Process` an.

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  Der im Rahmen dieser Anmeldung zurückgegebene Azure-Kontext ist _ausschließlich_ für die aktuelle Sitzung gültig und wird unabhängig von der Einstellung für die automatische Azure PowerShell-Kontextspeicherung nicht automatisch gespeichert.
* Die automatische Kontextspeicherung von Azure PowerShell kann mithilfe des Cmdlets [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) deaktiviert werden.
  Gespeicherte Token werden durch die Deaktivierung der automatischen Kontextspeicherung __nicht__ gelöscht. Informationen zum Löschen gespeicherter Azure-Kontextinformationen finden Sie unter [Entfernen von Azure-Kontexten und gespeicherten Anmeldeinformationen](#remove-azure-contexts-and-stored-credentials).
* Die automatische Speicherung von Azure-Kontexten kann mithilfe des Cmdlets [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) explizit aktiviert werden. Bei aktivierter automatischer Speicherung werden alle Kontexte eines Benutzers lokal für spätere PowerShell-Sitzungen gespeichert.
* Mithilfe von [Save-AzContext](/powershell/module/az.accounts/save-azcontext) können Kontexte manuell gespeichert und mithilfe von [Import-AzContext](/powershell/module/az.accounts/import-azcontext) in späteren PowerShell-Sitzungen geladen werden:

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> Wenn Sie die automatische Kontextspeicherung deaktivieren, werden __keine__ gespeicherten Kontextinformationen gelöscht. Zum Entfernen gespeicherter Informationen muss das Cmdlet [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) verwendet werden. Weitere Informationen zum Entfernen gespeicherter Kontexte finden Sie unter [Entfernen von Azure-Kontexten und gespeicherten Anmeldeinformationen](#remove-azure-contexts-and-stored-credentials).

Jeder dieser Befehle unterstützt den Parameter `-Scope`. Dieser kann auf den Wert `Process` festgelegt werden, damit der Befehl nur für den aktuell ausgeführten Prozess gilt. Wenn Sie also beispielsweise sicherstellen möchten, dass neu erstellte Kontexte nach dem Verlassen einer PowerShell-Sitzung nicht gespeichert werden, verwenden Sie Folgendes:

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

Kontextinformationen und Token werden unter Windows im Verzeichnis `$env:USERPROFILE\.Azure` und auf anderen Plattformen unter `$HOME/.Azure` gespeichert. Es kann vorkommen, dass sensible Informationen wie Abonnement- und Mandanten-IDs in gespeicherten Informationen über Protokolle oder gespeicherte Kontexte offengelegt werden. Informationen zum Löschen gespeicherter Informationen finden Sie im Abschnitt [Entfernen von Azure-Kontexten und gespeicherten Anmeldeinformationen](#remove-azure-contexts-and-stored-credentials).

## <a name="remove-azure-contexts-and-stored-credentials"></a>Entfernen von Azure-Kontexten und gespeicherten Anmeldeinformationen

So löschen Sie Azure-Kontexte und -Anmeldeinformationen:

* Melden Sie sich mithilfe von [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount) von einem Konto ab.
  Zur Abmeldung können Sie entweder das Konto oder den Kontext verwenden:

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  Beim Trennen der Verbindung werden gespeicherte Authentifizierungstoken entfernt und gespeicherte Kontexte gelöscht, die dem getrennten Benutzer oder Kontext zugeordnet sind.
* Verwenden Sie [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext). Dieses Cmdlet entfernt zuverlässig gespeicherte Kontexte und Authentifizierungstoken und meldet Sie außerdem ab.
* Verwenden Sie zum Entfernen eines Kontexts das Cmdlet [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  Wenn Sie den aktiven Kontext entfernen, wird die Verbindung mit Azure getrennt, und Sie müssen sich mithilfe von `Connect-AzAccount` erneut authentifizieren.

## <a name="see-also"></a>Weitere Informationen

* [Ausführen von Azure PowerShell-Cmdlets in PowerShell-Aufträgen](using-psjobs.md)
* [Azure Active Directory-Terminologie](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [Az.Accounts](/powershell/module/az.accounts)
