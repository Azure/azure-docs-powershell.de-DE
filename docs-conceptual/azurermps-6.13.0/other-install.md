---
title: Andere Installationsmöglichkeiten für Azure PowerShell
description: Installieren von Azure PowerShell ohne PowerShellGet per MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: e1d8877c185b4537c476128e279eda563f2575d1
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "83385863"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Installieren von Azure PowerShell unter Windows per MSI

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

In diesem Artikel erfahren Sie, wie Sie Azure PowerShell unter Windows mit einem MSI-Installationsprogramm installieren.  
Verwenden Sie diese Installationsmethoden nur, wenn sie für Ihr System erforderlich sind. Die empfohlene Vorgehensweise zum Installieren von Azure PowerShell unter Windows ist die Verwendung von PowerShellGet. Eine Anleitung für die Installation von Azure PowerShell unter Verwendung von PowerShellGet finden Sie unter [Installieren von Azure PowerShell mit PowerShellGet](install-azurerm-ps.md).

> [!NOTE]
> Die Vorgehensweise mit dem Webplattform-Installer für die Installation ist für die Versionen Azure PowerShell 6.x und höher nicht mehr verfügbar. Falls Sie den Webplattform-Installer benötigen, können Sie stattdessen die Nutzung des MSI-Installationsprogramms erwägen, oder Sie können eine frühere Version von Azure PowerShell installieren.

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Installieren oder Aktualisieren unter Windows mithilfe des MSI-Pakets

Azure PowerShell für Windows PowerShell 5.x kann mithilfe der bei [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018) verfügbaren MSI-Datei installiert werden. Ältere per MSI installierte Versionen von Azure-Modulen werden vom Installationsprogramm automatisch entfernt. Mit dem MSI-Paket werden Module unter `${env:ProgramFiles}\WindowsPowerShell\Modules` installiert. Sowohl das Modul `AzureRM` als auch das Modul `Azure` werden installiert.

> [!NOTE]
> Verwenden Sie das Modul `Azure` nur, wenn Sie mit dem klassischen Azure-Bereitstellungsmodell arbeiten.

Melden Sie sich mit Ihren Azure-Anmeldeinformationen an, um Azure PowerShell zu verwenden.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> Wenn Sie das automatische Laden von Modulen deaktiviert haben, müssen Sie das Modul manuell mit `Import-Module AzureRM` importieren. Aufgrund der Modulstruktur kann dieser Vorgang einige Sekunden dauern.

Sie müssen diesen Schritt für jede neue PowerShell-Sitzung wiederholen, die Sie starten. Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung in PowerShell finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).
