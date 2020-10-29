---
title: Migrieren von Azure PowerShell-Skripts von AzureRM zu Az
description: Hier lernen Sie die Schritte und Tools kennen, mit denen Sie Skripts vom AzureRM-Modul zum neuen Az-Modul migrieren können.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753616"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="58dc3-103">Migrieren von Azure PowerShell von AzureRM zum Az-Modul</span><span class="sxs-lookup"><span data-stu-id="58dc3-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="58dc3-104">Alle Versionen des AzureRM PowerShell-Moduls sind veraltet, werden aber weiterhin unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58dc3-104">All versions of the AzureRM PowerShell module are outdated, but not out of support.</span></span> <span data-ttu-id="58dc3-105">Für die Interaktion mit Azure wird nun das [Az PowerShell-Modul](install-az-ps.md) empfohlen.</span><span class="sxs-lookup"><span data-stu-id="58dc3-105">The [Az PowerShell module](install-az-ps.md) is now the recommended PowerShell module for interacting with Azure.</span></span>

<span data-ttu-id="58dc3-106">Für die AzureRM-Cmdlets geschriebene Skripts funktionieren nicht automatisch auch mit dem neuen Modul.</span><span class="sxs-lookup"><span data-stu-id="58dc3-106">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="58dc3-107">Um den Umstieg zu vereinfachen, wurde das [Toolkit für die Migration von AzureRM zu Az](https://github.com/Azure/azure-powershell-migration) entwickelt.</span><span class="sxs-lookup"><span data-stu-id="58dc3-107">To make the transition easier, the [AzureRM to Az migration toolkit](https://github.com/Azure/azure-powershell-migration) was developed.</span></span> <span data-ttu-id="58dc3-108">Eine Migration zu einem neuen Befehlssatz ist immer unangenehm. Dieser Artikel hilft Ihnen jedoch dabei, den Umstieg auf das Az PowerShell-Modul in die Wege zu leiten.</span><span class="sxs-lookup"><span data-stu-id="58dc3-108">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the Az PowerShell module.</span></span> <span data-ttu-id="58dc3-109">Weitere Informationen zu den Gründen für die Entwicklung des Az PowerShell-Moduls finden Sie unter [Einführung in das neue Azure PowerShell Az-Modul](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="58dc3-109">To learn more about why the Az PowerShell module was created, see [Introducing the new Azure PowerShell Az module](new-azureps-module-az.md).</span></span>

<span data-ttu-id="58dc3-110">Die vollständige Liste mit grundlegenden Änderungen zwischen AzureRM und Az finden Sie unter [Vollständige Änderungen von AzureRM zu Az](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="58dc3-110">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="58dc3-111">Vergewissern, dass vorhandene Skripts mit der neuesten AzureRM-Version funktionieren</span><span class="sxs-lookup"><span data-stu-id="58dc3-111">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="58dc3-112">Überprüfen Sie, welche Versionen von AzureRM auf Ihrem System installiert sind, bevor Sie Migrationsschritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="58dc3-112">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span>
<span data-ttu-id="58dc3-113">So können Sie sicherstellen, dass für Skripts bereits das aktuelle Release verwendet wird, und Sie können ermitteln, welche Versionen von AzureRM deinstalliert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="58dc3-113">Doing so allows you to make sure scripts are already running on the latest release, and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="58dc3-114">Führen Sie das folgende Beispiel aus, um zu überprüfen, welche Versionen von AzureRM bei Ihnen installiert sind:</span><span class="sxs-lookup"><span data-stu-id="58dc3-114">To check which version(s) of AzureRM you have installed, run the following example:</span></span>

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

<span data-ttu-id="58dc3-115">Die **aktuellste** verfügbare Version von AzureRM ist **6.13.1** .</span><span class="sxs-lookup"><span data-stu-id="58dc3-115">The **latest** available release of AzureRM is **6.13.1** .</span></span> <span data-ttu-id="58dc3-116">Sollte diese Version nicht installiert sein, sind für die Verwendung des Az-Moduls möglicherweise zusätzliche Änderungen für Ihre vorhandenen Skripts erforderlich, die über die Beschreibungen in diesem Artikel und in der [Breaking Changes-Liste](migrate-az-1.0.0.md) hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="58dc3-116">If you don't have this version installed, your existing scripts may need additional modifications to work with the Az module beyond what's described in this article and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="58dc3-117">Wenn Ihre Skripts nicht mit AzureRM 6.13.1 funktionieren, aktualisieren Sie sie gemäß dem [Leitfaden zur Migration von AzureRM 5.x zu 6.x](/powershell/azure/azurerm/migration-guide.6.0.0).</span><span class="sxs-lookup"><span data-stu-id="58dc3-117">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span> <span data-ttu-id="58dc3-118">Wenn Sie eine frühere Version des AzureRM-Moduls verwenden, gibt es für jede Hauptversion Migrationsleitfäden.</span><span class="sxs-lookup"><span data-stu-id="58dc3-118">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="install-the-azurerm-to-az-migration-toolkit"></a><span data-ttu-id="58dc3-119">Installieren des Toolkits für die Migration von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="58dc3-119">Install the AzureRM to Az migration toolkit</span></span>

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a><span data-ttu-id="58dc3-120">Automatisches Migrieren Ihrer PowerShell-Skripts</span><span class="sxs-lookup"><span data-stu-id="58dc3-120">Automatically migrate your PowerShell scripts</span></span>

<span data-ttu-id="58dc3-121">Mit dem Toolkit für die Migration von AzureRM zu Az können Sie einen Plan generieren, um zu ermitteln, welche Änderungen für Ihre Skripts vorgenommen werden, bevor Sie tatsächlich Änderungen vornehmen und das Az PowerShell-Modul installieren.</span><span class="sxs-lookup"><span data-stu-id="58dc3-121">With the AzureRM to Az migration toolkit, you can generate a plan to determine what changes will be performed on your scripts before making any modifications to them and before installing the Az PowerShell module.</span></span>

<span data-ttu-id="58dc3-122">In der Schnellstartanleitung [Automatisches Migrieren von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul](quickstart-migrate-azurerm-to-az-automatically.md) werden die einzelnen Schritte für die automatische Aktualisierung Ihrer PowerShell-Skripts von AzureRM auf das Az PowerShell-Modul beschrieben.</span><span class="sxs-lookup"><span data-stu-id="58dc3-122">The [Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module](quickstart-migrate-azurerm-to-az-automatically.md) quickstart walks you through the entire process of automatically updating your PowerShell scripts from AzureRM to the Az PowerShell module.</span></span>

## <a name="next-steps"></a><span data-ttu-id="58dc3-123">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="58dc3-123">Next steps</span></span>

<span data-ttu-id="58dc3-124">[Installieren von Azure PowerShell](install-az-ps.md)
[Deinstallieren von AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="58dc3-124">[Install Azure PowerShell](install-az-ps.md)
[Uninstall AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span></span>
