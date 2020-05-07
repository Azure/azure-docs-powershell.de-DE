---
title: Grundlegende Änderungen für Microsoft Azure PowerShell 6.0.0
description: Dieser Migrationsleitfaden enthält eine Liste mit grundlegenden Änderungen, die in Version 6 an Azure PowerShell vorgenommen wurden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 1fbd24996da2fbc7d4e95c2a63f828aea6cb3145
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534923"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a><span data-ttu-id="617a0-103">Grundlegende Änderungen für Microsoft Azure PowerShell 6.0.0</span><span class="sxs-lookup"><span data-stu-id="617a0-103">Breaking changes for Microsoft Azure PowerShell 6.0.0</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="617a0-104">Dieses Dokument informiert über grundlegende Änderungen und fungiert als Migrationsleitfaden für Kunden mit Microsoft Azure PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="617a0-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="617a0-105">In den einzelnen Abschnitten werden jeweils der Grund für die grundlegende Änderung und der Migrationspfad des geringsten Widerstands beschrieben.</span><span class="sxs-lookup"><span data-stu-id="617a0-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="617a0-106">Ausführlichen Kontext finden Sie unter der Pull-Anforderung für die jeweilige Änderung.</span><span class="sxs-lookup"><span data-stu-id="617a0-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="617a0-107">Inhaltsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="617a0-107">Table of Contents</span></span>

