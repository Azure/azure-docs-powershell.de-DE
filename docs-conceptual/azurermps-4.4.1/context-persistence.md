---
title: Speichern von Benutzeranmeldungen zwischen PowerShell-Sitzungen
description: Dieser Artikel enthält Informationen zu neuen Features in Azure PowerShell, mit denen Sie Anmeldeinformationen und andere Benutzerinformationen zwischen mehreren PowerShell-Sitzungen wiederverwenden können.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: d650cfaae580acd10b3ddb06edec9883f1a32844
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853966"
---
# <a name="persisting-user-logins-across-powershell-sessions"></a>Speichern von Benutzeranmeldungen zwischen PowerShell-Sitzungen

In der Azure PowerShell-Version vom September 2017 wird für Azure Resource Manager-Cmdlets ein neues Feature eingeführt: die**** automatische Speicherung des Azure-Kontexts. Dieses Feature kann beispielsweise für folgende neue Benutzerszenarien verwendet werden:

- Speicherung von Anmeldeinformationen zur Wiederverwendung in neuen PowerShell-Sitzungen
- Einfachere Verwendung von Hintergrundaufgaben für die Ausführung von Cmdlets mit langer Ausführungszeit
- Wechsel zwischen Konten, Abonnements und Umgebungen ohne separate Anmeldung
- Gleichzeitige Ausführung von Aufgaben mit unterschiedlichen Anmeldeinformationen und Abonnements über die gleiche PowerShell-Sitzung

## <a name="azure-contexts-defined"></a>Definition von Azure-Kontexten

Bei einem *Azure-Kontext* handelt es sich um einen Satz von Informationen, die das Ziel von Azure PowerShell-Cmdlets definieren. Der Kontext setzt sich aus fünf Teilen zusammen:

- Ein *Konto*: Der Benutzername oder Dienstprinzipal, der verwendet wird, um die Kommunikation mit Azure zu authentifizieren.
- Ein *Abonnement*: Das Azure-Abonnement mit den Ressourcen, für die eine Aktion ausgeführt wird.
- Ein *Mandant*: Der Azure Active Directory-Mandant mit Ihrem Abonnement. Mandanten sind eher für die Dienstprinzipalauthentifizierung relevant.
- Eine *Umgebung*: Die spezielle Azure-Cloud, die als Ziel fungiert (in der Regel die globale Azure-Cloud).
  Über die Umgebungseinstellung können Sie jedoch auch nationale Clouds, Government Clouds und lokale Clouds (Azure Stack) als Ziel festlegen.
- *Anmeldeinformationen*: Die Informationen, die von Azure verwendet werden, um Ihre Identität zu überprüfen und die Autorisierung des Zugriffs auf Ressourcen in Azure zu gewährleisten.

In früheren Versionen musste der Azure-Kontext bei jedem Öffnen einer neuen PowerShell-Sitzung erstellt werden. Ab Azure PowerShell 4.4.0 können Sie die automatische Speicherung und Wiederverwendung von Azure-Kontexten beim Öffnen einer neuen PowerShell-Sitzung aktivieren.

## <a name="automatically-saving-the-context-for-the-next-login"></a>Automatisches Speichern des Kontexts für die nächste Anmeldung

Standardmäßig verwirft Azure PowerShell Ihre Kontextinformationen, sobald Sie die PowerShell-Sitzung beenden.

Mit `Enable-AzureRmContextAutosave` können Sie es Azure PowerShell ermöglichen, den Kontext über das Sitzungsende hinaus zu speichern. Kontext und Anmeldeinformationen werden automatisch in einem speziellen ausgeblendeten Ordner in Ihrem Benutzerverzeichnis (`%AppData%\Roaming\Windows Azure PowerShell`) gespeichert.
Anschließend verwendet jede neue PowerShell-Sitzung den Kontext aus Ihrer letzten Sitzung als Ziel.

Wenn PowerShell den Kontext und die Anmeldeinformationen verwerfen soll, verwenden Sie `Disable-AzureRmContextAutoSave`. Daraufhin müssen Sie sich jedes Mal anmelden, wenn Sie eine PowerShell-Sitzung öffnen.

