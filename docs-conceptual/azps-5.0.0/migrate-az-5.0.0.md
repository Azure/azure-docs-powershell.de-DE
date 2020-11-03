---
title: Migrationsleitfaden für Az 5.0.0
description: Dieser Migrationsleitfaden enthält eine Liste mit Breaking Changes, die in Az-Version 5.0.0 an Azure PowerShell vorgenommen wurden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 3a82e738bcb652ddc38886f7064e7373b5fb8cc1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753823"
---
# <a name="migration-guide-for-az-500"></a>Migrationsleitfaden für Az 5.0.0

In diesem Dokument werden die Änderungen beschrieben, die zwischen den Versionen 4.0.0 und 5.0.0 von Az vorgenommen wurden.

- [Migrationsleitfaden für Az 5.0.0](#migration-guide-for-az-500)
  - [Az.Aks](#azaks)
    - [New-AzAksCluster](#new-azakscluster)
    - [Set-AzAksCluster](#set-azakscluster)
  - [Az.ContainerRegistry](#azcontainerregistry)
    - [New-AzContainerRegistry](#new-azcontainerregistry)
  - [Az.Functions](#azfunctions)
    - [Get-AzFunctionApp](#get-azfunctionapp)
    - [New-AzFunctionApp](#new-azfunctionapp)
  - [Az.KeyVault](#azkeyvault)
    - [New-AzKeyVault](#new-azkeyvault)
    - [Update-AzKeyVault](#update-azkeyvault)
    - [Get-AzKeyVaultSecret](#get-azkeyvaultsecret)
  - [Az.ManagedServices](#azmanagedservices)
    - [Get-AzManagedServicesDefinition](#get-azmanagedservicesdefinition)
    - [New-AzManagedServicesAssignment](#new-azmanagedservicesassignment)
    - [Remove-AzManagedServicesAssignment](#remove-azmanagedservicesassignment)
    - [Remove-AzManagedServicesDefinition](#remove-azmanagedservicesdefinition)
  - [Az.ResourceManager](#azresourcemanager)
    - [Get-AzManagementGroupDeployment](#get-azmanagementgroupdeployment)
    - [Get-AzManagementGroupDeploymentOperation](#get-azmanagementgroupdeploymentoperation)
    - [Get-AzDeployment](#get-azdeployment)
    - [Get-AzDeploymentOperation](#get-azdeploymentoperation)
    - [Get-AzDeploymentWhatIfResult](#get-azdeploymentwhatifresult)
    - [Get-AzTenantDeployment](#get-aztenantdeployment)
    - [Get-AzTenantDeploymentOperation](#get-aztenantdeploymentoperation)
    - [New-AzManagementGroupDeployment](#new-azmanagementgroupdeployment)
    - [New-AzDeployment](#new-azdeployment)
    - [New-AzTenantDeployment](#new-aztenantdeployment)
    - [Remove-AzManagementGroupDeployment](#remove-azmanagementgroupdeployment)
    - [Remove-AzDeployment](#remove-azdeployment)
    - [Remove-AzTenantDeployment](#remove-aztenantdeployment)
    - [Save-AzManagementGroupDeploymentTemplate](#save-azmanagementgroupdeploymenttemplate)
    - [Save-AzDeploymentTemplate](#save-azdeploymenttemplate)
    - [Save-AzTenantDeploymentTemplate](#save-aztenantdeploymenttemplate)
    - [Stop-AzManagementGroupDeployment](#stop-azmanagementgroupdeployment)
    - [Stop-AzDeployment](#stop-azdeployment)
    - [Stop-AzTenantDeployment](#stop-aztenantdeployment)
    - [Test-AzManagementGroupDeployment](#test-azmanagementgroupdeployment)
    - [Test-AzDeployment](#test-azdeployment)
    - [Test-AzTenantDeployment](#test-aztenantdeployment)
    - [Get-AzResourceGroupDeployment](#get-azresourcegroupdeployment)
    - [Get-AzResourceGroupDeploymentOperation](#get-azresourcegroupdeploymentoperation)
    - [Get-AzResourceGroupDeploymentWhatIfResult](#get-azresourcegroupdeploymentwhatifresult)
    - [New-AzResourceGroupDeployment](#new-azresourcegroupdeployment)
    - [Remove-AzResourceGroupDeployment](#remove-azresourcegroupdeployment)
    - [Save-AzResourceGroupDeploymentTemplate](#save-azresourcegroupdeploymenttemplate)
    - [Stop-AzResourceGroupDeployment](#stop-azresourcegroupdeployment)
    - [Test-AzResourceGroupDeployment](#test-azresourcegroupdeployment)
    - [Get-AzManagementGroupDeploymentWhatIfResult](#get-azmanagementgroupdeploymentwhatifresult)
    - [Get-AzTenantDeploymentWhatIfResult](#get-aztenantdeploymentwhatifresult)
  - [Az.Sql](#azsql)
    - [Set-AzSqlServerActiveDirectoryAdministrator](#set-azsqlserveractivedirectoryadministrator)
  - [Az.Synapse](#azsynapse)
    - [New-AzSynapseSqlPool](#new-azsynapsesqlpool)
    - [Update-AzSynapseSqlPool](#update-azsynapsesqlpool)
  - [Az.Network](#aznetwork)
    - [Approve-AzPrivateEndpointConnection](#approve-azprivateendpointconnection)
    - [Deny-AzPrivateEndpointConnection](#deny-azprivateendpointconnection)
    - [Get-AzPrivateEndpointConnection](#get-azprivateendpointconnection)
    - [Remove-AzPrivateEndpointConnection](#remove-azprivateendpointconnection)
    - [Set-AzPrivateEndpointConnection](#set-azprivateendpointconnection)
    - [New-AzNetworkWatcherConnectionMonitorEndpointObject](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a>Az.Aks

### <a name="new-azakscluster"></a>New-AzAksCluster

- Der Parameter `NodeOsType` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden. Er lautet immer `Linux`.
- Der Alias `ClientIdAndSecret` für den Parameter `ServicePrincipalIdAndSecret` wird nicht mehr unterstützt.
- Der Standardwert von `NodeVmSetType` wurde von `AvailabilitySet` in `VirtualMachineScaleSets` geändert.
- Der Standardwert von `NetworkPlugin` wurde von `none` in `azure` geändert.

#### <a name="before"></a>Vorher

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a>Danach

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a>Set-AzAksCluster

Der Alias `ClientIdAndSecret` für den Parameter `ServicePrincipalIdAndSecret` wird nicht mehr unterstützt.

#### <a name="before"></a>Vorher

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a>Danach

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a>Az.ContainerRegistry

### <a name="new-azcontainerregistry"></a>New-AzContainerRegistry

Der Parameter `StorageAccountName` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.

#### <a name="before"></a>Vorher

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a>Danach

`Classic` wurde als veraltet eingestuft, und der Parameter `StorageAccountName` wurde entfernt, da er nur mit der klassischen Containerregistrierung funktioniert.

## <a name="azfunctions"></a>Az.Functions

### <a name="get-azfunctionapp"></a>Get-AzFunctionApp

Der Switch-Parameter `IncludeSlot` wurde aus allen Parametersätzen von „`Get-AzFunctionApp`“ entfernt (bis auf einen). Das Cmdlet unterstützt jetzt das Abrufen von Bereitstellungsslots in den Ergebnissen, wenn `-IncludeSlot` angegeben ist.
Diese Funktionalität war in der vorherigen Cmdlet-Version beschädigt. Der Fehler ist jetzt aber behoben.

### <a name="new-azfunctionapp"></a>New-AzFunctionApp

- `-DisableApplicationInsights` wurde in `New-AzFunctionApp` korrigiert, damit bei Angabe dieser Option kein Application Insights-Projekt erstellt wird.
- Die Unterstützung für die Erstellung von PowerShell 6.2-Funktions-Apps wurde entfernt, da für PowerShell 6.2 der EOL-Zeitpunkt erreicht wurde. Für Kunden wird derzeit empfohlen, stattdessen PowerShell 7.0-Funktions-Apps zu erstellen.
- Es wurde festgelegt, dass in Functions-Version 3 von Windows für PowerShell-Funktions-Apps anstelle der Runtime-Standardversion 6.2 die Version 7.0 verwendet wird, wenn der Parameter `RuntimeVersion` nicht angegeben ist.
- Es wurde festgelegt, dass in Functions-Version 3 von Windows/Linux für Node-Funktions-Apps anstelle der Runtime-Standardversion 10 die Version 12 verwendet wird, wenn der Parameter `RuntimeVersion` nicht angegeben ist. Benutzer können aber weiterhin Node 10-Funktions-Apps erstellen, indem sie `-Runtime Node` und `-RuntimeVersion 10` angeben. Es wurde festgelegt, dass in Functions-Version 3 von Linux für Python-Funktions-Apps anstelle der Runtime-Standardversion 3.7 die Version 3.8 verwendet wird, wenn der Parameter `RuntimeVersion` nicht angegeben ist. Benutzer können aber weiterhin Python 3.7-Funktions-Apps erstellen, indem sie `-Runtime Python` und `-RuntimeVersion 3.7` angeben.

#### <a name="before"></a>Vorher

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python
```

#### <a name="after"></a>Danach

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node `
                  -RuntimeVersion 10

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python `
                  -RuntimeVersion 3.7
```

## <a name="azkeyvault"></a>Az.KeyVault

### <a name="new-azkeyvault"></a>New-AzKeyVault

Der Parameter `DisableSoftDelete` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.

#### <a name="before"></a>Vorher

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a>Danach

Die Möglichkeit zum Aktualisieren der Einstellung für das vorläufige Löschen wurde in Az.KeyVault 3.0.0 als veraltet eingestuft. Weitere Informationen: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="update-azkeyvault"></a>Update-AzKeyVault

Die Parameter `EnableSoftDelete` und `SoftDeleteRetentionInDays` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.

#### <a name="before"></a>Vorher

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a>Danach

Die Möglichkeit zum Aktualisieren der Einstellung für das vorläufige Löschen wurde in Az.KeyVault 3.0.0 als veraltet eingestuft. Weitere Informationen: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="get-azkeyvaultsecret"></a>Get-AzKeyVaultSecret

Die `SecretValueText`-Eigenschaft vom Typ `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` wurde entfernt. Die Eigenschaft `SecretValueText` wurde durch `SecretValue` ersetzt.

#### <a name="before"></a>Vorher

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a>Danach

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a>Az.ManagedServices

### <a name="get-azmanagedservicesdefinition"></a>Get-AzManagedServicesDefinition

Der Parameter `ResourceId` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.

#### <a name="before"></a>Vorher

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>Danach

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a>New-AzManagedServicesAssignment

Die Parameter `RegistrationDefinitionName` und `RegistrationDefinitionResourceId` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.

#### <a name="before"></a>Vorher

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a>Danach

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a>Remove-AzManagedServicesAssignment

Die Parameter `Id` und `ResourceId` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.

#### <a name="before"></a>Vorher

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a>Danach

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a>Remove-AzManagedServicesDefinition

Die Parameter `Id` und `ResourceId` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.

#### <a name="before"></a>Vorher

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>Danach

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a>Az.ResourceManager

### <a name="get-azmanagementgroupdeployment"></a>Get-AzManagementGroupDeployment

Der Parameter `ApiVersion` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.

#### <a name="before"></a>Vorher

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a>Danach

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a>Get-AzManagementGroupDeploymentOperation

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="get-azdeployment"></a>Get-AzDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="get-azdeploymentoperation"></a>Get-AzDeploymentOperation

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="get-azdeploymentwhatifresult"></a>Get-AzDeploymentWhatIfResult

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="get-aztenantdeployment"></a>Get-AzTenantDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="get-aztenantdeploymentoperation"></a>Get-AzTenantDeploymentOperation

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="new-azmanagementgroupdeployment"></a>New-AzManagementGroupDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="new-azdeployment"></a>New-AzDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="new-aztenantdeployment"></a>New-AzTenantDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="remove-azmanagementgroupdeployment"></a>Remove-AzManagementGroupDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="remove-azdeployment"></a>Remove-AzDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="remove-aztenantdeployment"></a>Remove-AzTenantDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="save-azmanagementgroupdeploymenttemplate"></a>Save-AzManagementGroupDeploymentTemplate

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="save-azdeploymenttemplate"></a>Save-AzDeploymentTemplate

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="save-aztenantdeploymenttemplate"></a>Save-AzTenantDeploymentTemplate

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="stop-azmanagementgroupdeployment"></a>Stop-AzManagementGroupDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="stop-azdeployment"></a>Stop-AzDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="stop-aztenantdeployment"></a>Stop-AzTenantDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="test-azmanagementgroupdeployment"></a>Test-AzManagementGroupDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="test-azdeployment"></a>Test-AzDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="test-aztenantdeployment"></a>Test-AzTenantDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="get-azresourcegroupdeployment"></a>Get-AzResourceGroupDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="get-azresourcegroupdeploymentoperation"></a>Get-AzResourceGroupDeploymentOperation

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="get-azresourcegroupdeploymentwhatifresult"></a>Get-AzResourceGroupDeploymentWhatIfResult

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="new-azresourcegroupdeployment"></a>New-AzResourceGroupDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="remove-azresourcegroupdeployment"></a>Remove-AzResourceGroupDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="save-azresourcegroupdeploymenttemplate"></a>Save-AzResourceGroupDeploymentTemplate

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="stop-azresourcegroupdeployment"></a>Stop-AzResourceGroupDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="test-azresourcegroupdeployment"></a>Test-AzResourceGroupDeployment

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a>Get-AzManagementGroupDeploymentWhatIfResult

Identisch mit `Get-AzManagementGroupDeployment`.

### <a name="get-aztenantdeploymentwhatifresult"></a>Get-AzTenantDeploymentWhatIfResult

Identisch mit `Get-AzManagementGroupDeployment`.

## <a name="azsql"></a>Az.Sql

### <a name="set-azsqlserveractivedirectoryadministrator"></a>Set-AzSqlServerActiveDirectoryAdministrator

Der Parameter `IsAzureADOnlyAuthentication` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.

#### <a name="before"></a>Vorher

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a>Danach

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a>Az.Synapse

### <a name="new-azsynapsesqlpool"></a>New-AzSynapseSqlPool

Die Parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId` und `RestorePoint` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.

#### <a name="before"></a>Vorher

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a>Danach

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a>Update-AzSynapseSqlPool

Die Parameter `Suspend` und `Resume` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.

## <a name="aznetwork"></a>Az.Network

### <a name="approve-azprivateendpointconnection"></a>Approve-AzPrivateEndpointConnection

Der Parameter `PrivateLinkResourceType` wird nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.

#### <a name="before"></a>Vorher

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a>Danach

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a>Deny-AzPrivateEndpointConnection

Identisch mit `Approve-AzPrivateEndpointConnection`.

### <a name="get-azprivateendpointconnection"></a>Get-AzPrivateEndpointConnection

Identisch mit `Approve-AzPrivateEndpointConnection`.

### <a name="remove-azprivateendpointconnection"></a>Remove-AzPrivateEndpointConnection

Identisch mit `Approve-AzPrivateEndpointConnection`.

### <a name="set-azprivateendpointconnection"></a>Set-AzPrivateEndpointConnection

Identisch mit `Approve-AzPrivateEndpointConnection`.

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a>New-AzNetworkWatcherConnectionMonitorEndpointObject

Die Parameter `FilterType` und `FilterItem` werden nicht mehr unterstützt, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.

#### <a name="before"></a>Vorher

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a>Nach

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
