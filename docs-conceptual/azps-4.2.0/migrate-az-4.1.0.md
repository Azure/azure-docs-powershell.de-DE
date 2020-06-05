---
title: Migrationsleitfaden für Az 4.1.0
description: Dieser Migrationsleitfaden enthält eine Liste mit Breaking Changes, die in Az-Version 4.1.0 an Azure PowerShell vorgenommen wurden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.openlocfilehash: e3a4563acf4b0820b61a2ac5da244b26490c8174
ms.sourcegitcommit: cef87acc9f2a0d296bef74f526afd2e067e8146b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/02/2020
ms.locfileid: "84299042"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="a8807-103">Migrationsleitfaden für Az 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a8807-103">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="a8807-104">In diesem Dokument werden die Änderungen beschrieben, die zwischen den Versionen 3.0.0 und 4.1.0 von Az vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="a8807-104">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="a8807-105">Migrationsleitfaden für Az 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a8807-105">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="a8807-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8807-106">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="a8807-107">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a8807-107">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="a8807-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="a8807-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="a8807-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="a8807-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="a8807-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="a8807-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="a8807-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8807-111">Az.Compute</span></span>](#azcompute)
    - [`Remove-AzVmssDiagnosticsExtension`](#remove-azvmssdiagnosticsextension)
    - [`Get-AzVMImage`](#get-azvmimage)
    - [`New-AzVMConfig`](#new-azvmconfig)
    - [`Update-AzVM`](#update-azvm)
    - [`New-AzProximityPlacementGroup`](#new-azproximityplacementgroup)
    - [`Remove-AzProximityPlacementGroup`](#remove-azproximityplacementgroup)
    - [`Get-AzProximityPlacementGroup`](#get-azproximityplacementgroup)
    - [`Add-AzVmssAdditionalUnattendContent`](#add-azvmssadditionalunattendcontent)
    - [`Add-AzVmssDataDisk`](#add-azvmssdatadisk)
    - [`Add-AzVmssExtension`](#add-azvmssextension)
    - [`Add-AzVmssNetworkInterfaceConfiguration`](#add-azvmssnetworkinterfaceconfiguration)
    - [`Add-AzVmssSecret`](#add-azvmsssecret)
    - [`Add-AzVmssSshPublicKey`](#add-azvmsssshpublickey)
    - [`Add-AzVmssWinRMListener`](#add-azvmsswinrmlistener)
    - [`New-AzVmssConfig`](#new-azvmssconfig)
    - [`Remove-AzVmssDataDisk`](#remove-azvmssdatadisk)
    - [`Remove-AzVmssExtension`](#remove-azvmssextension)
    - [`Remove-AzVmssNetworkInterfaceConfiguration`](#remove-azvmssnetworkinterfaceconfiguration)
    - [`Set-AzVmssBootDiagnostic`](#set-azvmssbootdiagnostic)
    - [`Set-AzVmssOsProfile`](#set-azvmssosprofile)
    - [`Set-AzVmssRollingUpgradePolicy`](#set-azvmssrollingupgradepolicy)
    - [`Set-AzVmssStorageProfile`](#set-azvmssstorageprofile)
    - [`New-AzVmss`](#new-azvmss)
    - [`Repair-AzVmssServiceFabricUpdateDomain`](#repair-azvmssservicefabricupdatedomain)
    - [`Get-AzVmss`](#get-azvmss)
    - [`Set-AzVmssOrchestrationServiceState`](#set-azvmssorchestrationservicestate)
    - [`Update-AzVmss`](#update-azvmss)
    - [`Add-AzVmssDiagnosticsExtension`](#add-azvmssdiagnosticsextension)
    - [`Disable-AzVmssDiskEncryption`](#disable-azvmssdiskencryption)
  - [<span data-ttu-id="a8807-112">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a8807-112">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="a8807-113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a8807-113">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="a8807-114">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8807-114">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="a8807-115">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a8807-115">Az.OperationalInsights</span></span>](#azoperationalinsights)
    - [`Get-AzOperationalInsightsDataSource`](#get-azoperationalinsightsdatasource)
    - [`New-AzOperationalInsightsApplicationInsightsDataSource`](#new-azoperationalinsightsapplicationinsightsdatasource)
    - [`New-AzOperationalInsightsAzureActivityLogDataSource`](#new-azoperationalinsightsazureactivitylogdatasource)
    - [`New-AzOperationalInsightsCustomLogDataSource`](#new-azoperationalinsightscustomlogdatasource)
    - [`New-AzOperationalInsightsLinuxPerformanceObjectDataSource`](#new-azoperationalinsightslinuxperformanceobjectdatasource)
    - [`New-AzOperationalInsightsLinuxSyslogDataSource`](#new-azoperationalinsightslinuxsyslogdatasource)
    - [`New-AzOperationalInsightsWindowsEventDataSource`](#new-azoperationalinsightswindowseventdatasource)
    - [`New-AzOperationalInsightsWindowsPerformanceCounterDataSource`](#new-azoperationalinsightswindowsperformancecounterdatasource)
    - [`Remove-AzOperationalInsightsDataSource`](#remove-azoperationalinsightsdatasource)
    - [`Disable-AzOperationalInsightsIISLogCollection`](#disable-azoperationalinsightsiislogcollection)
    - [`Disable-AzOperationalInsightsLinuxCustomLogCollection`](#disable-azoperationalinsightslinuxcustomlogcollection)
    - [`Disable-AzOperationalInsightsLinuxPerformanceCollection`](#disable-azoperationalinsightslinuxperformancecollection)
    - [`Disable-AzOperationalInsightsLinuxSyslogCollection`](#disable-azoperationalinsightslinuxsyslogcollection)
    - [`Enable-AzOperationalInsightsIISLogCollection`](#enable-azoperationalinsightsiislogcollection)
    - [`Enable-AzOperationalInsightsLinuxCustomLogCollection`](#enable-azoperationalinsightslinuxcustomlogcollection)
    - [`Enable-AzOperationalInsightsLinuxPerformanceCollection`](#enable-azoperationalinsightslinuxperformancecollection)
    - [`Enable-AzOperationalInsightsLinuxSyslogCollection`](#enable-azoperationalinsightslinuxsyslogcollection)
    - [`Get-AzOperationalInsightsSavedSearch`](#get-azoperationalinsightssavedsearch)
    - [`Get-AzOperationalInsightsSavedSearchResult`](#get-azoperationalinsightssavedsearchresult)
    - [`Get-AzOperationalInsightsSearchResult`](#get-azoperationalinsightssearchresult)
    - [`Get-AzOperationalInsightsStorageInsight`](#get-azoperationalinsightsstorageinsight)
    - [`New-AzOperationalInsightsStorageInsight`](#new-azoperationalinsightsstorageinsight)
    - [`Remove-AzOperationalInsightsStorageInsight`](#remove-azoperationalinsightsstorageinsight)
    - [`Set-AzOperationalInsightsStorageInsight`](#set-azoperationalinsightsstorageinsight)
    - [`Get-AzOperationalInsightsLinkTarget`](#get-azoperationalinsightslinktarget)
    - [`Get-AzOperationalInsightsWorkspace`](#get-azoperationalinsightsworkspace)
    - [`New-AzOperationalInsightsWorkspace`](#new-azoperationalinsightsworkspace)
    - [`Set-AzOperationalInsightsWorkspace`](#set-azoperationalinsightsworkspace)
    - [`Invoke-AzOperationalInsightsQuery`](#invoke-azoperationalinsightsquery)
  - [<span data-ttu-id="a8807-116">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8807-116">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="a8807-117">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8807-117">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="a8807-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="a8807-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="a8807-119">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="a8807-119">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="a8807-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="a8807-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="a8807-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="a8807-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="a8807-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="a8807-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="a8807-123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8807-123">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="a8807-124">Der Typ der Eigenschaft `Type` des Typs `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` wurde von `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` in `System.String` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-124">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="a8807-125">Das Cmdlet `New-AzApiManagement` unterstützt den Parameter `AssignIdentity` nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="a8807-125">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="a8807-126">Der Parametersatz `__AllParameterSets` für das Cmdlet `New-AzApiManagement` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-126">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="a8807-127">Das Cmdlet `Set-AzApiManagement` unterstützt den Parameter `AssignIdentity` nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="a8807-127">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="a8807-128">Der Parametersatz `__AllParameterSets` für das Cmdlet `Set-AzApiManagement` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-128">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="a8807-129">Das Cmdlet `Get-AzApiManagementProperty` wurde durch `Get-AzureApiManagementNamedValue` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a8807-129">The cmdlet `Get-AzApiManagementProperty` has been replaced by `Get-AzureApiManagementNamedValue`.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="a8807-130">Das Cmdlet `New-AzApiManagementProperty` wurde durch `New-AzureApiManagementNamedValue` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a8807-130">The cmdlet `New-AzApiManagementProperty` has been replaced by `New-AzureApiManagementNamedValue`.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="a8807-131">Das Cmdlet `Remove-AzApiManagementProperty` wurde durch `Remove-AzureApiManagementNamedValue` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a8807-131">The cmdlet `Remove-AzApiManagementProperty` has been replaced by `Remove-AzureApiManagementNamedValue`.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="a8807-132">Das Cmdlet `Set-AzApiManagementProperty` wurde durch `Set-AzureApiManagementNamedValue` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a8807-132">The cmdlet `Set-AzApiManagementProperty` has been replaced by `Set-AzureApiManagementNamedValue`.</span></span>

## <a name="azbatch"></a><span data-ttu-id="a8807-133">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a8807-133">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="a8807-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="a8807-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="a8807-135">Die `ApplicationPackages`-Eigenschaft vom Typ `Microsoft.Azure.Commands.Batch.Models.PSApplication` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-135">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="a8807-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="a8807-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="a8807-137">Die `PublicIPs`-Eigenschaft des Typs `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-137">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="a8807-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="a8807-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="a8807-139">Der Typ der Eigenschaft `StorageUrlExpiry` des Typs `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` wurde von `System.DateTime` in `System.DateTime?` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-139">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="a8807-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8807-140">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="a8807-141">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-141">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="a8807-142">Das Cmdlet `Get-AzVMImage` unterstützt den Parameter `FilterExpression` nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="a8807-142">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="a8807-143">Der Parametersatz `ListVMImage` für das Cmdlet `Get-AzVMImage` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-143">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="a8807-144">Das Cmdlet `New-AzVMConfig` unterstützt den Parameter `AssignIdentity` nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="a8807-144">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="a8807-145">Der Parametersatz `AssignIdentityParameterSet` für das Cmdlet `New-AzVMConfig` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-145">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="a8807-146">Das Cmdlet `Update-AzVM` unterstützt den Parameter `AssignIdentity` nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="a8807-146">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="a8807-147">Der Parametersatz `AssignIdentityParameterSet` für das Cmdlet `Update-AzVM` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-147">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="a8807-148">Der generische Typ für die Eigenschaften `VirtualMachines`, `VirtualMachineScaleSets` und `AvailabilitySets` wurde von `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` in `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-148">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="a8807-149">Die Eigenschaften `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` und `AvailabilitySetsColocationStatus` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-149">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="a8807-150">vor</span><span class="sxs-lookup"><span data-stu-id="a8807-150">Before</span></span>

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="a8807-151">Nach</span><span class="sxs-lookup"><span data-stu-id="a8807-151">After</span></span>

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Remove-AzProximityPlacementGroup`

- <span data-ttu-id="a8807-152">Der generische Typ für die Eigenschaften `VirtualMachines`, `VirtualMachineScaleSets` und `AvailabilitySets` wurde von `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` in `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-152">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="a8807-153">Die Eigenschaften `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` und `AvailabilitySetsColocationStatus` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-153">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="a8807-154">vor</span><span class="sxs-lookup"><span data-stu-id="a8807-154">Before</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="a8807-155">Nach</span><span class="sxs-lookup"><span data-stu-id="a8807-155">After</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Get-AzProximityPlacementGroup`

- <span data-ttu-id="a8807-156">Der generische Typ für die Eigenschaften `VirtualMachines`, `VirtualMachineScaleSets` und `AvailabilitySets` wurde von `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` in `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-156">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="a8807-157">Die Eigenschaften `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` und `AvailabilitySetsColocationStatus` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-157">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="a8807-158">vor</span><span class="sxs-lookup"><span data-stu-id="a8807-158">Before</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="a8807-159">Nach</span><span class="sxs-lookup"><span data-stu-id="a8807-159">After</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Add-AzVmssAdditionalUnattendContent`

<span data-ttu-id="a8807-160">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="a8807-161">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="a8807-162">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="a8807-163">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="a8807-164">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="a8807-165">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="a8807-166">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-166">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="a8807-167">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-167">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="a8807-168">Der Parameter `AutomaticRepairMaxInstanceRepairsPercent` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="a8807-168">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="a8807-169">Der Parameter `AssignIdentity` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="a8807-169">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="a8807-170">Der Parametersatz `__AllParameterSets` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-170">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="a8807-171">Der Parametersatz `ExplicitIdentityParameterSet` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-171">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="a8807-172">Der Parametersatz `AssignIdentityParameterSet` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-172">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="a8807-173">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="a8807-174">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="a8807-175">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="a8807-176">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="a8807-177">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="a8807-178">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="a8807-179">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="a8807-180">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="a8807-181">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="a8807-182">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="a8807-183">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-183">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="a8807-184">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-184">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="a8807-185">Der Parameter `AutomaticRepairMaxInstanceRepairsPercent` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="a8807-185">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="a8807-186">Der Parametersatz `__AllParameterSets` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-186">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="a8807-187">Der Parametersatz `ExplicitIdentityParameterSet` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-187">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="a8807-188">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-188">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="a8807-189">Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-189">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="a8807-190">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a8807-190">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="a8807-191">Der Alias `New-AzKeyVaultCertificateOrganizationDetails` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-191">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="a8807-192">Verwenden Sie `New-AzKeyVaultCertificateOrganizationDetail`.</span><span class="sxs-lookup"><span data-stu-id="a8807-192">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="a8807-193">vor</span><span class="sxs-lookup"><span data-stu-id="a8807-193">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="a8807-194">Nach</span><span class="sxs-lookup"><span data-stu-id="a8807-194">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="a8807-195">Der Alias `New-AzKeyVaultCertificateAdministratorDetails` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-195">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="a8807-196">Verwenden Sie `New-AzKeyVaultCertificateAdministratorDetail`.</span><span class="sxs-lookup"><span data-stu-id="a8807-196">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="a8807-197">vor</span><span class="sxs-lookup"><span data-stu-id="a8807-197">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="a8807-198">Nach</span><span class="sxs-lookup"><span data-stu-id="a8807-198">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="a8807-199">`-EnableSoftDelete` wurde entfernt, da das vorläufige Löschen standardmäßig aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a8807-199">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="a8807-200">Verwenden Sie `-DisableSoftDelete`, wenn Sie dieses Verhalten nicht wünschen.</span><span class="sxs-lookup"><span data-stu-id="a8807-200">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="a8807-201">vor</span><span class="sxs-lookup"><span data-stu-id="a8807-201">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="a8807-202">Nach</span><span class="sxs-lookup"><span data-stu-id="a8807-202">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="a8807-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a8807-203">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="a8807-204">Der Typ der Eigenschaft `RetentionPolicy` des Typs `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` wurde von `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` in `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-204">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="a8807-205">Der Typ der Eigenschaft `RetentionPolicy` des Typs `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` wurde von `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` in `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-205">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="a8807-206">Der Parametersatz `__AllParameterSets` für das Cmdlet `New-AzMetricAlertRuleV2Criteria` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-206">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="a8807-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8807-207">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="a8807-208">Der generische Typ für die Eigenschaft `RoundTripTimeMs` wurde von `System.Nullable1[System.Int32]` in `System.Nullable1[System.Double]` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-208">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="a8807-209">Der generische Typ für den Parameter `SuccessThresholdRoundTripTimeMs` wurde von `System.Nullable1[System.Int32]` in `System.Nullable1[System.Double]` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-209">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="a8807-210">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a8807-210">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="a8807-211">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="a8807-212">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="a8807-213">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="a8807-214">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="a8807-215">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="a8807-216">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="a8807-217">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="a8807-218">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="a8807-219">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="a8807-220">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="a8807-221">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="a8807-222">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="a8807-223">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="a8807-224">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="a8807-225">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="a8807-226">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-226">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="a8807-227">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-227">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="a8807-228">Die `Metadata`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-228">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="a8807-229">Das Cmdlet `Get-AzOperationalInsightsSavedSearchResult` wurde vom SDK nicht mehr unterstützt und wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-229">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="a8807-230">Das Cmdlet-`Get-AzOperationalInsightsSearchResult` wurde vom SDK nicht mehr unterstützt und wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-230">The cmdlet `Get-AzOperationalInsightsSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="a8807-231">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="a8807-232">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="a8807-233">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-233">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="a8807-234">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="a8807-235">Das Cmdlet `Get-AzOperationalInsightsLinkTarget` wurde vom SDK nicht mehr unterstützt und wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-235">The cmdlet `Get-AzOperationalInsightsLinkTarget` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="a8807-236">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-236">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="a8807-237">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-237">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="a8807-238">Das Cmdlet `New-AzOperationalInsightsWorkspace` unterstützt den Parameter `CustomerId` nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="a8807-238">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="a8807-239">Der Parametersatz `__AllParameterSets` für das Cmdlet `New-AzOperationalInsightsWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-239">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="a8807-240">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-240">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="a8807-241">Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-241">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="a8807-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8807-242">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="a8807-243">Der Typ der Eigenschaft `Status` des Typs `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` wurde von `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` in `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="a8807-244">Der Typ der Eigenschaft `Status` des Typs `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` wurde von `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` in `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-244">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="a8807-245">Der Typ der Eigenschaft `Status` des Typs `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` wurde von `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` in `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-245">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="a8807-246">Der Parameter `TenantLevel` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8807-246">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="a8807-247">Der generische Typ für die Eigenschaft `Aliases` wurde von `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` in `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-247">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="a8807-248">Das Cmdlet `New-AzPolicyAssignment` unterstützt den Typ `System.Management.Automation.PSObject` für den Parameter `PolicyDefinition` nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="a8807-248">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="a8807-249">Das Cmdlet `New-AzPolicyAssignment` unterstützt den Typ `System.Management.Automation.PSObject` für den Parameter `PolicySetDefinition` nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="a8807-249">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="a8807-250">Der Typ der Eigenschaft `Status` des Typs `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` wurde von `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` in `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` geändert.</span><span class="sxs-lookup"><span data-stu-id="a8807-250">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="a8807-251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8807-251">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="a8807-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="a8807-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="a8807-253">Der Wert von DefaultAction für NetWorkRule wurde geändert von: Allow = 1, Deny = 0 in: Allow = 0, Deny = 1.</span><span class="sxs-lookup"><span data-stu-id="a8807-253">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="a8807-254">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="a8807-254">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="a8807-255">Aus dem Output-Objekt von AzureStorageTable.CloudTable.ServiceClient wurden zwei Eigenschaften entfernt: ConnectionPolicy und ConsistencyLevel.</span><span class="sxs-lookup"><span data-stu-id="a8807-255">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="a8807-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="a8807-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="a8807-257">Der Ausgabetyp wurde von CloudFile in AzureStorageFile geändert. Die ursprüngliche Ausgabe wird zur untergeordneten Eigenschaft „CloudFile“ der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a8807-257">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="a8807-258">vor</span><span class="sxs-lookup"><span data-stu-id="a8807-258">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="a8807-259">Nach</span><span class="sxs-lookup"><span data-stu-id="a8807-259">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="a8807-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="a8807-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="a8807-261">Der Ausgabetyp wurde von CloudFileDirectory in AzureStorageFileDirectory geändert. Die ursprüngliche Ausgabe wird zur untergeordneten Eigenschaft „CloudFileDirectory“ der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a8807-261">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="a8807-262">vor</span><span class="sxs-lookup"><span data-stu-id="a8807-262">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="a8807-263">Nach</span><span class="sxs-lookup"><span data-stu-id="a8807-263">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="a8807-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="a8807-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="a8807-265">Der Ausgabetyp wurde von FileShareProperties in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zur untergeordneten Eigenschaft „CloudFileShare“ der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a8807-265">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="a8807-266">vor</span><span class="sxs-lookup"><span data-stu-id="a8807-266">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="a8807-267">Nach</span><span class="sxs-lookup"><span data-stu-id="a8807-267">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="a8807-268">Der Ausgabetyp von FileShareProperties wurde in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zur untergeordneten Eigenschaft „CloudFileShare.Properties“ der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a8807-268">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="a8807-269">vor</span><span class="sxs-lookup"><span data-stu-id="a8807-269">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="a8807-270">Nach</span><span class="sxs-lookup"><span data-stu-id="a8807-270">After</span></span>

```powershell
PS C:\> $share = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $share

   File End Point: https://weiors1.file.core.windows.net/

Name     QuotaGiB LastModified                IsSnapshot SnapshotTime
----     -------- ------------                ---------- ------------
weitest1 100      5/11/2020 3:03:30 PM +00:00 False

PS C:\> $share.CloudFileShare.Properties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

### `Remove-AzStorageDirectory`

<span data-ttu-id="a8807-271">Beim Entfernen untergeordneter Dateiverzeichnisse mit übergeordnetem Directory-Objekt und -Path kann die Eingabe für -Path nicht mehr über eine Pipeline mit einer Übereinstimmung vom Typ (string) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="a8807-271">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="a8807-272">vor</span><span class="sxs-lookup"><span data-stu-id="a8807-272">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="a8807-273">Nach</span><span class="sxs-lookup"><span data-stu-id="a8807-273">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
