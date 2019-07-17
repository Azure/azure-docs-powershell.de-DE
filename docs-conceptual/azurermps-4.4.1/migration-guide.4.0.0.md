---
title: Grundlegende Änderungen für Microsoft Azure PowerShell 4.0.0
description: Dieser Migrationsleitfaden enthält eine Liste mit grundlegenden Änderungen, die in Version 4 an Azure PowerShell vorgenommen wurden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 2f61e41b701dfc263df18064f6ac2cc4c6e4021e
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863556"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a>Grundlegende Änderungen für Microsoft Azure PowerShell 4.0.0

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Dieses Dokument informiert über grundlegende Änderungen und fungiert als Migrationsleitfaden für Kunden mit Microsoft Azure PowerShell-Cmdlets. In den einzelnen Abschnitten werden jeweils der Grund für die grundlegende Änderung und der Migrationspfad des geringsten Widerstands beschrieben. Ausführlichen Kontext finden Sie unter der Pull-Anforderung für die jeweilige Änderung.

## <a name="table-of-contents"></a>Inhaltsverzeichnis

- [Grundlegende Änderungen für Compute-Cmdlets](#breaking-changes-to-compute-cmdlets)
- [Grundlegende Änderungen für EventHub-Cmdlets](#breaking-changes-to-eventhub-cmdlets)
- [Grundlegende Änderungen für Insights-Cmdlets](#breaking-changes-to-insights-cmdlets)
- [Grundlegende Änderungen für Network-Cmdlets](#breaking-changes-to-network-cmdlets)
- [Grundlegende Änderungen für ServiceBus-Cmdlets](#breaking-changes-to-servicebus-cmdlets)
- [Grundlegende Änderungen für Sql-Cmdlets](#breaking-changes-to-sql-cmdlets)
- [Grundlegende Änderungen für Storage-Cmdlets](#breaking-changes-to-storage-cmdlets)
- [Grundlegende Änderungen für Profile-Cmdlets](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a>Grundlegende Änderungen für Compute-Cmdlets

Diese Version hat Auswirkungen auf folgende Ausgabetypen:

### <a name="psvirtualmachine"></a>PSVirtualMachine
- Die übergeordneten Eigenschaften `DataDiskNames` und `NetworkInterfaceIDs` des Objekts `PSVirtualMachine` wurden aus dem Ausgabetyp entfernt. Diese Eigenschaften waren schon immer in den Eigenschaften `StorageProfile` und `NetworkProfile` des Objekts `PSVirtualMachine` verfügbar und müssen fortan für den Zugriff auf die Eigenschaften verwendet werden.
- Diese Änderung wirkt sich auf folgende Cmdlets aus:
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell-interactive
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>Grundlegende Änderungen für EventHub-Cmdlets

Diese Version hat Auswirkungen auf folgende Cmdlets:

### <a name="get-azurermeventhubnamespace"></a>Get-AzureRmEventHubNamespace
- Die Eigenschaft `ResourceGroupName` wurde aus dem Ausgabetyp `NamespaceAttributes` entfernt.

### <a name="new-azurermeventhubnamespace"></a>New-AzureRmEventHubNamespace
- Die Eigenschaft `ResourceGroupName` wurde aus dem Ausgabetyp `NamespaceAttributes` entfernt.

## <a name="breaking-changes-to-insights-cmdlets"></a>Grundlegende Änderungen für Insights-Cmdlets

Diese Version hat Auswirkungen auf folgende Cmdlets:
    
### <a name="get-azurermusage"></a>Get-AzureRmUsage
- Dieses Cmdlet ist veraltet.

### <a name="remove-azurermalertrule"></a>Remove-AzureRmAlertRule
- Die Ausgabe dieses Cmdlets wurde von einer Liste mit einem einzelnen Objekt in ein einzelnes Objekt geändert, das die Anforderungs-ID und den Statuscode enthält.
    
```powershell-interactive
# Old  
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogalertrule"></a>Add-AzureRmLogAlertRule
- Dieses Cmdlet ist veraltet.
    
### <a name="get-azurermalertrule"></a>Get-AzureRmAlertRule
- Jedes Element der Ausgabe dieses Cmdlets (eine Liste mit Objekten) wird vereinfacht. Anstelle von Objekten mit der Struktur `{ Id, Location, Name, Tags, Properties }` werden also Objekte mit der Struktur `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}` zurückgegeben. Diese umfasst alle Attribute einer Azure-Ressource sowie alle Attribute eines AlertRuleResource-Objekts auf der obersten Ebene.
    
```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
      
    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
 
    Write-Host $rules(0).Id
      
    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```
    
### <a name="get-azurermautoscalesetting"></a>Get-AzureRmAutoscaleSetting
- Das Feld `AutoscaleSettingResourceName` ist veraltet, da es immer denselben Wert besitzt wie das Feld `Name`.

```powershell-interactive
# Old  
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```
    
### <a name="remove-azurermlogprofile"></a>Remove-AzureRmLogProfile
- Die Ausgabe dieses Cmdlets ändert sich von `Boolean` in ein Objekt mit `RequestId` und `StatusCode`.

```powershell-interactive
# Old  
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogprofile"></a>Add-AzureRmLogProfile
- Die Ausgabe dieses Cmdlets ändert sich von einem Objekt mit Anforderungs-ID, Statuscode und aktualisierter oder neu erstellter Ressource.
    
```powershell-interactive
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a>Set-AzureRmDiagnosticSettings
- Der Befehl wird in `Update-AzureRmDiagnosticSettings` umbenannt.

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a>Grundlegende Änderungen für Network-Cmdlets

Diese Version hat Auswirkungen auf folgende Cmdlets:

### <a name="new-azurermvirtualnetworkgatewayconnection"></a>New-AzureRmVirtualNetworkGatewayConnection
- Der Parameter `EnableBgp` wurde geändert und akzeptiert nun einen Wert vom Typ `boolean` anstelle eines Werts vom Typ `string`.

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>Grundlegende Änderungen für ServiceBus-Cmdlets

Diese Version hat Auswirkungen auf folgende Cmdlets:

### <a name="get-azurermservicebusnamespace"></a>Get-AzureRmServiceBusNamespace
- Die Eigenschaft `ResourceGroupName` wurde aus dem Ausgabetyp `NamespaceAttributes` entfernt.

### <a name="new-azurermservicebusnamespace"></a>New-AzureRmServiceBusNamespace

- Die Eigenschaft `ResourceGroupName` wurde aus dem Ausgabetyp `NamespaceAttributes` entfernt.

## <a name="breaking-changes-to-sql-cmdlets"></a>Grundlegende Änderungen für Sql-Cmdlets

Diese Version hat Auswirkungen auf folgende Cmdlets:

### <a name="new-azurermsqldatabasefailovergroup"></a>New-AzureRmSqlDatabaseFailoverGroup
- Der Parameter `Tag` wurde entfernt.
- Der Parameter `GracePeriodWithDataLossHour` wurde in `GracePeriodWithDataLossHours` umbenannt.

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a>Set-AzureRmSqlDatabaseFailoverGroup
- Der Parameter `Tag` wurde entfernt.
- Der Parameter `GracePeriodWithDataLossHour` wurde in `GracePeriodWithDataLossHours` umbenannt.

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a>Add-AzureRmSqlDatabaseToFailoverGroup
- Der Parameter `Tag` wurde entfernt.

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a>Remove-AzureRmSqlDatabaseFromFailoverGroup
- Der Parameter `Tag` wurde entfernt.

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a>Remove-AzureRmSqlDatabaseFailoverGroup
- Der Parameter `PartnerResourceGroupName` wurde entfernt.
- Der Parameter `PartnerServerName` wurde entfernt.

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a>Set-AzureRmSqlDatabaseThreatDetectionPolicy
- Der Wert `Usage_Anomaly` ist für den Parameter `ExcludedDetectionType` nicht mehr gültig.

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a>Set-AzureRmSqlServerThreatDetectionPolicy
- Der Wert `Usage_Anomaly` ist für den Parameter `ExcludedDetectionType` nicht mehr gültig.

## <a name="breaking-changes-to-storage-cmdlets"></a>Grundlegende Änderungen für Storage-Cmdlets

Diese Version hat Auswirkungen auf folgende Ausgabetypeigenschaften:

### <a name="azurestorageblobicloudblobserviceclient"></a>AzureStorageBlob.ICloudBlob.ServiceClient
- Folgende Eigenschaften wurden aus diesem Typ entfernt. (_Hinweis:_ Sie stehen weiterhin in der Eigenschaft `DefaultRequestOptions` zur Verfügung.)
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- Diese Änderung wirkt sich auf folgende Cmdlets aus:
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a>AzureStorageContainer.CloudBlobContainer.ServiceClient
- Folgende Eigenschaften wurden aus diesem Typ entfernt. (_Hinweis:_ Sie stehen weiterhin in der Eigenschaft `DefaultRequestOptions` zur Verfügung.)
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- Diese Änderung wirkt sich auf folgende Cmdlets aus:
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a>AzureStorageQueue.CloudQueue.ServiceClient
- Folgende Eigenschaften wurden aus diesem Typ entfernt. (_Hinweis:_ Sie stehen weiterhin in der Eigenschaft `DefaultRequestOptions` zur Verfügung.)
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- Diese Änderung wirkt sich auf folgende Cmdlets aus:
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a>AzureStorageTable.CloudTable.ServiceClient
- Folgende Eigenschaften wurden aus diesem Typ entfernt. (_Hinweis:_ Sie stehen weiterhin in der Eigenschaft `DefaultRequestOptions` zur Verfügung.)
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- Diese Änderung wirkt sich auf folgende Cmdlets aus:
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell-interactive
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode       
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode     
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a>Grundlegende Änderungen für Profile-Cmdlets

In dieser Version wurden folgende Cmdlets und Cmdlet-Ausgabetypen geändert:

### <a name="add-azurermaccount-breaking-changes"></a>Grundlegende Änderungen für „Add-AzureRmAccount“

- Der Parameter ```EnvironmentName``` wurde entfernt und durch ```Environment``` ersetzt. ```Environment``` akzeptiert nun eine Zeichenfolge anstelle eines Objekts vom Typ ```AzureEnvironment```.

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a>„Select-AzureRmProfile“ wurde in „Import-AzureRmContext“ umbenannt.

```Select-AzureRmProfile``` wurde in ```Import-AzureRmContext``` umbenannt.

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a>„Save-AzureRmProfile“ wurde in „Save-AzureRmContext“ umbenannt.

```Save-AzureRmProfile``` wurde in ```Save-AzureRmContext``` umbenannt.

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a>Grundlegende Änderungen für den Ausgabetyp „PSAzureContext“

- Die Eigenschaft ```TokenCache``` wurde in einen Typ geändert, der ```IAzureTokenCache``` (anstelle von ```byte[]```) implementiert.

```powershell-interactive
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a>Grundlegende Änderungen für den Ausgabetyp „PSAzureAccount“

- Die Eigenschaft ```AccountType``` wurde in ```Type``` geändert.

```powershell-interactive
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a>Grundlegende Änderungen für den Ausgabetyp „PSAzureSubscription“
- Die Eigenschaft ```SubscriptionId``` wurde in ```Id``` geändert.

```powershell-interactive
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- Die Eigenschaft ```SubscriptionName``` wurde in ```Name``` geändert.

```powershell-interactive
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a>Grundlegende Änderungen für den Ausgabetyp „PSAzureTenant“

- Die Eigenschaft ```TenantId``` wurde in ```Id``` geändert.

```powershell-interactive
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- Die Eigenschaft ```Domain``` wurde in ```Directory``` geändert.

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
