---
title: Übersicht über Azure PowerShell
description: Enthält eine Übersicht über das Azure PowerShell Az-Modul und Informationen zur Installation und zum Einstieg.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 1978ba5415a27349ac68175144cca0d89fa26d96
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657619"
---
# <a name="overview-of-azure-powershell"></a>Übersicht über Azure PowerShell

Azure PowerShell bietet eine Reihe von Cmdlets, die das [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview)-Modell für die Verwaltung von Azure-Ressourcen verwenden. Für Azure PowerShell wird .NET Standard verwendet, damit die Umgebung für Windows, macOS und Linux verfügbar ist.
Azure PowerShell steht auch in Azure Cloud Shell zur Verfügung.

## <a name="about-the-new-az-module"></a>Informationen zum neuen Az-Modul

In dieser Dokumentation wird das neue Az-Modul für Azure PowerShell beschrieben. Dieses neue Modul wurde von Grund auf in .NET Standard geschrieben. Bei Verwendung von .NET Standard kann Azure PowerShell unter PowerShell 5.1 auf Windows oder PowerShell Core 6.x oder höher auf einer beliebigen Plattform ausgeführt werden. Das Az-Modul ist jetzt die bevorzugte Vorgehensweise für die Interaktion mit Azure über PowerShell.
Für AzureRM werden weiterhin Fehlerbehebungen bereitgestellt, aber keine neuen Features mehr.

Alle Details zum neuen Modul, z.B. die Umbenennung der Befehle und die Wartungspläne für AzureRM, finden Sie unter [Einführung in das Az-Modul von Azure PowerShell](new-azureps-module-az.md). Wenn Sie gleich in die Nutzung des neuen Moduls einsteigen möchten, können Sie den Artikel [Migrieren von AzureRM zum Az-Modul von Azure PowerShell](migrate-from-azurerm-to-az.md) lesen.

Darüber hinaus ist die [AzureRM-Dokumentation](/powershell/azure/azurerm) verfügbar.

> [!IMPORTANT]
>
> Während die Azure-Dokumentation aktualisiert wird, damit die neuen Cmdlet-Namen des Moduls darin widergespiegelt werden, werden in den Artikeln unter Umständen vorerst noch die AzureRM-Befehle verwendet. Nach der Installation des Az-Moduls ist es ratsam, die Cmdlet-Aliase von AzureRM mit `Enable-AzureRmAlias` zu aktivieren. Ausführlichere Informationen finden Sie im Artikel [Migrieren von AzureRM zum Az-Modul von Azure PowerShell](migrate-from-azurerm-to-az.md).

## <a name="run-or-install"></a>Ausführen oder Installieren

Sie können Azure PowerShell auf PowerShell 5.1 oder höher unter Windows und PowerShell Core 6.x oder höher auf jeder Plattform installieren oder in Azure Cloud Shell ausführen.

* Informationen zum Ausführen im Browser mit Azure Cloud Shell finden Sie unter [Schnellstart für PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).
* Informationen zum Installieren von Azure PowerShell auf Ihrem System finden Sie unter [Install Azure PowerShell](install-az-ps.md) (Installieren von Azure PowerShell).

Informationen zur neuesten Azure PowerShell-Version finden Sie in den [Versionshinweisen](release-notes-azureps.md).

## <a name="get-started"></a>Erste Schritte

Lesen Sie den Artikel [Get Started with Azure PowerShell](get-started-azureps.md) (Erste Schritte mit Azure PowerShell), um sich über die Grundlagen von Azure PowerShell zu informieren. Falls Sie noch nicht mit PowerShell vertraut sind, kann es hilfreich sein, eine Einführung zu lesen:

* [Installieren von PowerShell](/powershell/scripting/install/installing-powershell)
* [Skripterstellung mit PowerShell](/powershell/scripting/powershell-scripting)
* [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (PowerShell-Grundlagen – Teil 1: Erste Schritte mit PowerShell)

Die folgenden Beispiele veranschaulichen einige gängige Nutzungsszenarien von Azure:

* [Virtuelle Linux-Computer](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Virtuelle Windows-Computer](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Web-Apps](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [SQL-Datenbanken](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a>Erweitern Ihrer Fähigkeiten mit Microsoft Learn

- [Automatisieren von Azure-Aufgaben mithilfe von Skripts über PowerShell](/learn/modules/automate-azure-tasks-with-powershell/)
- [Mehr interaktives Lernen...](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>Andere Azure PowerShell-Module

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure ElasticDB](/powershell/azure/elasticdbjobs/)