Die Cmdlets zum Verwalten von Azure-Kontexten ermöglichen eine präzise Steuerung. So können Sie festlegen, ob Änderungen nur für die aktuelle PowerShell-Sitzung (`Process`-Bereich) oder für jede PowerShell-Sitzung (`CurrentUser`-Bereich) gelten sollen. Ausführlichere Informationen zu diesen Optionen finden Sie unter [Verwenden von Kontextbereichen](#Using-Context-Scopes).

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>Ausführen von Azure PowerShell-Cmdlets als Hintergrundaufträge

Dank der**** automatischen Speicherung des Azure-Kontexts können Sie Ihren Kontext auch für PowerShell-Hintergrundaufträge freigeben. Mit PowerShell können Sie Aufgaben mit langer Ausführungszeit als Hintergrundaufträge starten und überwachen, ohne auf den Abschluss der Aufgaben warten zu müssen. Sie können Anmeldeinformationen auf zwei Arten an Hintergrundaufträge weitergeben:

- Übergeben des Kontexts als Argument

  Bei den meisten AzureRM-Cmdlets kann der Kontext als Parameter an das Cmdlet übergeben werden. Das folgende Beispiel veranschaulicht das Übergeben eines Kontexts an einen Hintergrundauftrag:

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- Verwenden des Standardkontexts bei aktivierter automatischer Speicherung

  Wenn Sie die automatische Speicherung des Kontexts**** aktiviert haben, wird von Hintergrundaufträgen automatisch der gespeicherte Standardkontext verwendet.

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

Falls Sie das Ergebnis des Hintergrundauftrags ermitteln möchten, können Sie mit `Get-Job` den Auftragsstatus prüfen und mit `Wait-Job` auf den Abschluss des Auftrags warten. Mit `Receive-Job` können Sie die Ausgabe des Hintergrundauftrags erfassen oder anzeigen. Weitere Informationen finden Sie unter [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="creating-selecting-renaming-and-removing-contexts"></a>Erstellen, Auswählen, Umbenennen und Entfernen von Kontexten

Für die Kontexterstellung müssen Sie bei Azure angemeldet sein. Das Cmdlet `Add-AzureRmAccount` (oder dessen Alias `Login-AzureRmAccount`) legt den von nachfolgenden Azure PowerShell-Cmdlets verwendeten Standardkontext fest und ermöglicht den Zugriff auf beliebige Mandanten oder Abonnements, die im Rahmen Ihrer Anmeldeinformationen zulässig sind.

Verwenden Sie `Set-AzureRmContext` (oder dessen Alias `Select-AzureRmSubscription`), um nach der Anmeldung einen neuen Kontext hinzuzufügen.

```powershell
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

Im vorherigen Beispiel wird ein neuer Kontext mit dem Ziel „Contoso Subscription 1“ und Ihren aktuellen Anmeldeinformationen hinzugefügt. Der neue Kontext heißt „Contoso1“. Falls Sie keinen Namen für den Kontext angeben, wird ein Standardname aus Konto-ID und Abonnement-ID verwendet.

Einen vorhandenen Kontext können Sie mithilfe des Cmdlets `Rename-AzureRmContext` umbenennen. Beispiel: 

```powershell
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

In diesem Beispiel wird der Kontext mit dem automatisch vergebenen Namen `[user1@contoso.org; 123456-7890-1234-564321]` in den einfachen Namen „Contoso2“ umbenannt. Dank Vervollständigung mit der TAB-TASTE können Sie in Kontextverwaltungs-Cmdlets schnell einen Kontext auswählen.

Zum Entfernen eines Kontexts steht das Cmdlet `Remove-AzureRmContext` zur Verfügung.  Beispiel: 

```powershell
PS C:\> Remove-AzureRmContext Contoso2
```

Verwirft den Kontext namens „Contoso2“. Er kann anschließend mit `Set-AzureRmContext` erneut erstellt werden.

## <a name="removing-credentials"></a>Entfernen von Anmeldeinformationen

Mit `Remove-AzureRmAccount` (auch bekannt als `Logout-AzureRmAccount`) können Sie alle Anmeldeinformationen und zugeordneten Kontexte für einen Benutzer oder Dienstprinzipal entfernen. Wenn das Cmdlet `Remove-AzureRmAccount` ohne Parameter ausgeführt wird, entfernt es alle Anmeldeinformationen und Kontexte, die dem Benutzer oder Dienstprinzipal im aktuellen Kontext zugeordnet sind. Wenn Sie einen bestimmten Prinzipal als Ziel verwenden möchten, können Sie einen Benutzernamen, Dienstprinzipalnamen oder Kontext übergeben.

```powershell
Remove-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>Verwenden von Kontextbereichen

Manchmal möchten Sie unter Umständen einen Kontext in einer PowerShell-Sitzung auswählen, ändern oder entfernen, ohne dass sich das auf andere Sitzungen auswirkt. Das Standardverhalten von Kontext-Cmdlets kann mithilfe des Parameters `Scope`geändert werden. Der Bereich `Process` überschreibt das Standardverhalten, indem er die Gültigkeit auf die aktuelle Sitzung beschränkt. Im Gegensatz dazu ändert der Bereich `CurrentUser` den Kontext nicht nur in der aktuellen Sitzung, sondern in allen Sitzungen.

Verwenden Sie beispielsweise Folgendes, um den Standardkontext in der aktuellen PowerShell-Sitzung zu ändern, ohne andere Fenster oder den Kontext zu beeinflussen, der beim nächsten Öffnen einer Sitzung verwendet wird:

```powershell
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>Speicherung der Einstellung für die automatische Speicherung des Kontexts

Die Einstellung für die automatische Speicherung des Kontexts wird im Azure PowerShell-Verzeichnis des Benutzers (`%AppData%\Roaming\Windows Azure PowerShell`) gespeichert. Manche Computerkonten haben möglicherweise keinen Zugriff auf dieses Verzeichnis. In solchen Fällen können Sie die Umgebungsvariable verwenden.

```powershell
$env:AzureRmContextAutoSave="true" | "false"
```

Bei Verwendung von „true“ wird der Kontext automatisch gespeichert. Bei Verwendung von „false“ wird der Kontext nicht gespeichert.

## <a name="changes-to-the-azurermprofile-module"></a>Änderungen am Modul „AzureRM.Profile“

Neue Cmdlets für die Kontextverwaltung

- [Enable-AzureRmContextAutosave][enable]: Ermöglicht das Speichern des Kontexts zwischen PowerShell-Sitzungen.
  Änderungen wirken sich auf den globalen Kontext aus.
- [Disable-AzureRmContextAutosave][disable]: Deaktiviert die automatische Speicherung des Kontexts. Bei jeder neuen PowerShell-Sitzung ist eine erneute Anmeldung erforderlich.
- [Select-AzureRmContext][select]: Ermöglicht das Auswählen eines Standardkontexts. Alle nachfolgenden Cmdlets verwenden die Anmeldeinformationen aus diesem Kontext für die Authentifizierung.
- [Remove-AzureRmAccount][remove-cred]: Dient zum Entfernen aller einem Konto zugeordneten Anmeldeinformationen und Kontexte.
- [Remove-AzureRmContext][remove-context]: Dient zum Entfernen eines benannten Kontexts.
- [Rename-AzureRmContext][rename]: Dient zum Umbenennen eines vorhandenen Kontexts.

Änderungen an vorhandenen Profil-Cmdlets

- [Add-AzureRmAccount][login]: Ermöglicht es, den Gültigkeitsbereich der Anmeldung auf den Prozess oder auf den aktuellen Benutzer festzulegen.
  Ermöglicht die Benennung des Standardkontexts nach der Anmeldung.
- [Import-AzureRmContext][import]: Ermöglicht es, den Gültigkeitsbereich der Anmeldung auf den Prozess oder auf den aktuellen Benutzer festzulegen.
- [Set-AzureRmContext][set-context]: Ermöglicht die Wahl vorhandener benannter Kontexte sowie die Festlegung, ob Änderungen auf den Prozess oder auf den aktuellen Benutzer angewendet werden sollen.

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Remove-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Add-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
