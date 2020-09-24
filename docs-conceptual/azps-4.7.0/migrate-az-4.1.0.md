---
title: Migrationsleitfaden für Az 4.1.0
description: Dieser Migrationsleitfaden enthält eine Liste mit Breaking Changes, die in Az-Version 4.1.0 an Azure PowerShell vorgenommen wurden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: c64541beb5eb0d3db38932fb3915de865919641b
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "90928156"
---
# <a name="migration-guide-for-az-410"></a>Migrationsleitfaden für Az 4.1.0

In diesem Dokument werden die Änderungen beschrieben, die zwischen den Versionen 3.0.0 und 4.1.0 von Az vorgenommen wurden.

- [Migrationsleitfaden für Az 4.1.0](#migration-guide-for-az-410)
  - [Az.ApiManagement](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [Az.Batch](#azbatch)
    - [`Get-AzBatchApplication`, `New-AzBatchApplication`](#get-azbatchapplication-new-azbatchapplication)
    - [`Get-AzBatchComputeNode`, `New-AzBatchPool`](#get-azbatchcomputenode-new-azbatchpool)
    - [`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [Az.Compute](#azcompute)
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
  - [Az.KeyVault](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [Az.Monitor](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [Az.Network](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [Az.OperationalInsights](#azoperationalinsights)
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
  - [Az.Resources](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [Az.Storage](#azstorage)
    - [`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [`New-AzStorageTable`, `Get-AzStorageTable`](#new-azstoragetable-get-azstoragetable)
    - [`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a>Az.ApiManagement

### `Add-AzApiManagementRegion`

Der Typ der Eigenschaft `Type` des Typs `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` wurde von `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` in `System.String` geändert.

### `New-AzApiManagement`

- Das Cmdlet `New-AzApiManagement` unterstützt den Parameter `AssignIdentity` nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.
- Der Parametersatz `__AllParameterSets` für das Cmdlet `New-AzApiManagement` wurde entfernt.

### `Set-AzApiManagement`

- Das Cmdlet `Set-AzApiManagement` unterstützt den Parameter `AssignIdentity` nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.
- Der Parametersatz `__AllParameterSets` für das Cmdlet `Set-AzApiManagement` wurde entfernt.

### `Get-AzApiManagementProperty`

Das Cmdlet `Get-AzApiManagementProperty` wurde durch `Get-AzApiManagementNamedValue` ersetzt.

### `New-AzApiManagementProperty`

Das Cmdlet `New-AzApiManagementProperty` wurde durch `New-AzApiManagementNamedValue` ersetzt.

### `Remove-AzApiManagementProperty`

Das Cmdlet `Remove-AzApiManagementProperty` wurde durch `Remove-AzApiManagementNamedValue` ersetzt.

### `Set-AzApiManagementProperty`

Das Cmdlet `Set-AzApiManagementProperty` wurde durch `Set-AzApiManagementNamedValue` ersetzt.

## <a name="azbatch"></a>Az.Batch

### <a name="get-azbatchapplication-new-azbatchapplication"></a>`Get-AzBatchApplication`, `New-AzBatchApplication`

Die `ApplicationPackages`-Eigenschaft vom Typ `Microsoft.Azure.Commands.Batch.Models.PSApplication` wurde entfernt.

### <a name="get-azbatchcomputenode-new-azbatchpool"></a>`Get-AzBatchComputeNode`, `New-AzBatchPool`

Die `PublicIPs`-Eigenschaft des Typs `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` wurde entfernt.

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a>`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`

Der Typ der Eigenschaft `StorageUrlExpiry` des Typs `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` wurde von `System.DateTime` in `System.DateTime?` geändert.

## <a name="azcompute"></a>Az.Compute

### `Remove-AzVmssDiagnosticsExtension`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Get-AzVMImage`

- Das Cmdlet `Get-AzVMImage` unterstützt den Parameter `FilterExpression` nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.
- Der Parametersatz `ListVMImage` für das Cmdlet `Get-AzVMImage` wurde entfernt.

### `New-AzVMConfig`

- Das Cmdlet `New-AzVMConfig` unterstützt den Parameter `AssignIdentity` nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.
- Der Parametersatz `AssignIdentityParameterSet` für das Cmdlet `New-AzVMConfig` wurde entfernt.

### `Update-AzVM`

- Das Cmdlet `Update-AzVM` unterstützt den Parameter `AssignIdentity` nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.
- Der Parametersatz `AssignIdentityParameterSet` für das Cmdlet `Update-AzVM` wurde entfernt.

### `New-AzProximityPlacementGroup`

- Der generische Typ für die Eigenschaften `VirtualMachines`, `VirtualMachineScaleSets` und `AvailabilitySets` wurde von `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` in `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` geändert.
- Die Eigenschaften `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` und `AvailabilitySetsColocationStatus` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` wurden entfernt.

#### <a name="before"></a>vor

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

#### <a name="after"></a>Nach

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

- Der generische Typ für die Eigenschaften `VirtualMachines`, `VirtualMachineScaleSets` und `AvailabilitySets` wurde von `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` in `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` geändert.
- Die Eigenschaften `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` und `AvailabilitySetsColocationStatus` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` wurden entfernt.

#### <a name="before"></a>vor

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

#### <a name="after"></a>Nach

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

- Der generische Typ für die Eigenschaften `VirtualMachines`, `VirtualMachineScaleSets` und `AvailabilitySets` wurde von `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` in `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]` geändert.
- Die Eigenschaften `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` und `AvailabilitySetsColocationStatus` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` wurden entfernt.

#### <a name="before"></a>vor

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

#### <a name="after"></a>Nach

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

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Add-AzVmssDataDisk`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Add-AzVmssExtension`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Add-AzVmssNetworkInterfaceConfiguration`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Add-AzVmssSecret`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Add-AzVmssSshPublicKey`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Add-AzVmssWinRMListener`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `New-AzVmssConfig`

- Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.
- Der Parameter `AutomaticRepairMaxInstanceRepairsPercent` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.
- Der Parameter `AssignIdentity` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.
- Der Parametersatz `__AllParameterSets` wurde entfernt.
- Der Parametersatz `ExplicitIdentityParameterSet` wurde entfernt.
- Der Parametersatz `AssignIdentityParameterSet` wurde entfernt.

### `Remove-AzVmssDataDisk`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Remove-AzVmssExtension`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Remove-AzVmssNetworkInterfaceConfiguration`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Set-AzVmssBootDiagnostic`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Set-AzVmssOsProfile`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Set-AzVmssRollingUpgradePolicy`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Set-AzVmssStorageProfile`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `New-AzVmss`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Repair-AzVmssServiceFabricUpdateDomain`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Get-AzVmss`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Set-AzVmssOrchestrationServiceState`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Update-AzVmss`

- Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.
- Der Parameter `AutomaticRepairMaxInstanceRepairsPercent` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.
- Der Parametersatz `__AllParameterSets` wurde entfernt.
- Der Parametersatz `ExplicitIdentityParameterSet` wurde entfernt.

### `Add-AzVmssDiagnosticsExtension`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

### `Disable-AzVmssDiskEncryption`

Der Typ der Eigenschaft `AutomaticRepairsPolicy` des Typs `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` wurde von `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` in `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy` geändert.

## <a name="azkeyvault"></a>Az.KeyVault

### `New-AzKeyVaultCertificateOrganizationDetail`

Der Alias `New-AzKeyVaultCertificateOrganizationDetails` wurde entfernt. Verwenden Sie `New-AzKeyVaultCertificateOrganizationDetail`.

#### <a name="before"></a>vor

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a>Nach

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

Der Alias `New-AzKeyVaultCertificateAdministratorDetails` wurde entfernt. Verwenden Sie `New-AzKeyVaultCertificateAdministratorDetail`.

#### <a name="before"></a>vor

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a>Nach

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

`-EnableSoftDelete` wurde entfernt, da das vorläufige Löschen standardmäßig aktiviert ist. Verwenden Sie `-DisableSoftDelete`, wenn Sie dieses Verhalten nicht wünschen.

#### <a name="before"></a>vor

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a>Nach

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a>Az.Monitor

### `Add-AzLogProfile`

Der Typ der Eigenschaft `RetentionPolicy` des Typs `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` wurde von `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` in `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy` geändert.

### `Get-AzLogProfile`

Der Typ der Eigenschaft `RetentionPolicy` des Typs `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` wurde von `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` in `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy` geändert.

### `New-AzMetricAlertRuleV2Criteria`

Der Parametersatz `__AllParameterSets` für das Cmdlet `New-AzMetricAlertRuleV2Criteria` wurde entfernt.

## <a name="aznetwork"></a>Az.Network

### `Get-AzNetworkWatcherConnectionMonitor`

Der generische Typ für die Eigenschaft `RoundTripTimeMs` wurde von `System.Nullable1[System.Int32]` in `System.Nullable1[System.Double]` geändert.

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

Der generische Typ für den Parameter `SuccessThresholdRoundTripTimeMs` wurde von `System.Nullable1[System.Int32]` in `System.Nullable1[System.Double]` geändert.

## <a name="azoperationalinsights"></a>Az.OperationalInsights

### `Get-AzOperationalInsightsDataSource`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `New-AzOperationalInsightsApplicationInsightsDataSource`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `New-AzOperationalInsightsAzureActivityLogDataSource`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `New-AzOperationalInsightsCustomLogDataSource`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `New-AzOperationalInsightsLinuxSyslogDataSource`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `New-AzOperationalInsightsWindowsEventDataSource`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Remove-AzOperationalInsightsDataSource`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Disable-AzOperationalInsightsIISLogCollection`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Enable-AzOperationalInsightsIISLogCollection`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Get-AzOperationalInsightsSavedSearch`

Die `Metadata`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` wurde entfernt.

### `Get-AzOperationalInsightsSavedSearchResult`

Das Cmdlet `Get-AzOperationalInsightsSavedSearchResult` wurde vom SDK nicht mehr unterstützt und wurde entfernt.

### `Get-AzOperationalInsightsSearchResult`

Das Cmdlet-`Get-AzOperationalInsightsSearchResult` wurde vom SDK nicht mehr unterstützt und wurde entfernt.

### `Get-AzOperationalInsightsStorageInsight`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `New-AzOperationalInsightsStorageInsight`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Remove-AzOperationalInsightsStorageInsight`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Set-AzOperationalInsightsStorageInsight`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Get-AzOperationalInsightsLinkTarget`

Das Cmdlet `Get-AzOperationalInsightsLinkTarget` wurde vom SDK nicht mehr unterstützt und wurde entfernt.

### `Get-AzOperationalInsightsWorkspace`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `New-AzOperationalInsightsWorkspace`

- Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.
- Das Cmdlet `New-AzOperationalInsightsWorkspace` unterstützt den Parameter `CustomerId` nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.
- Der Parametersatz `__AllParameterSets` für das Cmdlet `New-AzOperationalInsightsWorkspace` wurde entfernt.

### `Set-AzOperationalInsightsWorkspace`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

### `Invoke-AzOperationalInsightsQuery`

Die `PortalUrl`-Eigenschaft vom Typ `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` wurde entfernt.

## <a name="azresources"></a>Az.Resources

### `Get-AzDeploymentScript`

Der Typ der Eigenschaft `Status` des Typs `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` wurde von `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` in `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` geändert.

### `Get-AzDeploymentScriptLog`

Der Typ der Eigenschaft `Status` des Typs `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` wurde von `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` in `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` geändert.

### `Save-AzDeploymentScriptLog`

Der Typ der Eigenschaft `Status` des Typs `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` wurde von `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` in `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` geändert.

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

Der Parameter `TenantLevel` wurde entfernt.

### `Get-AzPolicyAlias`

Der generische Typ für die Eigenschaft `Aliases` wurde von `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` in `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]` geändert.

### `New-AzPolicyAssignment`

- Das Cmdlet `New-AzPolicyAssignment` unterstützt den Typ `System.Management.Automation.PSObject` für den Parameter `PolicyDefinition` nicht mehr.
- Das Cmdlet `New-AzPolicyAssignment` unterstützt den Typ `System.Management.Automation.PSObject` für den Parameter `PolicySetDefinition` nicht mehr.

### `Remove-AzDeploymentScript`

Der Typ der Eigenschaft `Status` des Typs `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` wurde von `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` in `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus` geändert.

## <a name="azstorage"></a>Az.Storage

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a>`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`

Der Wert von DefaultAction für NetWorkRule wurde geändert von: Allow = 1, Deny = 0 in: Allow = 0, Deny = 1.

### <a name="new-azstoragetable-get-azstoragetable"></a>`New-AzStorageTable`, `Get-AzStorageTable`

Aus dem Output-Objekt von AzureStorageTable.CloudTable.ServiceClient wurden zwei Eigenschaften entfernt: ConnectionPolicy und ConsistencyLevel.

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a>`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`

Der Ausgabetyp wurde von CloudFile in AzureStorageFile geändert. Die ursprüngliche Ausgabe wird zur untergeordneten Eigenschaft „CloudFile“ der neuen Ausgabe.

#### <a name="before"></a>vor

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a>Nach

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a>`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`

Der Ausgabetyp wurde von CloudFileDirectory in AzureStorageFileDirectory geändert. Die ursprüngliche Ausgabe wird zur untergeordneten Eigenschaft „CloudFileDirectory“ der neuen Ausgabe.

#### <a name="before"></a>vor

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>Nach

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a>`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`

Der Ausgabetyp wurde von FileShareProperties in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zur untergeordneten Eigenschaft „CloudFileShare“ der neuen Ausgabe.

#### <a name="before"></a>vor

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a>Nach

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

Der Ausgabetyp von FileShareProperties wurde in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zur untergeordneten Eigenschaft „CloudFileShare.Properties“ der neuen Ausgabe.

#### <a name="before"></a>vor

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a>Nach

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

Beim Entfernen untergeordneter Dateiverzeichnisse mit übergeordnetem Directory-Objekt und -Path kann die Eingabe für -Path nicht mehr über eine Pipeline mit einer Übereinstimmung vom Typ (string) erfolgen.

#### <a name="before"></a>vor

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>Nach

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
