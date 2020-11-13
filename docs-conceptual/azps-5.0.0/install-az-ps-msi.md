---
title: Installieren von Azure PowerShell mit einer MSI
description: Installieren von Azure PowerShell ohne PowerShellGet per MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: de9ac41b86e97c948943d22b2019c8022bdf52e0
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409515"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Installieren von Azure PowerShell unter Windows per MSI

In diesem Artikel erfahren Sie, wie Sie Azure PowerShell unter Windows mit einem MSI-Installationsprogramm installieren. Das MSI-Installationsprogramm wird für Umgebungen bereitgestellt, in denen der PowerShell-Katalog unter Umständen durch eine Firewall blockiert oder in denen ein Offlineinstallationsprogramm benötigt wird. Die empfohlene Vorgehensweise zum Installieren von Azure PowerShell ist die Verwendung von PowerShellGet. Eine Anleitung für die Installation von Azure PowerShell unter Verwendung von PowerShellGet finden Sie unter [Installieren von Azure PowerShell mit PowerShellGet](install-az-ps.md).

## <a name="requirements"></a>Requirements (Anforderungen)

Das MSI-Installationsprogramm unter Windows ist nur für die Installation von Azure PowerShell für PowerShell 5.1 konzipiert. Verwenden Sie zur Installation auf Nicht-Windows-Plattformen oder unter höheren Versionen von PowerShell [PowerShellGet](install-az-ps.md). Führen Sie den Befehl aus, um Ihre PowerShell-Version zu überprüfen:

```powershell-interactive
$PSVersionTable.PSVersion
```

Für die Verwendung von Azure PowerShell in PowerShell 5.1 ist Folgendes erforderlich:

1. Führen Sie bei Bedarf ein Update auf [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) aus. Unter Windows 10 ist PowerShell 5.1 bereits installiert.
2. Installieren Sie [.NET Framework 4.7.2 oder höher](/dotnet/framework/install).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Installieren oder Aktualisieren unter Windows mithilfe des MSI-Pakets

Das MSI-Paket für Azure PowerShell ist auf [GitHub](https://github.com/Azure/azure-powershell/releases) verfügbar:

1. Gehe zu https://github.com/Azure/azure-powershell/releases.
2. Suchen Sie nach dem aktuellen Katalogmodul für Azure PowerShell (diese sind chronologisch aufgelistet und in der Regel nur als Releaseversion ohne Namen, z. B. „4.7.0“).
3. Scrollen Sie zum unteren Rand der Patchnotizen, und klicken Sie auf den Pfeil neben „Ressourcen“, um die MSI-Optionen anzuzeigen.
4. Klicken Sie auf die MSI-Datei der Az-Cmdlets Ihrer Wahl, um den Download zu starten.

Ältere per MSI installierte Versionen von Azure PowerShell werden vom Installationsprogramm automatisch entfernt. Mit dem MSI-Paket werden Module unter `${env:ProgramFiles}\WindowsPowerShell\Modules` installiert.

Melden Sie sich mit Ihren Azure-Anmeldeinformationen an, um Azure PowerShell zu verwenden.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> Wenn Sie das automatische Laden von Modulen deaktiviert haben, müssen Sie das Modul manuell mit `Import-Module Az` importieren. Aufgrund der Modulstruktur kann dieser Vorgang bis zu einer Minute dauern.

Sie müssen diesen Schritt für jede neue PowerShell-Sitzung wiederholen, die Sie starten. Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung in PowerShell finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).

## <a name="provide-feedback"></a>Feedback geben

[Melden Sie auf GitHub ein Problem](https://github.com/Azure/azure-powershell/issues), wenn Sie in Azure PowerShell einen Fehler finden. Verwenden Sie das [Send-Feedback](/powershell/module/az.accounts/send-feedback)-Cmdlet, um über die Befehlszeile Feedback zu senden.

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zu Azure PowerShell-Modulen und den zugehörigen Features finden Sie unter [Erste Schritte mit Azure PowerShell](get-started-azureps.md). Falls Sie mit Azure PowerShell vertraut sind und die Migration aus AzureRM durchführen möchten, hilft Ihnen der Artikel [Migrieren von AzureRM zum Az-Modul von Azure PowerShell](migrate-from-azurerm-to-az.md) weiter.
