---
title: Installieren von Azure PowerShell mit einer MSI
description: Installieren von Azure PowerShell ohne PowerShellGet per MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: d16aea3fa2059cd32f584134e2da43e01e3def31
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "75722005"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Installieren von Azure PowerShell unter Windows per MSI

In diesem Artikel erfahren Sie, wie Sie Azure PowerShell unter Windows mit einem MSI-Installationsprogramm installieren. Das MSI-Installationsprogramm wird für Umgebungen bereitgestellt, in denen der PowerShell-Katalog unter Umständen durch eine Firewall blockiert oder in denen ein Offlineinstallationsprogramm benötigt wird. Die empfohlene Vorgehensweise zum Installieren von Azure PowerShell ist die Verwendung von PowerShellGet. Eine Anleitung für die Installation von Azure PowerShell unter Verwendung von PowerShellGet finden Sie unter [Installieren von Azure PowerShell mit PowerShellGet](install-az-ps.md).

## <a name="requirements"></a>Requirements (Anforderungen)

Das MSI-Installationsprogramm für Azure PowerShell funktioniert __nur__ für PowerShell 5.1 unter Windows. Verwenden Sie zur Installation auf Nicht-Windows-Plattformen oder unter höheren Versionen von PowerShell [PowerShellGet](install-az-ps.md).
Führen Sie den Befehl aus, um Ihre PowerShell-Version zu überprüfen:

```powershell-interactive
$PSVersionTable.PSVersion
```

Für die Verwendung von Azure PowerShell in PowerShell 5.1 ist Folgendes erforderlich:

1. Führen Sie bei Bedarf ein Update auf [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) aus. Unter Windows 10 ist PowerShell 5.1 bereits installiert.
2. Installieren Sie [.NET Framework 4.7.2 oder höher](/dotnet/framework/install).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Installieren oder Aktualisieren unter Windows mithilfe des MSI-Pakets

Azure PowerShell für Windows wird mithilfe der auf [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v2.8.0-October2019) verfügbaren MSI-Datei installiert. Ältere per MSI installierte Versionen von Azure-Modulen werden vom Installationsprogramm automatisch entfernt. Mit dem MSI-Paket werden Module unter `${env:ProgramFiles}\WindowsPowerShell\Modules` installiert.

Melden Sie sich mit Ihren Azure-Anmeldeinformationen an, um Azure PowerShell zu verwenden.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
>
> Wenn Sie das automatische Laden von Modulen deaktiviert haben, müssen Sie das Modul manuell mit `Import-Module Az` importieren. Aufgrund der Modulstruktur kann dieser Vorgang bis zu einer Minute dauern.

Sie müssen diesen Schritt für jede neue PowerShell-Sitzung wiederholen, die Sie starten. Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung in PowerShell finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).

## <a name="provide-feedback"></a>Feedback geben

[Melden Sie auf GitHub ein Problem](https://github.com/Azure/azure-powershell/issues), wenn Sie in Azure PowerShell einen Fehler finden.
Verwenden Sie das [Send-Feedback](/powershell/module/az.accounts/send-feedback)-Cmdlet, um über die Befehlszeile Feedback zu senden.

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zu Azure PowerShell-Modulen und den zugehörigen Features finden Sie unter [Erste Schritte mit Azure PowerShell](get-started-azureps.md).
Falls Sie mit Azure PowerShell vertraut sind und die Migration aus AzureRM durchführen möchten, hilft Ihnen der Artikel [Migrieren von AzureRM zum Az-Modul von Azure PowerShell](migrate-from-azurerm-to-az.md) weiter.