- [<span data-ttu-id="617a0-108">Allgemeine grundlegende Änderungen</span><span class="sxs-lookup"><span data-stu-id="617a0-108">General breaking changes</span></span>](#general-breaking-changes)
    - [<span data-ttu-id="617a0-109">Festlegung der erforderlichen PowerShell-Mindestversion auf 5.0</span><span class="sxs-lookup"><span data-stu-id="617a0-109">Minimum PowerShell version required bumped to 5.0</span></span>](#minimum-powershell-version-required-bumped-to-50)
    - [<span data-ttu-id="617a0-110">Standardmäßige Aktivierung der automatischen Kontextspeicherung</span><span class="sxs-lookup"><span data-stu-id="617a0-110">Context autosaved enabled by default</span></span>](#context-autosave-enabled-by-default)
    - [<span data-ttu-id="617a0-111">Entfernung des Tags-Alias</span><span class="sxs-lookup"><span data-stu-id="617a0-111">Removal of Tags alias</span></span>](#removal-of-tags-alias)
- [<span data-ttu-id="617a0-112">Grundlegende Änderungen an AzureRM.Compute-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-112">Breaking changes to AzureRM.Compute cmdlets</span></span>](#breaking-changes-to-azurermcompute-cmdlets)
- [<span data-ttu-id="617a0-113">Grundlegende Änderungen an AzureRM.DataLakeStore-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-113">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [<span data-ttu-id="617a0-114">Grundlegende Änderungen an AzureRM.Dns-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-114">Breaking changes to AzureRM.Dns cmdlets</span></span>](#breaking-changes-to-azurermdns-cmdlets)
- [<span data-ttu-id="617a0-115">Grundlegende Änderungen an AzureRM.Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-115">Breaking changes to AzureRM.Insights cmdlets</span></span>](#breaking-changes-to-azurerminsights-cmdlets)
- [<span data-ttu-id="617a0-116">Grundlegende Änderungen an AzureRM.KeyVault-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-116">Breaking changes to AzureRM.KeyVault cmdlets</span></span>](#breaking-changes-to-azurermkeyvault-cmdlets)
- [<span data-ttu-id="617a0-117">Grundlegende Änderungen an AzureRM.Network-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-117">Breaking changes to AzureRM.Network cmdlets</span></span>](#breaking-changes-to-azurermnetwork-cmdlets)
- [<span data-ttu-id="617a0-118">Grundlegende Änderungen an AzureRM.RedisCache-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-118">Breaking changes to AzureRM.RedisCache cmdlets</span></span>](#breaking-changes-to-azurermrediscache-cmdlets)
- [<span data-ttu-id="617a0-119">Grundlegende Änderungen an AzureRM.Resources-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-119">Breaking changes to AzureRM.Resources cmdlets</span></span>](#breaking-changes-to-azurermresources-cmdlets)
- [<span data-ttu-id="617a0-120">Grundlegende Änderungen an AzureRM.Storage-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-120">Breaking changes to AzureRM.Storage cmdlets</span></span>](#breaking-changes-to-azurermstorage-cmdlets)
- [<span data-ttu-id="617a0-121">Entfernte Module</span><span class="sxs-lookup"><span data-stu-id="617a0-121">Removed modules</span></span>](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a><span data-ttu-id="617a0-122">Allgemeine grundlegende Änderungen</span><span class="sxs-lookup"><span data-stu-id="617a0-122">General breaking changes</span></span>

### <a name="minimum-powershell-version-required-bumped-to-50"></a><span data-ttu-id="617a0-123">Festlegung der erforderlichen PowerShell-Mindestversion auf 5.0</span><span class="sxs-lookup"><span data-stu-id="617a0-123">Minimum PowerShell version required bumped to 5.0</span></span>

<span data-ttu-id="617a0-124">Bisher war _mindestens_ Version 3.0 von PowerShell erforderlich, um Cmdlets ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="617a0-124">Previously, Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.</span></span> <span data-ttu-id="617a0-125">Diese Anforderung wurde auf Version 5.0 von PowerShell erhöht.</span><span class="sxs-lookup"><span data-stu-id="617a0-125">Moving forward, this requirement will be raised to version 5.0 of PowerShell.</span></span> <span data-ttu-id="617a0-126">Informationen zur Durchführung eines Upgrades auf PowerShell 5.0 finden Sie in [dieser Tabelle](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="617a0-126">For information on upgrading to PowerShell 5.0, please see [this table](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

### <a name="context-autosave-enabled-by-default"></a><span data-ttu-id="617a0-127">Standardmäßige Aktivierung der automatischen Kontextspeicherung</span><span class="sxs-lookup"><span data-stu-id="617a0-127">Context autosave enabled by default</span></span>

<span data-ttu-id="617a0-128">Bei der automatischen Kontextspeicherung geht es um die Speicherung von Azure-Anmeldeinformationen, die für neue und unterschiedliche PowerShell-Sitzungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="617a0-128">Context autosave is the storage of Azure sign in information that can be used between new and different PowerShell sessions.</span></span> <span data-ttu-id="617a0-129">Weitere Informationen zur automatischen Kontextspeicherung finden Sie in [diesem Dokument](https://docs.microsoft.com/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="617a0-129">For more information on context autosave, please see [this document](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="617a0-130">Bisher war die automatische Kontextspeicherung standardmäßig deaktiviert. Die Azure-Authentifizierungsinformationen eines Benutzers wurden zwischen Sitzungen erst gespeichert, wenn er das `Enable-AzureRmContextAutosave`-Cmdlet ausgeführt hat, um die Kontextbeibehaltung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="617a0-130">Previously by default, context autosave was disabled, which meant the user's Azure authentication information was not stored between sessions until they ran the `Enable-AzureRmContextAutosave` cmdlet to turn on context persistence.</span></span> <span data-ttu-id="617a0-131">Ab jetzt ist die automatische Kontextspeicherung standardmäßig aktiviert. Dies bedeutet, dass für Benutzer _ohne gespeicherte Einstellungen für die automatische Kontextspeicherung_ der Kontext bei der nächsten Anmeldung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="617a0-131">Moving forward, context autosave will be enabled by default, which means that users _with no saved context autosave settings_ will have their context stored the next time they sign in.</span></span> <span data-ttu-id="617a0-132">Benutzer können sich gegen die Nutzung dieser Funktionalität entscheiden, indem sie das `Disable-AzureRmContextAutosave`-Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="617a0-132">Users can opt out of this functionality by using the `Disable-AzureRmContextAutosave` cmdlet.</span></span>

<span data-ttu-id="617a0-133">_Hinweis_: Benutzer, die die automatische Kontextspeicherung bisher deaktiviert bzw. aktiviert hatten, und vorhandene Kontexte sind von dieser Änderung nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="617a0-133">_Note_: users that previously disabled context autosave or users with context autosave enabled and existing contexts will not be affected by this change</span></span>

### <a name="removal-of-tags-alias"></a><span data-ttu-id="617a0-134">Entfernung des Tags-Alias</span><span class="sxs-lookup"><span data-stu-id="617a0-134">Removal of Tags alias</span></span>

<span data-ttu-id="617a0-135">Der `Tags`-Alias für den Parameter `Tag` wurde für viele Cmdlets entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-135">The alias `Tags` for the `Tag` parameter has been removed across numerous cmdlets.</span></span> <span data-ttu-id="617a0-136">Hier ist eine Liste mit den Modulen (und den dazugehörigen Cmdlets) angegeben, die hiervon betroffen sind:</span><span class="sxs-lookup"><span data-stu-id="617a0-136">Below is a list of modules (and the corresponding cmdlets) affected by this:</span></span>

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a><span data-ttu-id="617a0-137">Grundlegende Änderungen an AzureRM.Compute-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-137">Breaking changes to AzureRM.Compute cmdlets</span></span>

<span data-ttu-id="617a0-138">**Verschiedenes**</span><span class="sxs-lookup"><span data-stu-id="617a0-138">**Miscellaneous**</span></span>
- <span data-ttu-id="617a0-139">Die in den Typen `PSDisk` und `PSSnapshot` geschachtelte SKU-Name-Eigenschaft wurde von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-139">The sku name property nested in types `PSDisk` and `PSSnapshot` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell-interactive
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- <span data-ttu-id="617a0-140">Die in den Typen `PSVirtualMachine`, `PSVirtualMachineScaleSet` und `PSImage` geschachtelte Speicherkontotyp-Eigenschaft wurde von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-140">The storage account type property nested in types `PSVirtualMachine`, `PSVirtualMachineScaleSet` and `PSImage` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell-interactive
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

<span data-ttu-id="617a0-141">**Add-AzureRmImageDataDisk**</span><span class="sxs-lookup"><span data-stu-id="617a0-141">**Add-AzureRmImageDataDisk**</span></span>
- <span data-ttu-id="617a0-142">Die zulässigen Werte für den Parameter `StorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-142">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="617a0-143">**Add-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="617a0-143">**Add-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="617a0-144">Die zulässigen Werte für den Parameter `StorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-144">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="617a0-145">**Add-AzureRmVmssDataDisk**</span><span class="sxs-lookup"><span data-stu-id="617a0-145">**Add-AzureRmVmssDataDisk**</span></span>
- <span data-ttu-id="617a0-146">Die zulässigen Werte für den Parameter `StorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-146">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="617a0-147">**New-AzureRmAvailabilitySet**</span><span class="sxs-lookup"><span data-stu-id="617a0-147">**New-AzureRmAvailabilitySet**</span></span>
- <span data-ttu-id="617a0-148">Der Parameter `Managed` wurde entfernt und durch `Sku` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="617a0-148">The parameter `Managed` was removed in favor of `Sku`</span></span>

```powershell-interactive
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

<span data-ttu-id="617a0-149">**New-AzureRmDiskConfig**</span><span class="sxs-lookup"><span data-stu-id="617a0-149">**New-AzureRmDiskConfig**</span></span>
- <span data-ttu-id="617a0-150">Die zulässigen Werte für den Parameter `SkuName` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-150">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="617a0-151">**New-AzureRmDiskUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="617a0-151">**New-AzureRmDiskUpdateConfig**</span></span>
- <span data-ttu-id="617a0-152">Die zulässigen Werte für den Parameter `SkuName` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-152">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="617a0-153">**New-AzureRmSnapshotConfig**</span><span class="sxs-lookup"><span data-stu-id="617a0-153">**New-AzureRmSnapshotConfig**</span></span>
- <span data-ttu-id="617a0-154">Die zulässigen Werte für den Parameter `SkuName` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-154">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="617a0-155">**New-AzureRmSnapshotUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="617a0-155">**New-AzureRmSnapshotUpdateConfig**</span></span>
- <span data-ttu-id="617a0-156">Die zulässigen Werte für den Parameter `SkuName` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-156">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="617a0-157">**Set-AzureRmImageOsDisk**</span><span class="sxs-lookup"><span data-stu-id="617a0-157">**Set-AzureRmImageOsDisk**</span></span>
- <span data-ttu-id="617a0-158">Die zulässigen Werte für den Parameter `StorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-158">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="617a0-159">**Set-AzureRmVMAEMExtension**</span><span class="sxs-lookup"><span data-stu-id="617a0-159">**Set-AzureRmVMAEMExtension**</span></span>
- <span data-ttu-id="617a0-160">Der Parameter `DisableWAD` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-160">The parameter `DisableWAD` was removed</span></span>
    -  <span data-ttu-id="617a0-161">Die Microsoft Azure-Diagnose ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="617a0-161">Windows Azure Diagnostics is disabled by default</span></span>

<span data-ttu-id="617a0-162">**Set-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="617a0-162">**Set-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="617a0-163">Die zulässigen Werte für den Parameter `StorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-163">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="617a0-164">**Set-AzureRmVMOSDisk**</span><span class="sxs-lookup"><span data-stu-id="617a0-164">**Set-AzureRmVMOSDisk**</span></span>
- <span data-ttu-id="617a0-165">Die zulässigen Werte für den Parameter `StorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-165">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="617a0-166">**Set-AzureRmVmssStorageProfile**</span><span class="sxs-lookup"><span data-stu-id="617a0-166">**Set-AzureRmVmssStorageProfile**</span></span>
- <span data-ttu-id="617a0-167">Die zulässigen Werte für den Parameter `ManagedDisk` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-167">The accepted values for parameter `ManagedDisk` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="617a0-168">**Update-AzureRmVmss**</span><span class="sxs-lookup"><span data-stu-id="617a0-168">**Update-AzureRmVmss**</span></span>
- <span data-ttu-id="617a0-169">Die zulässigen Werte für den Parameter `ManagedDiskStorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-169">The accepted values for parameter `ManagedDiskStorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a><span data-ttu-id="617a0-170">Grundlegende Änderungen an AzureRM.DataLakeStore-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-170">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>

<span data-ttu-id="617a0-171">**Export-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="617a0-171">**Export-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="617a0-172">Die Parameter `PerFileThreadCount` und `ConcurrentFileCount` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-172">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="617a0-173">Verwenden Sie ab jetzt den Parameter `Concurrency`.</span><span class="sxs-lookup"><span data-stu-id="617a0-173">Please use the `Concurrency` parameter moving forward</span></span>

```powershell-interactive
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

<span data-ttu-id="617a0-174">**Import-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="617a0-174">**Import-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="617a0-175">Die Parameter `PerFileThreadCount` und `ConcurrentFileCount` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-175">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="617a0-176">Verwenden Sie ab jetzt den Parameter `Concurrency`.</span><span class="sxs-lookup"><span data-stu-id="617a0-176">Please use the `Concurrency` parameter moving forward</span></span>

```powershell-interactive
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

<span data-ttu-id="617a0-177">**Remove-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="617a0-177">**Remove-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="617a0-178">Der Parameter `Clean` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-178">Parameter `Clean` was removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a><span data-ttu-id="617a0-179">Grundlegende Änderungen an AzureRM.Dns-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-179">Breaking changes to AzureRM.Dns cmdlets</span></span>

<span data-ttu-id="617a0-180">**New-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="617a0-180">**New-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="617a0-181">Der Parameter `Force` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-181">The parameter `Force` was removed</span></span>

<span data-ttu-id="617a0-182">**Remove-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="617a0-182">**Remove-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="617a0-183">Der Parameter `Force` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-183">The parameter `Force` was removed</span></span>

<span data-ttu-id="617a0-184">**Remove-AzureRmDnsZone**</span><span class="sxs-lookup"><span data-stu-id="617a0-184">**Remove-AzureRmDnsZone**</span></span>
- <span data-ttu-id="617a0-185">Der Parameter `Force` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-185">The parameter `Force` was removed</span></span>

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a><span data-ttu-id="617a0-186">Grundlegende Änderungen an AzureRM.Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-186">Breaking changes to AzureRM.Insights cmdlets</span></span>

<span data-ttu-id="617a0-187">**Add-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="617a0-187">**Add-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="617a0-188">Die Parameteraliase `AutoscaleProfiles` und `Notifications` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-188">The parameter aliases `AutoscaleProfiles` and `Notifications` were removed</span></span>

<span data-ttu-id="617a0-189">**Add-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="617a0-189">**Add-AzureRmLogProfile**</span></span>
- <span data-ttu-id="617a0-190">Die Parameteraliase `Categories` und `Locations` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-190">The parameter aliases `Categories` and `Locations` were removed</span></span>

<span data-ttu-id="617a0-191">**Add-AzureRmMetricAlertRule**</span><span class="sxs-lookup"><span data-stu-id="617a0-191">**Add-AzureRmMetricAlertRule**</span></span>
- <span data-ttu-id="617a0-192">Der Parameteralias `Actions` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-192">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="617a0-193">**Add-AzureRmWebtestAlertRule**</span><span class="sxs-lookup"><span data-stu-id="617a0-193">**Add-AzureRmWebtestAlertRule**</span></span>
- <span data-ttu-id="617a0-194">Der Parameteralias `Actions` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-194">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="617a0-195">**Get-AzureRmLog**</span><span class="sxs-lookup"><span data-stu-id="617a0-195">**Get-AzureRmLog**</span></span>
- <span data-ttu-id="617a0-196">Die Parameteraliase `MaxRecords` und `MaxEvents` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-196">The parameter aliases `MaxRecords` and `MaxEvents` were removed</span></span>

<span data-ttu-id="617a0-197">**Get-AzureRmMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="617a0-197">**Get-AzureRmMetricDefinition**</span></span>
- <span data-ttu-id="617a0-198">Der Parameteralias `MetricNames` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-198">The parameter alias `MetricNames` was removed</span></span>

<span data-ttu-id="617a0-199">**New-AzureRmAlertRuleEmail**</span><span class="sxs-lookup"><span data-stu-id="617a0-199">**New-AzureRmAlertRuleEmail**</span></span>
- <span data-ttu-id="617a0-200">Die Parameteraliase `CustomEmails` und `SendToServiceOwners` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-200">The parameter aliases `CustomEmails` and `SendToServiceOwners` were removed</span></span>

<span data-ttu-id="617a0-201">**New-AzureRmAlertRuleWebhook**</span><span class="sxs-lookup"><span data-stu-id="617a0-201">**New-AzureRmAlertRuleWebhook**</span></span>
- <span data-ttu-id="617a0-202">Der Parameteralias `Properties` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-202">The parameter alias `Properties` was removed</span></span>

<span data-ttu-id="617a0-203">**New-AzureRmAutoscaleNotification**</span><span class="sxs-lookup"><span data-stu-id="617a0-203">**New-AzureRmAutoscaleNotification**</span></span>
- <span data-ttu-id="617a0-204">Die Parameteraliase `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` und `Webhooks` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-204">The parameter aliases `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` and `Webhooks` were removed</span></span>

<span data-ttu-id="617a0-205">**New-AzureRmAutoscaleProfile**</span><span class="sxs-lookup"><span data-stu-id="617a0-205">**New-AzureRmAutoscaleProfile**</span></span>
- <span data-ttu-id="617a0-206">Die Parameteraliase `Rules`, `ScheduleDays`, `ScheduleHours` und `ScheduleMinutes` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-206">The parameter aliases `Rules`, `ScheduleDays`, `ScheduleHours` and `ScheduleMinutes` were removed</span></span>

<span data-ttu-id="617a0-207">**New-AzureRmAutoscaleWebhook**</span><span class="sxs-lookup"><span data-stu-id="617a0-207">**New-AzureRmAutoscaleWebhook**</span></span>
- <span data-ttu-id="617a0-208">Der Parameteralias `Properties` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-208">The parameter alias `Properties` was removed</span></span>

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a><span data-ttu-id="617a0-209">Grundlegende Änderungen an AzureRM.KeyVault-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-209">Breaking changes to AzureRM.KeyVault cmdlets</span></span>

<span data-ttu-id="617a0-210">**Add-AzureKeyVaultCertificate**</span><span class="sxs-lookup"><span data-stu-id="617a0-210">**Add-AzureKeyVaultCertificate**</span></span>
- <span data-ttu-id="617a0-211">Der Parameter `CertificatePolicy` ist jetzt obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="617a0-211">The `CertificatePolicy` parameter has become mandatory.</span></span>

<span data-ttu-id="617a0-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span><span class="sxs-lookup"><span data-stu-id="617a0-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span></span>
- <span data-ttu-id="617a0-213">Das Cmdlet akzeptiert keine einzelnen Parameter mehr, aus denen das Zugriffstoken besteht. Stattdessen ersetzt das Cmdlet explizite Tokenparameter, z.B. `Service` oder `Permissions`, durch den generischen Parameter `TemplateUri`, der einem an anderer Stelle definierten Beispielzugriffstoken entspricht (meist über Storage PowerShell-Cmdlets oder per manueller Zusammenstellung gemäß Storage-Dokumentation). Das Cmdlet behält den Parameter `ValidityPeriod` bei.</span><span class="sxs-lookup"><span data-stu-id="617a0-213">The cmdlet no longer accepts individual parameters that compose the access token; instead, the cmdlet replaces explicit token parameters, such as `Service` or `Permissions`, with a generic `TemplateUri` parameter, corresponding to a sample access token defined elsewhere (presumably using Storage PowerShell cmdlets, or composed manually according to the Storage documentation.) The cmdlet retains the `ValidityPeriod` parameter.</span></span>

<span data-ttu-id="617a0-214">Weitere Informationen zum Verfassen von SAS-Token für Azure Storage finden Sie auf den entsprechenden Seiten in der Dokumentation:</span><span class="sxs-lookup"><span data-stu-id="617a0-214">For more information on composing shared access tokens for Azure Storage, please refer to the documentation pages, respectively:</span></span>
- [<span data-ttu-id="617a0-215">Constructing a Service SAS (Erstellen einer Dienstebenen-SAS)</span><span class="sxs-lookup"><span data-stu-id="617a0-215">Constructing a Service SAS</span></span>](https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)
- [<span data-ttu-id="617a0-216">Constructing an Account SAS (Erstellen einer Kontoebenen-SAS)</span><span class="sxs-lookup"><span data-stu-id="617a0-216">Constructing an Account SAS</span></span>](https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)

```powershell-interactive
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

<span data-ttu-id="617a0-217">**Set-AzureKeyVaultCertificateIssuer**</span><span class="sxs-lookup"><span data-stu-id="617a0-217">**Set-AzureKeyVaultCertificateIssuer**</span></span>
- <span data-ttu-id="617a0-218">Der Parameter `IssuerProvider` ist jetzt obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="617a0-218">The `IssuerProvider` parameter has become mandatory.</span></span>

<span data-ttu-id="617a0-219">**Undo-AzureKeyVaultCertificateRemoval**</span><span class="sxs-lookup"><span data-stu-id="617a0-219">**Undo-AzureKeyVaultCertificateRemoval**</span></span>
- <span data-ttu-id="617a0-220">Die Ausgabe dieses Cmdlets wurde von `CertificateBundle` in `PSKeyVaultCertificate` geändert.</span><span class="sxs-lookup"><span data-stu-id="617a0-220">The output of this cmdlet has changed from `CertificateBundle` to `PSKeyVaultCertificate`.</span></span>

<span data-ttu-id="617a0-221">**Undo-AzureRmKeyVaultRemoval**</span><span class="sxs-lookup"><span data-stu-id="617a0-221">**Undo-AzureRmKeyVaultRemoval**</span></span>
- <span data-ttu-id="617a0-222">`ResourceGroupName` wurde aus dem `InputObject`-Parametersatz entfernt und wird stattdessen über die `ResourceId`-Eigenschaft des Parameters `InputObject` abgerufen.</span><span class="sxs-lookup"><span data-stu-id="617a0-222">`ResourceGroupName` has been removed from the `InputObject` parameter set, and is instead obtained from the `InputObject` parameter's `ResourceId` property.</span></span>

<span data-ttu-id="617a0-223">**Set-AzureRmKeyVaultAccessPolicy**</span><span class="sxs-lookup"><span data-stu-id="617a0-223">**Set-AzureRmKeyVaultAccessPolicy**</span></span>
- <span data-ttu-id="617a0-224">Die Berechtigung `all` wurde aus `PermissionsToKeys`, `PermissionsToSecrets` und `PermissionsToCertificates` entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-224">The `all` permission was removed from `PermissionsToKeys`, `PermissionsToSecrets`, and `PermissionsToCertificates`.</span></span>

<span data-ttu-id="617a0-225">**Allgemein**</span><span class="sxs-lookup"><span data-stu-id="617a0-225">**General**</span></span>
- <span data-ttu-id="617a0-226">Die `ValueFromPipelineByPropertyName`-Eigenschaft wurde aus allen Cmdlets entfernt, für die das Piping per `InputObject` aktiviert war.</span><span class="sxs-lookup"><span data-stu-id="617a0-226">The `ValueFromPipelineByPropertyName` property was removed from all cmdlets where piping by `InputObject` was enabled.</span></span>  <span data-ttu-id="617a0-227">Hiervon sind die folgenden Cmdlets betroffen:</span><span class="sxs-lookup"><span data-stu-id="617a0-227">The cmdlets affected are:</span></span>
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="617a0-228">`ConfirmImpact`-Ebenen wurden aus allen Cmdlets entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-228">`ConfirmImpact` levels were removed from all cmdlets.</span></span>  <span data-ttu-id="617a0-229">Hiervon sind die folgenden Cmdlets betroffen:</span><span class="sxs-lookup"><span data-stu-id="617a0-229">The cmdlets affected are:</span></span>
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="617a0-230">Das `IKeyVaultDataServiceClient`-Element wurde aktualisiert, damit für alle Zertifikatvorgänge PSTypes anstelle von SDK-Typen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="617a0-230">The `IKeyVaultDataServiceClient` was updated so all Certificate operations return PSTypes instead of SDK types.</span></span> <span data-ttu-id="617a0-231">Dies schließt Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="617a0-231">This includes:</span></span>
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a><span data-ttu-id="617a0-232">Grundlegende Änderungen an AzureRM.Network-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-232">Breaking changes to AzureRM.Network cmdlets</span></span>


<span data-ttu-id="617a0-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="617a0-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="617a0-234">Der Parameter `ProbeEnabled` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-234">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="617a0-235">**Add-AzureRmVirtualNetworkPeering**</span><span class="sxs-lookup"><span data-stu-id="617a0-235">**Add-AzureRmVirtualNetworkPeering**</span></span>
- <span data-ttu-id="617a0-236">Der Parameteralias `AlloowGatewayTransit` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-236">The parameter alias `AlloowGatewayTransit` was removed</span></span>

<span data-ttu-id="617a0-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="617a0-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="617a0-238">Der Parameter `ProbeEnabled` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-238">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="617a0-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="617a0-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="617a0-240">Der Parameter `ProbeEnabled` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-240">The parameter `ProbeEnabled` was removed</span></span>

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a><span data-ttu-id="617a0-241">Grundlegende Änderungen an AzureRM.RedisCache-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-241">Breaking changes to AzureRM.RedisCache cmdlets</span></span>

<span data-ttu-id="617a0-242">**New-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="617a0-242">**New-AzureRmRedisCache**</span></span>
- <span data-ttu-id="617a0-243">Die Parameter `Subnet` und `VirtualNetwork` wurden entfernt und durch `SubnetId` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="617a0-243">The parameters `Subnet` and `VirtualNetwork` were removed in favor of `SubnetId`</span></span>
- <span data-ttu-id="617a0-244">Der Parameter `RedisVersion` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-244">The parameter `RedisVersion` was removed</span></span>
- <span data-ttu-id="617a0-245">Der Parameter `MaxMemoryPolicy` wurde entfernt und durch `RedisConfiguration` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="617a0-245">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell-interactive
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

<span data-ttu-id="617a0-246">**Set-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="617a0-246">**Set-AzureRmRedisCache**</span></span>
- <span data-ttu-id="617a0-247">Der Parameter `MaxMemoryPolicy` wurde entfernt und durch `RedisConfiguration` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="617a0-247">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell-interactive
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a><span data-ttu-id="617a0-248">Grundlegende Änderungen an AzureRM.Resources-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-248">Breaking changes to AzureRM.Resources cmdlets</span></span>

<span data-ttu-id="617a0-249">**Find-AzureRmResource**</span><span class="sxs-lookup"><span data-stu-id="617a0-249">**Find-AzureRmResource**</span></span>
- <span data-ttu-id="617a0-250">Dieses Cmdlet wurde entfernt, und die Funktionalität wurde in `Get-AzureRmResource` verschoben.</span><span class="sxs-lookup"><span data-stu-id="617a0-250">This cmdlet was removed and the functionality was moved into `Get-AzureRmResource`</span></span>

```powershell-interactive
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

<span data-ttu-id="617a0-251">**Find-AzureRmResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="617a0-251">**Find-AzureRmResourceGroup**</span></span>
- <span data-ttu-id="617a0-252">Dieses Cmdlet wurde entfernt, und die Funktionalität wurde in `Get-AzureRmResourceGroup` verschoben.</span><span class="sxs-lookup"><span data-stu-id="617a0-252">This cmdlet was removed and the functionality was moved into `Get-AzureRmResourceGroup`</span></span>

```powershell-interactive
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

<span data-ttu-id="617a0-253">**Get-AzureRmRoleDefinition**</span><span class="sxs-lookup"><span data-stu-id="617a0-253">**Get-AzureRmRoleDefinition**</span></span>
- <span data-ttu-id="617a0-254">Der Parameter `AtScopeAndBelow` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-254">Parameter `AtScopeAndBelow` was removed.</span></span>

```powershell-interactive

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a><span data-ttu-id="617a0-255">Grundlegende Änderungen an AzureRM.Storage-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="617a0-255">Breaking changes to AzureRM.Storage cmdlets</span></span>

<span data-ttu-id="617a0-256">**New-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="617a0-256">**New-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="617a0-257">Der Parameter `EnableEncryptionService` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-257">The parameter `EnableEncryptionService` was removed</span></span>

<span data-ttu-id="617a0-258">**Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="617a0-258">**Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="617a0-259">Die Parameter `EnableEncryptionService` und `DisableEncryptionService` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="617a0-259">The parameters `EnableEncryptionService` and `DisableEncryptionService` were removed</span></span>

## <a name="removed-modules"></a><span data-ttu-id="617a0-260">Entfernte Module</span><span class="sxs-lookup"><span data-stu-id="617a0-260">Removed modules</span></span>

### `AzureRM.ServerManagement`

<span data-ttu-id="617a0-261">Da der Serververwaltungstools-Dienst [letztes Jahr eingestellt](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/) wurde, wurde das entsprechende Modul `AzureRM.ServerManagement` für SMT aus `AzureRM` entfernt und wird nicht mehr ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="617a0-261">The Server Management Tools service was [retired last year](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), and as a result, the corresponding module for SMT, `AzureRM.ServerManagement`, was removed from `AzureRM` and will stop shipping moving forward.</span></span>

### `AzureRM.SiteRecovery`

<span data-ttu-id="617a0-262">Das Modul `AzureRM.SiteRecovery` wird von `AzureRM.RecoveryServices.SiteRecovery` abgelöst. Hierbei handelt es sich um eine funktionale Obermenge des Moduls `AzureRM.SiteRecovery` mit einem neuen Satz gleichwertiger Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="617a0-262">The `AzureRM.SiteRecovery` module is being superseded by `AzureRM.RecoveryServices.SiteRecovery`, which is a functional superset of the `AzureRM.SiteRecovery` module and includes a new set of equivalent cmdlets.</span></span> <span data-ttu-id="617a0-263">Die vollständige Liste mit der Zuordnung alter und neuer Cmdlets finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="617a0-263">The full list of mappings from old to new cmdlets can be found below:</span></span>

| <span data-ttu-id="617a0-264">Veraltetes Cmdlet</span><span class="sxs-lookup"><span data-stu-id="617a0-264">Deprecated cmdlet</span></span>                                        | <span data-ttu-id="617a0-265">Gleichwertiges Cmdlet</span><span class="sxs-lookup"><span data-stu-id="617a0-265">Equivalent cmdlet</span></span>                                                | <span data-ttu-id="617a0-266">Aliase</span><span class="sxs-lookup"><span data-stu-id="617a0-266">Aliases</span></span>                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
