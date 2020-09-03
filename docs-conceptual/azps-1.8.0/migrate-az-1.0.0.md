---
title: Alle Änderungen von AzureRM zum Azure PowerShell Az-Modul 1.0.0
description: Dieser Migrationsleitfaden enthält eine Liste mit grundlegenden Änderungen, die in Az-Version 1 an Azure PowerShell vorgenommen wurden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 5aad9264cf5ea19d17601a7217285ec30b6d93ac
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241149"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="0b40d-103">Grundlegende Änderungen für Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0b40d-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="0b40d-104">Dieses Dokument enthält ausführliche Informationen zu den Änderungen zwischen AzureRM 6.x und dem neuen Az-Modul, Version 1.x und höher.</span><span class="sxs-lookup"><span data-stu-id="0b40d-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="0b40d-105">Das Inhaltsverzeichnis führt Sie durch einen vollständigen Migrationspfad, einschließlich modulspezifischer Änderungen, die sich auf Ihre Skripte auswirken können.</span><span class="sxs-lookup"><span data-stu-id="0b40d-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="0b40d-106">Allgemeine Hinweise zu den ersten Schritten bei einer Migration von AzureRM zum Az-Modul finden Sie unter [Starten der Migration von AzureRM zu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="0b40d-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="0b40d-107">Inhaltsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="0b40d-107">Table of Contents</span></span>

