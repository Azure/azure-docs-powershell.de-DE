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
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "67863556"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="bbe95-103">Grundlegende Änderungen für Microsoft Azure PowerShell 4.0.0</span><span class="sxs-lookup"><span data-stu-id="bbe95-103">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="bbe95-104">Dieses Dokument informiert über grundlegende Änderungen und fungiert als Migrationsleitfaden für Kunden mit Microsoft Azure PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="bbe95-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="bbe95-105">In den einzelnen Abschnitten werden jeweils der Grund für die grundlegende Änderung und der Migrationspfad des geringsten Widerstands beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bbe95-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="bbe95-106">Ausführlichen Kontext finden Sie unter der Pull-Anforderung für die jeweilige Änderung.</span><span class="sxs-lookup"><span data-stu-id="bbe95-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="bbe95-107">Inhaltsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="bbe95-107">Table of Contents</span></span>

- [<span data-ttu-id="bbe95-108">Grundlegende Änderungen für Compute-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="bbe95-109">Grundlegende Änderungen für EventHub-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="bbe95-110">Grundlegende Änderungen für Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="bbe95-111">Grundlegende Änderungen für Network-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="bbe95-112">Grundlegende Änderungen für ServiceBus-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-112">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="bbe95-113">Grundlegende Änderungen für Sql-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-113">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="bbe95-114">Grundlegende Änderungen für Storage-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-114">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="bbe95-115">Grundlegende Änderungen für Profile-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-115">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="bbe95-116">Grundlegende Änderungen für Compute-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-116">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="bbe95-117">Diese Version hat Auswirkungen auf folgende Ausgabetypen:</span><span class="sxs-lookup"><span data-stu-id="bbe95-117">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="bbe95-118">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bbe95-118">PSVirtualMachine</span></span>
- <span data-ttu-id="bbe95-119">Die übergeordneten Eigenschaften `DataDiskNames` und `NetworkInterfaceIDs` des Objekts `PSVirtualMachine` wurden aus dem Ausgabetyp entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-119">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="bbe95-120">Diese Eigenschaften waren schon immer in den Eigenschaften `StorageProfile` und `NetworkProfile` des Objekts `PSVirtualMachine` verfügbar und müssen fortan für den Zugriff auf die Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bbe95-120">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="bbe95-121">Diese Änderung wirkt sich auf folgende Cmdlets aus:</span><span class="sxs-lookup"><span data-stu-id="bbe95-121">This change affects the following cmdlets:</span></span>
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

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="bbe95-122">Grundlegende Änderungen für EventHub-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-122">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="bbe95-123">Diese Version hat Auswirkungen auf folgende Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbe95-123">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="bbe95-124">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="bbe95-124">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="bbe95-125">Die Eigenschaft `ResourceGroupName` wurde aus dem Ausgabetyp `NamespaceAttributes` entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="bbe95-126">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="bbe95-126">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="bbe95-127">Die Eigenschaft `ResourceGroupName` wurde aus dem Ausgabetyp `NamespaceAttributes` entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-127">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="bbe95-128">Grundlegende Änderungen für Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-128">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="bbe95-129">Diese Version hat Auswirkungen auf folgende Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbe95-129">The following cmdlets were affected this release:</span></span>
    
### <a name="get-azurermusage"></a><span data-ttu-id="bbe95-130">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="bbe95-130">Get-AzureRmUsage</span></span>
- <span data-ttu-id="bbe95-131">Dieses Cmdlet ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="bbe95-131">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="bbe95-132">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="bbe95-132">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="bbe95-133">Die Ausgabe dieses Cmdlets wurde von einer Liste mit einem einzelnen Objekt in ein einzelnes Objekt geändert, das die Anforderungs-ID und den Statuscode enthält.</span><span class="sxs-lookup"><span data-stu-id="bbe95-133">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>
    
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
    
### <a name="add-azurermlogalertrule"></a><span data-ttu-id="bbe95-134">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="bbe95-134">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="bbe95-135">Dieses Cmdlet ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="bbe95-135">This cmdlet has been deprecated.</span></span>
    
### <a name="get-azurermalertrule"></a><span data-ttu-id="bbe95-136">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="bbe95-136">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="bbe95-137">Jedes Element der Ausgabe dieses Cmdlets (eine Liste mit Objekten) wird vereinfacht. Anstelle von Objekten mit der Struktur `{ Id, Location, Name, Tags, Properties }` werden also Objekte mit der Struktur `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}` zurückgegeben. Diese umfasst alle Attribute einer Azure-Ressource sowie alle Attribute eines AlertRuleResource-Objekts auf der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="bbe95-137">Each element of the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>
    
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
    
### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="bbe95-138">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="bbe95-138">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="bbe95-139">Das Feld `AutoscaleSettingResourceName` ist veraltet, da es immer denselben Wert besitzt wie das Feld `Name`.</span><span class="sxs-lookup"><span data-stu-id="bbe95-139">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

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
    
### <a name="remove-azurermlogprofile"></a><span data-ttu-id="bbe95-140">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="bbe95-140">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="bbe95-141">Die Ausgabe dieses Cmdlets ändert sich von `Boolean` in ein Objekt mit `RequestId` und `StatusCode`.</span><span class="sxs-lookup"><span data-stu-id="bbe95-141">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

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
    
### <a name="add-azurermlogprofile"></a><span data-ttu-id="bbe95-142">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="bbe95-142">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="bbe95-143">Die Ausgabe dieses Cmdlets ändert sich von einem Objekt mit Anforderungs-ID, Statuscode und aktualisierter oder neu erstellter Ressource.</span><span class="sxs-lookup"><span data-stu-id="bbe95-143">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>
    
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
    
### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="bbe95-144">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="bbe95-144">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="bbe95-145">Der Befehl wird in `Update-AzureRmDiagnosticSettings` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-145">The command is going to be renamed to `Update-AzureRmDiagnosticSettings`</span></span>

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="bbe95-146">Grundlegende Änderungen für Network-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-146">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="bbe95-147">Diese Version hat Auswirkungen auf folgende Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbe95-147">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="bbe95-148">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bbe95-148">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="bbe95-149">Der Parameter `EnableBgp` wurde geändert und akzeptiert nun einen Wert vom Typ `boolean` anstelle eines Werts vom Typ `string`.</span><span class="sxs-lookup"><span data-stu-id="bbe95-149">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="bbe95-150">Grundlegende Änderungen für ServiceBus-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-150">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="bbe95-151">Diese Version hat Auswirkungen auf folgende Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbe95-151">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="bbe95-152">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="bbe95-152">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="bbe95-153">Die Eigenschaft `ResourceGroupName` wurde aus dem Ausgabetyp `NamespaceAttributes` entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="bbe95-154">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="bbe95-154">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="bbe95-155">Die Eigenschaft `ResourceGroupName` wurde aus dem Ausgabetyp `NamespaceAttributes` entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-155">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="bbe95-156">Grundlegende Änderungen für Sql-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-156">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="bbe95-157">Diese Version hat Auswirkungen auf folgende Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbe95-157">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="bbe95-158">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bbe95-158">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="bbe95-159">Der Parameter `Tag` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-159">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="bbe95-160">Der Parameter `GracePeriodWithDataLossHour` wurde in `GracePeriodWithDataLossHours` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-160">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="bbe95-161">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bbe95-161">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="bbe95-162">Der Parameter `Tag` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-162">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="bbe95-163">Der Parameter `GracePeriodWithDataLossHour` wurde in `GracePeriodWithDataLossHours` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-163">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="bbe95-164">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bbe95-164">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="bbe95-165">Der Parameter `Tag` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-165">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="bbe95-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bbe95-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="bbe95-167">Der Parameter `Tag` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-167">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="bbe95-168">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bbe95-168">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="bbe95-169">Der Parameter `PartnerResourceGroupName` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-169">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="bbe95-170">Der Parameter `PartnerServerName` wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-170">`PartnerServerName` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="bbe95-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bbe95-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="bbe95-172">Der Wert `Usage_Anomaly` ist für den Parameter `ExcludedDetectionType` nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="bbe95-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="bbe95-173">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bbe95-173">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="bbe95-174">Der Wert `Usage_Anomaly` ist für den Parameter `ExcludedDetectionType` nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="bbe95-174">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="bbe95-175">Grundlegende Änderungen für Storage-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-175">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="bbe95-176">Diese Version hat Auswirkungen auf folgende Ausgabetypeigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bbe95-176">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="bbe95-177">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="bbe95-177">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="bbe95-178">Folgende Eigenschaften wurden aus diesem Typ entfernt. (_Hinweis:_ Sie stehen weiterhin in der Eigenschaft `DefaultRequestOptions` zur Verfügung.)</span><span class="sxs-lookup"><span data-stu-id="bbe95-178">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="bbe95-179">Diese Änderung wirkt sich auf folgende Cmdlets aus:</span><span class="sxs-lookup"><span data-stu-id="bbe95-179">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="bbe95-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="bbe95-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="bbe95-181">Folgende Eigenschaften wurden aus diesem Typ entfernt. (_Hinweis:_ Sie stehen weiterhin in der Eigenschaft `DefaultRequestOptions` zur Verfügung.)</span><span class="sxs-lookup"><span data-stu-id="bbe95-181">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="bbe95-182">Diese Änderung wirkt sich auf folgende Cmdlets aus:</span><span class="sxs-lookup"><span data-stu-id="bbe95-182">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="bbe95-183">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="bbe95-183">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="bbe95-184">Folgende Eigenschaften wurden aus diesem Typ entfernt. (_Hinweis:_ Sie stehen weiterhin in der Eigenschaft `DefaultRequestOptions` zur Verfügung.)</span><span class="sxs-lookup"><span data-stu-id="bbe95-184">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="bbe95-185">Diese Änderung wirkt sich auf folgende Cmdlets aus:</span><span class="sxs-lookup"><span data-stu-id="bbe95-185">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="bbe95-186">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="bbe95-186">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="bbe95-187">Folgende Eigenschaften wurden aus diesem Typ entfernt. (_Hinweis:_ Sie stehen weiterhin in der Eigenschaft `DefaultRequestOptions` zur Verfügung.)</span><span class="sxs-lookup"><span data-stu-id="bbe95-187">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="bbe95-188">Diese Änderung wirkt sich auf folgende Cmdlets aus:</span><span class="sxs-lookup"><span data-stu-id="bbe95-188">This change affects the following cmdlets:</span></span>
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

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="bbe95-189">Grundlegende Änderungen für Profile-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbe95-189">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="bbe95-190">In dieser Version wurden folgende Cmdlets und Cmdlet-Ausgabetypen geändert:</span><span class="sxs-lookup"><span data-stu-id="bbe95-190">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="bbe95-191">Grundlegende Änderungen für „Add-AzureRmAccount“</span><span class="sxs-lookup"><span data-stu-id="bbe95-191">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="bbe95-192">Der Parameter ```EnvironmentName``` wurde entfernt und durch ```Environment``` ersetzt. ```Environment``` akzeptiert nun eine Zeichenfolge anstelle eines Objekts vom Typ ```AzureEnvironment```.</span><span class="sxs-lookup"><span data-stu-id="bbe95-192">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="bbe95-193">„Select-AzureRmProfile“ wurde in „Import-AzureRmContext“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-193">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="bbe95-194">```Select-AzureRmProfile``` wurde in ```Import-AzureRmContext``` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-194">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="bbe95-195">„Save-AzureRmProfile“ wurde in „Save-AzureRmContext“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-195">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="bbe95-196">```Save-AzureRmProfile``` wurde in ```Save-AzureRmContext``` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bbe95-196">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="bbe95-197">Grundlegende Änderungen für den Ausgabetyp „PSAzureContext“</span><span class="sxs-lookup"><span data-stu-id="bbe95-197">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="bbe95-198">Die Eigenschaft ```TokenCache``` wurde in einen Typ geändert, der ```IAzureTokenCache``` (anstelle von ```byte[]```) implementiert.</span><span class="sxs-lookup"><span data-stu-id="bbe95-198">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

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

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="bbe95-199">Grundlegende Änderungen für den Ausgabetyp „PSAzureAccount“</span><span class="sxs-lookup"><span data-stu-id="bbe95-199">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="bbe95-200">Die Eigenschaft ```AccountType``` wurde in ```Type``` geändert.</span><span class="sxs-lookup"><span data-stu-id="bbe95-200">The ```AccountType``` property was changed to ```Type```</span></span>

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

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="bbe95-201">Grundlegende Änderungen für den Ausgabetyp „PSAzureSubscription“</span><span class="sxs-lookup"><span data-stu-id="bbe95-201">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="bbe95-202">Die Eigenschaft ```SubscriptionId``` wurde in ```Id``` geändert.</span><span class="sxs-lookup"><span data-stu-id="bbe95-202">The ```SubscriptionId``` property was changed to ```Id```</span></span>

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

- <span data-ttu-id="bbe95-203">Die Eigenschaft ```SubscriptionName``` wurde in ```Name``` geändert.</span><span class="sxs-lookup"><span data-stu-id="bbe95-203">The ```SubscriptionName``` property was changed to ```Name```</span></span>

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

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="bbe95-204">Grundlegende Änderungen für den Ausgabetyp „PSAzureTenant“</span><span class="sxs-lookup"><span data-stu-id="bbe95-204">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="bbe95-205">Die Eigenschaft ```TenantId``` wurde in ```Id``` geändert.</span><span class="sxs-lookup"><span data-stu-id="bbe95-205">The ```TenantId``` property was changed to ```Id```</span></span>

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

- <span data-ttu-id="bbe95-206">Die Eigenschaft ```Domain``` wurde in ```Directory``` geändert.</span><span class="sxs-lookup"><span data-stu-id="bbe95-206">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
