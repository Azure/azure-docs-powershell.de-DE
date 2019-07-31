---
title: Speichern von Azure-Anmeldeinformationen zwischen PowerShell-Sitzungen
description: Hier erfahren Sie, wie Sie Azure-Anmeldeinformationen und andere Informationen in mehreren PowerShell-Sitzungen wiederverwenden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 02b8090aa1868f24445ddff3a95c0d0c376e2cb8
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2019
ms.locfileid: "68658078"
---
# <a name="persist-azure-user-credentials-across-powershell-sessions"></a>Speichern von Azure-Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen

Azure PowerShell bietet ein Feature namens **Azure Context Autosave** mit den folgenden Funktionen:

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
- *Anmeldeinformationen*: Die Informationen, die von Azure verwendet werden, um Ihre Identität zu überprüfen und die Autorisierung des Zugriffs auf Ressourcen in Azure zu bestätigen.

Mit der aktuellen Version von Azure PowerShell können Azure-Kontexte jeweils automatisch gespeichert werden, wenn eine neue PowerShell-Sitzung geöffnet wird.

## <a name="automatically-save-the-context-for-the-next-sign-in"></a>Automatisches Speichern des Kontexts für die nächste Anmeldung

Azure PowerShell behält Ihre Kontextinformationen zwischen Sitzungen automatisch bei. Wenn PowerShell den Kontext und die Anmeldeinformationen verwerfen soll, verwenden Sie `Disable-AzContextAutoSave`. Wenn das Speichern des Kontexts deaktiviert ist, müssen Sie sich jedes Mal an Azure anmelden, wenn Sie eine PowerShell-Sitzung öffnen.

Mit `Enable-AzContextAutosave` können Sie es Azure PowerShell ermöglichen, den Kontext über das Sitzungsende hinaus zu speichern. Kontext und Anmeldeinformationen werden automatisch in einem speziellen ausgeblendeten Ordner in Ihrem Benutzerverzeichnis gespeichert (`$env:USERPROFILE\.Azure` unter Windows und `$HOME/.Azure` auf anderen Plattformen). Jede neue PowerShell-Sitzung verwendet den Kontext aus Ihrer letzten Sitzung als Ziel.

Die Cmdlets zum Verwalten von Azure-Kontexten ermöglichen eine präzise Steuerung. So können Sie festlegen, ob Änderungen nur für die aktuelle PowerShell-Sitzung (`Process`-Bereich) oder für jede PowerShell-Sitzung (`CurrentUser`-Bereich) gelten sollen. Ausführlichere Informationen zu diesen Optionen finden Sie unter [Verwenden von Kontextbereichen](#using-context-scopes).

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>Ausführen von Azure PowerShell-Cmdlets als Hintergrundaufträge

Dank der**automatischen Speicherung des Azure-Kontexts können** Sie Ihren Kontext auch für PowerShell-Hintergrundaufträge freigeben. Mit PowerShell können Sie Aufgaben mit langer Ausführungszeit als Hintergrundaufträge starten und überwachen, ohne auf den Abschluss der Aufgaben warten zu müssen. Sie können Anmeldeinformationen auf zwei Arten an Hintergrundaufträge weitergeben:

- Übergeben des Kontexts als Argument

  Bei den meisten AzureRM-Cmdlets kann der Kontext als Parameter an das Cmdlet übergeben werden. Das folgende Beispiel veranschaulicht das Übergeben eines Kontexts an einen Hintergrundauftrag:

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzContext)
  ```

- Verwenden des Standardkontexts bei aktivierter automatischer Speicherung

  Wenn Sie die **automatische Speicherung des Kontexts** aktiviert haben, wird von Hintergrundaufträgen automatisch der gespeicherte Standardkontext verwendet.

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzVm [... Additional parameters ...]}
  ```