- [<span data-ttu-id="0b40d-108">Allgemeine grundlegende Änderungen</span><span class="sxs-lookup"><span data-stu-id="0b40d-108">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="0b40d-109">Änderungen von Cmdlet-Nomen</span><span class="sxs-lookup"><span data-stu-id="0b40d-109">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="0b40d-110">Änderungen von Modulnamen</span><span class="sxs-lookup"><span data-stu-id="0b40d-110">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="0b40d-111">Entfernte Module</span><span class="sxs-lookup"><span data-stu-id="0b40d-111">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="0b40d-112">Windows PowerShell 5.1 und .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="0b40d-112">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="0b40d-113">Vorübergehende Entfernung der Benutzeranmeldung per PSCredential</span><span class="sxs-lookup"><span data-stu-id="0b40d-113">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="0b40d-114">Anmeldung per Standardgerätecode anstelle einer Webbrowser-Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="0b40d-114">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="0b40d-115">Grundlegende Änderungen am Modul</span><span class="sxs-lookup"><span data-stu-id="0b40d-115">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="0b40d-116">Az.ApiManagement (bisher AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="0b40d-116">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="0b40d-117">Az.Billing (bisher AzureRM.Billing, AzureRM.Consumption und AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="0b40d-117">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="0b40d-118">Az.CognitiveServices (bisher AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="0b40d-118">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="0b40d-119">Az.Compute (bisher AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="0b40d-119">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="0b40d-120">Az.DataFactory (bisher AzureRM.DataFactories und AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="0b40d-120">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="0b40d-121">Az.DataLakeAnalytics (bisher AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="0b40d-121">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="0b40d-122">Az.DataLakeStore (bisher AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="0b40d-122">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="0b40d-123">Az.KeyVault (bisher AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="0b40d-123">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="0b40d-124">Az.Media (bisher AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="0b40d-124">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="0b40d-125">Az.Monitor (bisher AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="0b40d-125">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="0b40d-126">Az.Network (bisher AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="0b40d-126">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="0b40d-127">Az.OperationalInsights (bisher AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="0b40d-127">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="0b40d-128">Az.RecoveryServices (bisher AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup und AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="0b40d-128">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="0b40d-129">Az.Resources (bisher AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="0b40d-129">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="0b40d-130">Az.ServiceFabric (bisher AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="0b40d-130">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="0b40d-131">Az.Sql (bisher AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="0b40d-131">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="0b40d-132">Az.Storage (bisher Azure.Storage und AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="0b40d-132">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="0b40d-133">Az.Websites (bisher AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="0b40d-133">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="0b40d-134">Allgemeine grundlegende Änderungen</span><span class="sxs-lookup"><span data-stu-id="0b40d-134">General breaking changes</span></span>

<span data-ttu-id="0b40d-135">In diesem Abschnitt werden die allgemeinen grundlegenden Änderungen beschrieben, die Teil des neuen Entwurfs des Az-Moduls sind.</span><span class="sxs-lookup"><span data-stu-id="0b40d-135">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="0b40d-136">Änderungen von Cmdlet-Nomen</span><span class="sxs-lookup"><span data-stu-id="0b40d-136">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="0b40d-137">Im AzureRM-Modul verwenden Cmdlets entweder `AzureRM` oder `Azure` als Nomenpräfix.</span><span class="sxs-lookup"><span data-stu-id="0b40d-137">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="0b40d-138">Az vereinfacht und normalisiert Cmdlet-Namen, sodass alle Cmdlets „Az“ als Nomenpräfix verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b40d-138">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="0b40d-139">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0b40d-139">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="0b40d-140">Geändert in:</span><span class="sxs-lookup"><span data-stu-id="0b40d-140">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="0b40d-141">Um die Umstellung auf diese neuen Cmdlet-Namen zu vereinfachen, werden mit Az die beiden neuen Cmdlets [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) und [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-141">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="0b40d-142">`Enable-AzureRmAlias` erstellt Aliase für die älteren Cmdlet-Namen in AzureRM, die den neueren Az-Cmdlet-Namen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0b40d-142">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="0b40d-143">Indem Sie das Argument `-Scope` mit `Enable-AzureRmAlias` verwenden, können Sie auswählen, wo Aliase aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="0b40d-143">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="0b40d-144">Ein Beispiel hierfür ist das folgende Skript in AzureRM:</span><span class="sxs-lookup"><span data-stu-id="0b40d-144">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="0b40d-145">Es kann mit `Enable-AzureRmAlias` mit minimalen Änderungen ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="0b40d-145">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="0b40d-146">Durch das Ausführen von `Enable-AzureRmAlias -Scope CurrentUser` werden die Aliase für alle von Ihnen geöffneten PowerShell-Sitzungen aktiviert. Nach der Ausführung dieses Cmdlets sind für ein Skript dieser Art keinerlei Änderungen erforderlich:</span><span class="sxs-lookup"><span data-stu-id="0b40d-146">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="0b40d-147">Ausführliche Informationen zur Nutzung der Alias-Cmdlets finden Sie in der [Enable-AzureRmAlias-Referenz](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="0b40d-147">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="0b40d-148">Wenn Sie bereit sind, Aliase zu deaktivieren, entfernt `Disable-AzureRmAlias` die erstellten Aliase.</span><span class="sxs-lookup"><span data-stu-id="0b40d-148">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="0b40d-149">Ausführliche Informationen finden Sie in der [Disable-AzureRmAlias-Referenz](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="0b40d-149">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b40d-150">Wenn Sie Aliase deaktivieren, stellen Sie sicher, dass sie für _alle_ Bereiche deaktiviert sind, in denen Aliase aktiviert waren.</span><span class="sxs-lookup"><span data-stu-id="0b40d-150">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="0b40d-151">Änderungen von Modulnamen</span><span class="sxs-lookup"><span data-stu-id="0b40d-151">Module Name Changes</span></span>

<span data-ttu-id="0b40d-152">Die Modulnamen wurden von `AzureRM.*` in `Az.*` geändert, mit Ausnahme der folgenden Module:</span><span class="sxs-lookup"><span data-stu-id="0b40d-152">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="0b40d-153">AzureRM-Modul</span><span class="sxs-lookup"><span data-stu-id="0b40d-153">AzureRM module</span></span> | <span data-ttu-id="0b40d-154">Az-Modul</span><span class="sxs-lookup"><span data-stu-id="0b40d-154">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="0b40d-155">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0b40d-155">Azure.Storage</span></span> | <span data-ttu-id="0b40d-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b40d-156">Az.Storage</span></span> |
| <span data-ttu-id="0b40d-157">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0b40d-157">Azure.AnalysisServices</span></span> | <span data-ttu-id="0b40d-158">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0b40d-158">Az.AnalysisServices</span></span> |
| <span data-ttu-id="0b40d-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0b40d-159">AzureRM.Profile</span></span> | <span data-ttu-id="0b40d-160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b40d-160">Az.Accounts</span></span> |
| <span data-ttu-id="0b40d-161">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="0b40d-161">AzureRM.Insights</span></span> | <span data-ttu-id="0b40d-162">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b40d-162">Az.Monitor</span></span> |
| <span data-ttu-id="0b40d-163">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="0b40d-163">AzureRM.DataFactories</span></span> | <span data-ttu-id="0b40d-164">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b40d-164">Az.DataFactory</span></span> |
| <span data-ttu-id="0b40d-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0b40d-165">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="0b40d-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b40d-166">Az.DataFactory</span></span> |
| <span data-ttu-id="0b40d-167">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0b40d-167">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="0b40d-168">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b40d-168">Az.RecoveryServices</span></span> |
| <span data-ttu-id="0b40d-169">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0b40d-169">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="0b40d-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b40d-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="0b40d-171">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="0b40d-171">AzureRM.Tags</span></span> | <span data-ttu-id="0b40d-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b40d-172">Az.Resources</span></span> |
| <span data-ttu-id="0b40d-173">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="0b40d-173">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="0b40d-174">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0b40d-174">Az.MachineLearning</span></span> |
| <span data-ttu-id="0b40d-175">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="0b40d-175">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="0b40d-176">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0b40d-176">Az.Billing</span></span> |
| <span data-ttu-id="0b40d-177">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="0b40d-177">AzureRM.Consumption</span></span> | <span data-ttu-id="0b40d-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0b40d-178">Az.Billing</span></span> |

<span data-ttu-id="0b40d-179">Die Änderungen der Modulnamen bedeuten, dass alle Skripts, die `#Requires` oder `Import-Module` zum Laden von bestimmten Modulen nutzen, auf die Verwendung des neuen Moduls umgestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0b40d-179">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="0b40d-180">Für Module, bei denen sich das Cmdlet-Suffix nicht geändert hat, bedeutet dies, dass sich das Suffix, das den Operationsbereich angibt, _nicht_ geändert hat, obwohl der Modulname geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0b40d-180">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="0b40d-181">Migrieren von #Requires- und Import-Module-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="0b40d-181">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="0b40d-182">Skripts, für die `#Requires` oder `Import-Module` zum Deklarieren einer Abhängigkeit von AzureRM-Modulen verwendet wird, müssen aktualisiert werden, damit die neuen Modulnamen genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="0b40d-182">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="0b40d-183">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0b40d-183">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="0b40d-184">Änderung erforderlich in:</span><span class="sxs-lookup"><span data-stu-id="0b40d-184">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="0b40d-185">Für `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="0b40d-185">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="0b40d-186">Änderung erforderlich in:</span><span class="sxs-lookup"><span data-stu-id="0b40d-186">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="0b40d-187">Migrieren von vollqualifizierten Cmdlet-Aufrufen</span><span class="sxs-lookup"><span data-stu-id="0b40d-187">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="0b40d-188">Bei Verwendung von Skripts, für die Cmdlet-Aufrufe mit Modulqualifikation verwendet werden, z. B.:</span><span class="sxs-lookup"><span data-stu-id="0b40d-188">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="0b40d-189">Diese müssen geändert werden, damit die neuen Modul- und Cmdlet-Namen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="0b40d-189">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="0b40d-190">Migrieren von Modulmanifestabhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="0b40d-190">Migrating module manifest dependencies</span></span>

<span data-ttu-id="0b40d-191">Für Module, die Abhängigkeiten von AzureRM-Modulen anhand einer Modulmanifestdatei (.psd1) ausdrücken, müssen die Modulnamen jeweils im Abschnitt `RequiredModules` aktualisiert werden:</span><span class="sxs-lookup"><span data-stu-id="0b40d-191">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="0b40d-192">Änderung erforderlich in:</span><span class="sxs-lookup"><span data-stu-id="0b40d-192">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="0b40d-193">Entfernte Module</span><span class="sxs-lookup"><span data-stu-id="0b40d-193">Removed modules</span></span>

<span data-ttu-id="0b40d-194">Folgende Module wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="0b40d-194">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="0b40d-195">Die Tools für diese Dienste werden nicht mehr aktiv unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-195">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="0b40d-196">Kunden wird die zeitnahe Umstellung auf alternative Dienste empfohlen.</span><span class="sxs-lookup"><span data-stu-id="0b40d-196">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="0b40d-197">Windows PowerShell 5.1 und .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="0b40d-197">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="0b40d-198">Für die Verwendung von Az mit PowerShell 5.1 für Windows ist die Installation von .NET Framework 4.7.2 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0b40d-198">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="0b40d-199">Die Verwendung von PowerShell Core 6.x oder höher erfordert kein .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="0b40d-199">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="0b40d-200">Vorübergehende Entfernung der Benutzeranmeldung per PSCredential</span><span class="sxs-lookup"><span data-stu-id="0b40d-200">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="0b40d-201">Aufgrund von Änderungen am Authentifizierungsablauf für .NET Standard entfernen wir die Benutzeranmeldung per PSCredential vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="0b40d-201">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="0b40d-202">Diese Funktion wird mit dem PowerShell 5.1-Release für Windows vom 15.01.2019 wieder eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-202">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="0b40d-203">Eine ausführliche Beschreibung finden Sie unter [diesem GitHub-Problem](https://github.com/Azure/azure-powershell/issues/7430).</span><span class="sxs-lookup"><span data-stu-id="0b40d-203">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="0b40d-204">Anmeldung per Standardgerätecode anstelle einer Webbrowser-Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="0b40d-204">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="0b40d-205">Aufgrund von Änderungen am Authentifizierungsablauf für .NET Standard nutzen wir die Geräteanmeldung während der interaktiven Anmeldung als Standardanmeldungsablauf.</span><span class="sxs-lookup"><span data-stu-id="0b40d-205">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="0b40d-206">Die Anmeldung per Webbrowser wird im PowerShell 5.1-Release für Windows vom 15.01.2019 wieder als Standard eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-206">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="0b40d-207">Benutzer können dann die Geräteanmeldung mit einem Switch-Parameter wählen.</span><span class="sxs-lookup"><span data-stu-id="0b40d-207">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="0b40d-208">Grundlegende Änderungen am Modul</span><span class="sxs-lookup"><span data-stu-id="0b40d-208">Module breaking changes</span></span>

<span data-ttu-id="0b40d-209">In diesem Abschnitt werden bestimmte wichtige Änderungen für einzelne Module und Cmdlets beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0b40d-209">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="0b40d-210">Az.ApiManagement (bisher AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="0b40d-210">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="0b40d-211">Folgende Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="0b40d-211">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="0b40d-212">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b40d-212">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="0b40d-213">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="0b40d-213">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="0b40d-214">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="0b40d-214">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="0b40d-215">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="0b40d-215">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="0b40d-216">Verwenden Sie stattdessen das Cmdlet **Set-AzApiManagement**, um diese Eigenschaften festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0b40d-216">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="0b40d-217">Die folgenden Eigenschaften wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="0b40d-217">Removed the following properties:</span></span>
  - <span data-ttu-id="0b40d-218">Die Eigenschaften `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` und `ScmHostnameConfiguration` vom Typ `PsApiManagementHostnameConfiguration` wurden aus `PsApiManagementContext` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-218">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="0b40d-219">Verwenden Sie stattdessen `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` und `ScmCustomHostnameConfiguration` vom Typ `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0b40d-219">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="0b40d-220">Die `StaticIPs`-Eigenschaft wurde aus PsApiManagementContext entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-220">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="0b40d-221">Die Eigenschaft wurde in `PublicIPAddresses` und `PrivateIPAddresses` unterteilt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-221">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="0b40d-222">Die erforderliche `Location`-Eigenschaft wurde aus dem Cmdlet New-AzureApiManagementVirtualNetwork entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-222">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="0b40d-223">Az.Billing (bisher AzureRM.Billing, AzureRM.Consumption und AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="0b40d-223">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="0b40d-224">Der Parameter `InvoiceName` wurde aus dem Cmdlet `Get-AzConsumptionUsageDetail` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-224">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="0b40d-225">Für Skripts müssen andere Identitätsparameter für die Rechnung genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="0b40d-225">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="0b40d-226">Az.CognitiveServices (bisher AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="0b40d-226">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="0b40d-227">Der Parametersatz `GetSkusWithAccountParamSetName` wurde aus dem Cmdlet `Get-AzCognitiveServicesAccountSkus` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-227">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="0b40d-228">Sie müssen SKUs nach Kontotyp und Standort abrufen, anstatt ResourceGroupName und den Kontonamen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b40d-228">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="0b40d-229">Az.Compute (bisher AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="0b40d-229">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="0b40d-230">`IdentityIds` wurden aus der `Identity`-Eigenschaft in den Objekten `PSVirtualMachine` und `PSVirtualMachineScaleSet` entfernt. In Skripts sollte der Wert dieses Felds nicht mehr verwendet werden, um Verarbeitungsentscheidungen zu treffen.</span><span class="sxs-lookup"><span data-stu-id="0b40d-230">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="0b40d-231">Der Typ der `InstanceView`-Eigenschaft des `PSVirtualMachineScaleSetVM`-Objekts wurde von `VirtualMachineInstanceView` in `VirtualMachineScaleSetVMInstanceView` geändert.</span><span class="sxs-lookup"><span data-stu-id="0b40d-231">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="0b40d-232">Die Eigenschaften `AutoOSUpgradePolicy` und `AutomaticOSUpgrade` wurden aus der `UpgradePolicy`-Eigenschaft entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-232">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="0b40d-233">Der Typ der `Sku`-Eigenschaft im `PSSnapshotUpdate`-Objekt wurde von `DiskSku` in `SnapshotSku` geändert.</span><span class="sxs-lookup"><span data-stu-id="0b40d-233">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="0b40d-234">`VmScaleSetVMParameterSet` wurde aus dem Cmdlet `Add-AzVMDataDisk` entfernt. Sie können einer ScaleSet-VM nicht mehr einzeln einen Datenträger hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0b40d-234">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="0b40d-235">Az.DataFactory (bisher AzureRM.DataFactories und AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="0b40d-235">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="0b40d-236">Der Parameter `GatewayName` ist im Cmdlet `New-AzDataFactoryEncryptValue` jetzt obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="0b40d-236">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="0b40d-237">Das Cmdlet `New-AzDataFactoryGatewayKey` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-237">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="0b40d-238">Der Parameter `LinkedServiceName` wurde aus dem Cmdlet `Get-AzDataFactoryV2ActivityRun` entfernt. In Skripts sollte der Wert dieses Felds nicht mehr verwendet werden, um Verarbeitungsentscheidungen zu treffen.</span><span class="sxs-lookup"><span data-stu-id="0b40d-238">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="0b40d-239">Az.DataLakeAnalytics (bisher AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="0b40d-239">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="0b40d-240">Veraltete Cmdlets wurden entfernt: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` und `Set-AzDataLakeAnalyticsCatalogSecret`.</span><span class="sxs-lookup"><span data-stu-id="0b40d-240">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="0b40d-241">Az.DataLakeStore (bisher AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="0b40d-241">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="0b40d-242">Für die folgenden Cmdlets wurde der Typ des Parameters `Encoding` von `FileSystemCmdletProviderEncoding` in `System.Text.Encoding` geändert.</span><span class="sxs-lookup"><span data-stu-id="0b40d-242">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="0b40d-243">Bei dieser Änderung wurden die Codierungswerte `String` und `Oem` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-243">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="0b40d-244">Alle anderen bisherigen Codierungswerte bleiben erhalten.</span><span class="sxs-lookup"><span data-stu-id="0b40d-244">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="0b40d-245">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0b40d-245">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="0b40d-246">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="0b40d-246">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="0b40d-247">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="0b40d-247">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="0b40d-248">Der veraltete Eigenschaftenalias `Tags` wurde aus den Cmdlets `New-AzDataLakeStoreAccount` und `Set-AzDataLakeStoreAccount` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-248">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="0b40d-249">Skripts mit Verwendung von:</span><span class="sxs-lookup"><span data-stu-id="0b40d-249">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="0b40d-250">Änderung erforderlich in:</span><span class="sxs-lookup"><span data-stu-id="0b40d-250">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="0b40d-251">Die veralteten Eigenschaften `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier` und `FirewallAllowAzureIps` wurden aus dem `PSDataLakeStoreAccountBasic`-Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-251">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="0b40d-252">Alle Skripts, für die das von `Get-AzDataLakeStoreAccount` zurückgegebene `PSDatalakeStoreAccount`-Objekt verwendet wird, sollten nicht auf diese Eigenschaften verweisen.</span><span class="sxs-lookup"><span data-stu-id="0b40d-252">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="0b40d-253">Az.KeyVault (bisher AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="0b40d-253">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="0b40d-254">Die `PurgeDisabled`-Eigenschaft wurde aus den Objekten `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` und `PSKeyVaultSecretAttributes` entfernt. In Skripts sollte nicht mehr auf die ```PurgeDisabled```-Eigenschaft verwiesen werden, um Verarbeitungsentscheidungen zu treffen.</span><span class="sxs-lookup"><span data-stu-id="0b40d-254">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="0b40d-255">Az.Media (bisher AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="0b40d-255">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="0b40d-256">Der veraltete Eigenschaftenalias `Tags` wurde aus dem Cmdlet `New-AzMediaService` entfernt. Skripts mit Verwendung von:</span><span class="sxs-lookup"><span data-stu-id="0b40d-256">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="0b40d-257">Änderung erforderlich in:</span><span class="sxs-lookup"><span data-stu-id="0b40d-257">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="0b40d-258">Az.Monitor (bisher AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="0b40d-258">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="0b40d-259">Die Plural-Parameternamen `Categories` und `Timegrains` wurden in Singular-Parameternamen aus dem Cmdlet `Set-AzDiagnosticSetting` geändert. Skripts mit Verwendung von:</span><span class="sxs-lookup"><span data-stu-id="0b40d-259">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="0b40d-260">Änderung erforderlich in:</span><span class="sxs-lookup"><span data-stu-id="0b40d-260">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="0b40d-261">Az.Network (bisher AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="0b40d-261">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="0b40d-262">Der veraltete Parameter `ResourceId` wurde aus dem Cmdlet `Get-AzServiceEndpointPolicyDefinition` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-262">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="0b40d-263">Die verwaltete `EnableVmProtection`-Eigenschaft wurde aus dem `PSVirtualNetwork`-Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-263">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="0b40d-264">Das veraltete Cmdlet `Set-AzVirtualNetworkGatewayVpnClientConfig` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-264">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="0b40d-265">Für Skripts sollten basierend auf den Werten dieser Felder keine Verarbeitungsentscheidungen mehr getroffen werden.</span><span class="sxs-lookup"><span data-stu-id="0b40d-265">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="0b40d-266">Az.OperationalInsights (bisher AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="0b40d-266">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="0b40d-267">Der Standardparametersatz für `Get-AzOperationalInsightsDataSource` wurde entfernt, und `ByWorkspaceNameByKind` ist zum Standardparametersatz geworden.</span><span class="sxs-lookup"><span data-stu-id="0b40d-267">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="0b40d-268">Skripts mit Auflistung von Datenquellen mit:</span><span class="sxs-lookup"><span data-stu-id="0b40d-268">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="0b40d-269">Änderung mit Angabe der Art erforderlich:</span><span class="sxs-lookup"><span data-stu-id="0b40d-269">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="0b40d-270">Az.RecoveryServices (bisher AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup und AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="0b40d-270">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="0b40d-271">Der Parameter `Encryption` wurde aus dem Cmdlet `New/Set-AzRecoveryServicesAsrPolicy` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-271">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="0b40d-272">Der Parameter `TargetStorageAccountName` ist für Wiederherstellungen von verwalteten Datenträgern im Cmdlet `Restore-AzRecoveryServicesBackupItem` jetzt obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="0b40d-272">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="0b40d-273">Die Parameter `StorageAccountName` und `StorageAccountResourceGroupName` im Cmdlet `Restore-AzRecoveryServicesBackupItem` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-273">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="0b40d-274">Der Parameter `Name` im Cmdlet `Get-AzRecoveryServicesBackupContainer` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-274">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="0b40d-275">Az.Resources (bisher AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="0b40d-275">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="0b40d-276">Der Parameter `Sku` wurde aus dem Cmdlet `New/Set-AzPolicyAssignment` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-276">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="0b40d-277">Der Parameter `Password` wurde aus den Cmdlets `New-AzADServicePrincipal` und `New-AzADSpCredential` entfernt. Die Kennwörter werden automatisch generiert. Bei Verwendung von Skripts mit Bereitstellung des Kennworts:</span><span class="sxs-lookup"><span data-stu-id="0b40d-277">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="0b40d-278">Änderung erforderlich, damit das Kennwort aus der Ausgabe verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="0b40d-278">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="0b40d-279">Az.ServiceFabric (bisher AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="0b40d-279">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="0b40d-280">Die folgenden Cmdlet-Rückgabetypen wurden geändert:</span><span class="sxs-lookup"><span data-stu-id="0b40d-280">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="0b40d-281">Die `ServiceTypeHealthPolicies`-Eigenschaft vom Typ `ApplicationHealthPolicy` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-281">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="0b40d-282">Die `ApplicationHealthPolicies`-Eigenschaft vom Typ `ClusterUpgradeDeltaHealthPolicy` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-282">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="0b40d-283">Die `OverrideUserUpgradePolicy`-Eigenschaft vom Typ `ClusterUpgradePolicy` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-283">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="0b40d-284">Diese Änderungen wirken sich auf die folgenden Cmdlets aus:</span><span class="sxs-lookup"><span data-stu-id="0b40d-284">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="0b40d-285">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0b40d-285">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="0b40d-286">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0b40d-286">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="0b40d-287">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0b40d-287">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="0b40d-288">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="0b40d-288">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="0b40d-289">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="0b40d-289">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="0b40d-290">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0b40d-290">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="0b40d-291">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0b40d-291">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="0b40d-292">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0b40d-292">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="0b40d-293">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="0b40d-293">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="0b40d-294">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="0b40d-294">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="0b40d-295">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="0b40d-295">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="0b40d-296">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="0b40d-296">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="0b40d-297">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="0b40d-297">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="0b40d-298">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="0b40d-298">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="0b40d-299">Az.Sql (bisher AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="0b40d-299">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="0b40d-300">Die Parameter `State` und `ResourceId` wurden aus dem Cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-300">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="0b40d-301">Veraltete Cmdlets wurden entfernt: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing` und `Remove-AzSqlServerAuditing`.</span><span class="sxs-lookup"><span data-stu-id="0b40d-301">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="0b40d-302">Der veraltete Parameter `Current` wurde aus dem Cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-302">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="0b40d-303">Der veraltete Parameter `DatabaseName` wurde aus dem Cmdlet `Get-AzSqlServerServiceObjective` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-303">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="0b40d-304">Der veraltete Parameter `PrivilegedLogin` wurde aus dem Cmdlet `Set-AzSqlDatabaseDataMaskingPolicy` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-304">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="0b40d-305">Az.Storage (bisher Azure.Storage und AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="0b40d-305">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="0b40d-306">Der Standardparametersatz wurde in `OAuthParameterSet` geändert, um die Erstellung eines OAuth-Speicherkontexts nur mit dem Speicherkontonamen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0b40d-306">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="0b40d-307">Beispiel: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="0b40d-307">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="0b40d-308">Der Parameter `Location` ist im Cmdlet `Get-AzStorageUsage` jetzt obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="0b40d-308">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="0b40d-309">Für die Methoden der Storage-API wird jetzt anstelle von synchronen API-Aufrufen das aufgabenbasierte asynchrone Muster (Task-based Asynchronous Pattern, TAP) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b40d-309">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="0b40d-310">Die folgenden Beispiele veranschaulichen die neuen asynchronen Befehle:</span><span class="sxs-lookup"><span data-stu-id="0b40d-310">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="0b40d-311">Momentaufnahme eines Blobs erstellen</span><span class="sxs-lookup"><span data-stu-id="0b40d-311">Blob Snapshot</span></span>

<span data-ttu-id="0b40d-312">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="0b40d-312">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="0b40d-313">Az:</span><span class="sxs-lookup"><span data-stu-id="0b40d-313">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="0b40d-314">Momentaufnahme freigeben</span><span class="sxs-lookup"><span data-stu-id="0b40d-314">Share Snapshot</span></span>

<span data-ttu-id="0b40d-315">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="0b40d-315">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="0b40d-316">Az:</span><span class="sxs-lookup"><span data-stu-id="0b40d-316">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="0b40d-317">Vorläufig gelöschten Blob wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="0b40d-317">Undelete soft-deleted blob</span></span>

<span data-ttu-id="0b40d-318">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="0b40d-318">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="0b40d-319">Az:</span><span class="sxs-lookup"><span data-stu-id="0b40d-319">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="0b40d-320">Blobtarif festlegen</span><span class="sxs-lookup"><span data-stu-id="0b40d-320">Set Blob Tier</span></span>

<span data-ttu-id="0b40d-321">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="0b40d-321">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="0b40d-322">Az:</span><span class="sxs-lookup"><span data-stu-id="0b40d-322">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="0b40d-323">Az.Websites (bisher AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="0b40d-323">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="0b40d-324">Die veralteten Eigenschaften wurden aus den Objekten `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` und `PSSite` entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b40d-324">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
