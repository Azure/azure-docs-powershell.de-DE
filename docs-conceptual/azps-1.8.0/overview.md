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
ms.openlocfilehash: 710decaf8fcc0ba57e1e978a665474047393adc7
ms.sourcegitcommit: 5bdedc77b27b66998387486761ec67ed9326f169
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2019
ms.locfileid: "67345243"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="7fbec-103">Übersicht über Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7fbec-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="7fbec-104">Azure PowerShell bietet eine Reihe von Cmdlets, die das [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview)-Modell für die Verwaltung von Azure-Ressourcen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7fbec-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="7fbec-105">Für Azure PowerShell wird .NET Standard verwendet, damit die Umgebung für Windows, macOS und Linux verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7fbec-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="7fbec-106">Azure PowerShell steht auch in Azure Cloud Shell zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7fbec-106">Azure PowerShell is also available on Azure Cloud Shell.</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="7fbec-107">Informationen zum neuen Az-Modul</span><span class="sxs-lookup"><span data-stu-id="7fbec-107">About the new Az module</span></span>

<span data-ttu-id="7fbec-108">In dieser Dokumentation wird das neue Az-Modul für Azure PowerShell beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7fbec-108">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="7fbec-109">Dieses neue Modul wurde von Grund auf in .NET Standard geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7fbec-109">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="7fbec-110">Bei Verwendung von .NET Standard kann Azure PowerShell unter PowerShell 5.1 auf Windows oder PowerShell Core 6.x oder höher auf einer beliebigen Plattform ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7fbec-110">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.1 on Windows or PowerShell Core 6.x and later on any platform.</span></span> <span data-ttu-id="7fbec-111">Das Az-Modul ist jetzt die bevorzugte Vorgehensweise für die Interaktion mit Azure über PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7fbec-111">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="7fbec-112">Für AzureRM werden weiterhin Fehlerbehebungen bereitgestellt, aber keine neuen Features mehr.</span><span class="sxs-lookup"><span data-stu-id="7fbec-112">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="7fbec-113">Alle Details zum neuen Modul, z.B. die Umbenennung der Befehle und die Wartungspläne für AzureRM, finden Sie unter [Einführung in das Az-Modul von Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="7fbec-113">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="7fbec-114">Wenn Sie gleich in die Nutzung des neuen Moduls einsteigen möchten, können Sie den Artikel [Migrieren von AzureRM zum Az-Modul von Azure PowerShell](migrate-from-azurerm-to-az.md) lesen.</span><span class="sxs-lookup"><span data-stu-id="7fbec-114">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="7fbec-115">Darüber hinaus ist die [AzureRM-Dokumentation](/powershell/azure/azurerm) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7fbec-115">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="7fbec-116">Während die Azure-Dokumentation aktualisiert wird, damit die neuen Cmdlet-Namen des Moduls darin widergespiegelt werden, werden in den Artikeln unter Umständen vorerst noch die AzureRM-Befehle verwendet.</span><span class="sxs-lookup"><span data-stu-id="7fbec-116">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="7fbec-117">Nach der Installation des Az-Moduls ist es ratsam, die Cmdlet-Aliase von AzureRM mit `Enable-AzureRmAlias` zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7fbec-117">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="7fbec-118">Ausführlichere Informationen finden Sie im Artikel [Migrieren von AzureRM zum Az-Modul von Azure PowerShell](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="7fbec-118">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="7fbec-119">Ausführen oder Installieren</span><span class="sxs-lookup"><span data-stu-id="7fbec-119">Run or install</span></span>

<span data-ttu-id="7fbec-120">Sie können Azure PowerShell auf PowerShell 5.1 oder höher unter Windows und PowerShell Core 6.x oder höher auf jeder Plattform installieren oder in Azure Cloud Shell ausführen.</span><span class="sxs-lookup"><span data-stu-id="7fbec-120">You can install Azure PowerShell on PowerShell 5.1 or higher on Windows, PowerShell Core 6.x and later on any platform, or run in Azure Cloud Shell.</span></span>

* <span data-ttu-id="7fbec-121">Informationen zum Ausführen im Browser mit Azure Cloud Shell finden Sie unter [Schnellstart für PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="7fbec-121">To run in your browser with Azure Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="7fbec-122">Informationen zum Installieren von Azure PowerShell auf Ihrem System finden Sie unter [Install Azure PowerShell](install-az-ps.md) (Installieren von Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="7fbec-122">To install Azure PowerShell on your system, see [Install Azure PowerShell](install-az-ps.md).</span></span>

<span data-ttu-id="7fbec-123">Informationen zur neuesten Azure PowerShell-Version finden Sie in den [Versionshinweisen](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="7fbec-123">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="7fbec-124">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="7fbec-124">Get Started</span></span>

<span data-ttu-id="7fbec-125">Lesen Sie den Artikel [Get Started with Azure PowerShell](get-started-azureps.md) (Erste Schritte mit Azure PowerShell), um sich über die Grundlagen von Azure PowerShell zu informieren.</span><span class="sxs-lookup"><span data-stu-id="7fbec-125">Read the [Get Started with Azure PowerShell](get-started-azureps.md) article to learn the Azure PowerShell basics.</span></span> <span data-ttu-id="7fbec-126">Falls Sie noch nicht mit PowerShell vertraut sind, kann es hilfreich sein, eine Einführung zu lesen:</span><span class="sxs-lookup"><span data-stu-id="7fbec-126">If you're not familiar with PowerShell, an introduction might be helpful:</span></span>

* [<span data-ttu-id="7fbec-127">Installieren von PowerShell</span><span class="sxs-lookup"><span data-stu-id="7fbec-127">Install PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
* [<span data-ttu-id="7fbec-128">Skripterstellung mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="7fbec-128">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)
* <span data-ttu-id="7fbec-129">[PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (PowerShell-Grundlagen – Teil 1: Erste Schritte mit PowerShell)</span><span class="sxs-lookup"><span data-stu-id="7fbec-129">[PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)</span></span>
* <span data-ttu-id="7fbec-130">[Getting Started with PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) (Erste Schritte mit PowerShell) in der Microsoft Virtual Academy</span><span class="sxs-lookup"><span data-stu-id="7fbec-130">Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)</span></span>

<span data-ttu-id="7fbec-131">Die folgenden Beispiele veranschaulichen einige gängige Nutzungsszenarien von Azure:</span><span class="sxs-lookup"><span data-stu-id="7fbec-131">The following samples can help you with some common uses of Azure:</span></span>

* [<span data-ttu-id="7fbec-132">Virtuelle Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="7fbec-132">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="7fbec-133">Virtuelle Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="7fbec-133">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="7fbec-134">Web-Apps</span><span class="sxs-lookup"><span data-stu-id="7fbec-134">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="7fbec-135">SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="7fbec-135">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="7fbec-136">Erweitern Ihrer Fähigkeiten mit Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="7fbec-136">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="7fbec-137">Automatisieren von Azure-Aufgaben mithilfe von Skripts über PowerShell</span><span class="sxs-lookup"><span data-stu-id="7fbec-137">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="7fbec-138">Mehr interaktives Lernen...</span><span class="sxs-lookup"><span data-stu-id="7fbec-138">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="7fbec-139">Andere Azure PowerShell-Module</span><span class="sxs-lookup"><span data-stu-id="7fbec-139">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="7fbec-140">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="7fbec-140">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="7fbec-141">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7fbec-141">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="7fbec-142">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="7fbec-142">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