Falls Sie das Ergebnis des Hintergrundauftrags ermitteln möchten, können Sie mit `Get-Job` den Auftragsstatus prüfen und mit `Wait-Job` auf den Abschluss des Auftrags warten. Mit `Receive-Job` können Sie die Ausgabe des Hintergrundauftrags erfassen oder anzeigen. Weitere Informationen finden Sie unter [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="creating-selecting-renaming-and-removing-contexts"></a>Erstellen, Auswählen, Umbenennen und Entfernen von Kontexten

Für die Kontexterstellung müssen Sie bei Azure angemeldet sein. Das Cmdlet `Connect-AzAccount` (oder dessen Alias `Login-AzAccount`) legt den von Azure PowerShell-Cmdlets verwendeten Standardkontext fest und ermöglicht den Zugriff auf beliebige Mandanten oder Abonnements, die im Rahmen Ihrer Anmeldeinformationen zulässig sind.

Verwenden Sie `Set-AzContext` (oder dessen Alias `Select-AzSubscription`), um nach der Anmeldung einen neuen Kontext hinzuzufügen.

```azurepowershell-interactive
PS C:\> Set-AzContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

Im vorherigen Beispiel wird ein neuer Kontext mit dem Ziel „Contoso Subscription 1“ und Ihren aktuellen Anmeldeinformationen hinzugefügt. Der neue Kontext heißt „Contoso1“. Falls Sie keinen Namen für den Kontext angeben, wird ein Standardname aus Konto-ID und Abonnement-ID verwendet.

Einen vorhandenen Kontext können Sie mithilfe des Cmdlets `Rename-AzContext` umbenennen. Beispiel:

```azurepowershell-interactive
PS C:\> Rename-AzContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

In diesem Beispiel wird der Kontext mit dem automatisch vergebenen Namen `[user1@contoso.org; 123456-7890-1234-564321]` in den einfachen Namen „Contoso2“ umbenannt. Dank Vervollständigung mit der TAB-TASTE können Sie in Kontextverwaltungs-Cmdlets schnell einen Kontext auswählen.

Zum Entfernen eines Kontexts steht das Cmdlet `Remove-AzContext` zur Verfügung.  Beispiel:

```azurepowershell-interactive
PS C:\> Remove-AzContext Contoso2
```

Verwirft den Kontext namens „Contoso2“. Sie können diesen Kontext neu erstellen, indem Sie `Set-AzContext` verwenden.

## <a name="removing-credentials"></a>Entfernen von Anmeldeinformationen

Mit `Disconnect-AzAccount` (auch bekannt als `Logout-AzAccount`) können Sie alle Anmeldeinformationen und zugeordneten Kontexte für einen Benutzer oder Dienstprinzipal entfernen. Wenn das Cmdlet `Disconnect-AzAccount` ohne Parameter ausgeführt wird, entfernt es alle Anmeldeinformationen und Kontexte, die dem Benutzer oder Dienstprinzipal im aktuellen Kontext zugeordnet sind. Wenn Sie einen bestimmten Prinzipal als Ziel verwenden möchten, können Sie einen Benutzernamen, Dienstprinzipalnamen oder Kontext übergeben.

```azurepowershell-interactive
Disconnect-AzAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>Verwenden von Kontextbereichen

Manchmal möchten Sie unter Umständen einen Kontext in einer PowerShell-Sitzung auswählen, ändern oder entfernen, ohne dass sich das auf andere Sitzungen auswirkt. Das Standardverhalten von Kontext-Cmdlets kann mithilfe des Parameters `Scope`geändert werden. Der Bereich `Process` überschreibt das Standardverhalten, indem er die Gültigkeit auf die aktuelle Sitzung beschränkt. Im Gegensatz dazu ändert der Bereich `CurrentUser` den Kontext nicht nur in der aktuellen Sitzung, sondern in allen Sitzungen.

Verwenden Sie beispielsweise Folgendes, um den Standardkontext in der aktuellen PowerShell-Sitzung zu ändern, ohne andere Fenster oder den Kontext zu beeinflussen, der beim nächsten Öffnen einer Sitzung verwendet wird:

```azurepowershell-interactive
PS C:\> Select-AzContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>Speicherung der Einstellung für die automatische Speicherung des Kontexts

Die Einstellung für die automatische Speicherung des Kontexts wird im Azure PowerShell-Benutzerverzeichnis gespeichert (`$env:USERPROFILE\.Azure` unter Windows und `$HOME/.Azure` auf anderen Plattformen). Manche Computerkonten haben möglicherweise keinen Zugriff auf dieses Verzeichnis. In solchen Fällen können Sie die Umgebungsvariable verwenden.

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

Bei Verwendung von „true“ wird der Kontext automatisch gespeichert. Bei Verwendung von „false“ wird der Kontext nicht gespeichert.

## <a name="context-management-cmdlets"></a>Cmdlets für die Kontextverwaltung

- [Enable-AzContextAutosave][enable]: Ermöglicht das Speichern des Kontexts zwischen PowerShell-Sitzungen.
  Änderungen wirken sich auf den globalen Kontext aus.
- [Disable-AzContextAutosave][disable]: Deaktiviert die automatische Speicherung des Kontexts. Bei jeder neuen PowerShell-Sitzung ist eine erneute Anmeldung erforderlich.
- [Select-AzContext][select]: Ermöglicht das Auswählen eines Standardkontexts. Alle Cmdlets verwenden die Anmeldeinformationen aus diesem Kontext für die Authentifizierung.
- [Disconnect-AzAccount][remove-cred]: Dient zum Entfernen aller einem Konto zugeordneten Anmeldeinformationen und Kontexte.
- [Remove-AzContext][remove-context]: Dient zum Entfernen eines benannten Kontexts.
- [Rename-AzContext][rename]: Dient zum Umbenennen eines vorhandenen Kontexts.
- [Add-AzAccount][login]: Ermöglicht es, den Gültigkeitsbereich der Anmeldung auf den Prozess oder auf den aktuellen Benutzer festzulegen.
  Ermöglicht die Benennung des Standardkontexts nach der Authentifizierung.
- [Import-AzContext][import]: Ermöglicht es, den Gültigkeitsbereich der Anmeldung auf den Prozess oder auf den aktuellen Benutzer festzulegen.
- [Set-AzContext][set-context]: Ermöglicht die Wahl vorhandener benannter Kontexte sowie die Festlegung, ob Änderungen auf den Prozess oder auf den aktuellen Benutzer angewendet werden sollen.

<!-- Hyperlinks -->
[enable]: /powershell/module/az.accounts/Enable-AzureRmContextAutosave
[disable]: /powershell/module/az.accounts/Disable-AzContextAutosave
[select]: /powershell/module/az.accounts/Select-AzContext
[remove-cred]: /powershell/module/az.accounts/Disconnect-AzAccount
[remove-context]: /powershell/module/az.accounts/Remove-AzContext
[rename]: /powershell/module/az.accounts/Rename-AzContext

<!-- Updated cmdlets -->
[login]: /powershell/module/az.accounts/Connect-AzAccount
[import]:  /powershell/module/az.accounts/Import-AzContext
[set-context]: /powershell/module/az.accounts/Set-AzContext
