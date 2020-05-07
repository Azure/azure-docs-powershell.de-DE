---
title: Grundlegende Änderungen für Microsoft Azure PowerShell 5.0.0
description: Dieser Migrationsleitfaden enthält eine Liste mit grundlegenden Änderungen, die in Version 5 an Azure PowerShell vorgenommen wurden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: f8dc413a91876e53e62d25cc38ac3b3ef6afda8e
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534587"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a>Grundlegende Änderungen für Microsoft Azure PowerShell 5.0.0

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Dieses Dokument informiert über grundlegende Änderungen und fungiert als Migrationsleitfaden für Kunden mit Microsoft Azure PowerShell-Cmdlets. In den einzelnen Abschnitten werden jeweils der Grund für die grundlegende Änderung und der Migrationspfad des geringsten Widerstands beschrieben. Ausführlichen Kontext finden Sie unter der Pull-Anforderung für die jeweilige Änderung.

## <a name="table-of-contents"></a>Inhaltsverzeichnis

- [Grundlegende Änderungen für ApiManagement-Cmdlets](#breaking-changes-to-apimanagement-cmdlets)
- [Grundlegende Änderungen für Batch-Cmdlets](#breaking-changes-to-batch-cmdlets)
- [Grundlegende Änderungen für Compute-Cmdlets](#breaking-changes-to-compute-cmdlets)
- [Grundlegende Änderungen für EventHub-Cmdlets](#breaking-changes-to-eventhub-cmdlets)
- [Grundlegende Änderungen für Insights-Cmdlets](#breaking-changes-to-insights-cmdlets)
- [Grundlegende Änderungen für Network-Cmdlets](#breaking-changes-to-network-cmdlets)
- [Grundlegende Änderungen für Resources-Cmdlets](#breaking-changes-to-resources-cmdlets)
- [Grundlegende Änderungen für ServiceBus-Cmdlets](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Grundlegende Änderungen für ApiManagement-Cmdlets

### <a name="new-azurermapimanagementbackendproxy"></a>**New-AzureRmApiManagementBackendProxy**
- Die Parameter „UserName“ und „Password“ werden durch ein PSCredential-Objekt ersetzt.

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a>**New-AzureRmApiManagementUser**
- Der Parameter „Password“ wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a>**Set-AzureRmApiManagementUser**
- Der Parameter „Password“ wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a>Grundlegende Änderungen für Batch-Cmdlets

### <a name="new-azurebatchcertificate"></a>**New-AzureBatchCertificate**
- Der Parameter `Password` wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a>**New-AzureBatchComputeNodeUser**
- Der Parameter `Password` wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a>**Set-AzureRmBatchComputeNodeUser**
- Der Parameter `Password` wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a>**New-AzureBatchTask**
 - Der Switch `RunElevated` wurde entfernt und durch `UserIdentity` ersetzt.

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

Dies betrifft auch die Eigenschaft `RunElevated` für `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` und `PSJobReleaseTask`.

### <a name="psmultiinstancesettings"></a>**PSMultiInstanceSettings**

- Der Konstruktor `PSMultiInstanceSettings` akzeptiert anstelle eines erforderlichen `numberOfInstances`-Parameters und einen erforderlichen `coordinationCommandLine`-Parameter.

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a>**Get-AzureBatchTask**
 - Die Eigenschaft `RunElevated` für `PSCloudTask` wurde entfernt. Als Ersatz für `RunElevated` wurde die Eigenschaft `UserIdentity` hinzugefügt.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

Dies betrifft auch die Eigenschaft `RunElevated` für `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` und `PSJobReleaseTask`.

### <a name="multiple-types"></a>**Mehrere Typen**

- Die Eigenschaft `SchedulingError` für `PSExitConditions` wurde in `PreProcessingError` umbenannt.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a>**Mehrere Typen**

- Die Eigenschaft `SchedulingError` für `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` und `PSTaskExecutionInformation` wurde in `FailureInformation` umbenannt.
  - `FailureInformation` wird im Falle eines Aufgabenfehlers zurückgegeben. Dazu zählen alle vorherigen Planungsfehler sowie Exitcodes ungleich Null und Dateiuploadfehler aus dem neuen Ausgabedateienfeature.
  - Da die Struktur unverändert bleibt, sind zur Verwendung dieses Typs keine Codeänderungen erforderlich.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

Dies wirkt sich auch auf Folgendes aus: Get-AzureBatchPool, Get-AzureBatchSubtask und Get-AzureBatchJobPreparationAndReleaseTaskStatus

### <a name="new-azurebatchpool"></a>**New-AzureBatchPool**
 - `TargetDedicated` wurde entfernt und durch `TargetDedicatedComputeNodes` und `TargetLowPriorityComputeNodes` ersetzt.
 - `TargetDedicatedComputeNodes` besitzt einen Alias (`TargetDedicated`).

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

Dies wirkt sich auch auf Folgendes aus: Start-AzureBatchPoolResize

### <a name="get-azurebatchpool"></a>**Get-AzureBatchPool**
 - Die Eigenschaften `TargetDedicated` und `CurrentDedicated` für `PSCloudPool` wurden in `TargetDedicatedComputeNodes` und `CurrentDedicatedComputeNodes` umbenannt.

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a>**Typ „PSCloudPool“**

- `ResizeError` wurde für `PSCloudPool` in `ResizeErrors` umbenannt und ist nun eine Sammlung.

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a>**New-AzureBatchJob**
- Die Eigenschaft `TargetDedicated` für `PSPoolSpecification` wurde in `TargetDedicatedComputeNodes` umbenannt.

```powershell-interactive
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a>**Get-AzureBatchNodeFile**
 - `Name` wurde entfernt und durch `Path` ersetzt.
 - `Path` besitzt einen Alias (`Name`).

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

Dies wirkt sich auch auf Folgendes aus: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile

### <a name="type-psnodefile"></a>**Typ „PSNodeFile“**

 - Die Eigenschaft `Name` für `PSNodeFile` wurde in `Path` umbenannt.

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a>**Get-AzureBatchSubtask**
- Die Eigenschaften `PreviousState` und `State` von `PSSubtaskInformation` sind nicht mehr vom Typ `TaskState`, sondern vom Typ `SubtaskState`.
  - Im Gegensatz zu `TaskState` besitzt `SubtaskState` keinen Wert vom Typ `Active`, da sich Unteraufgaben nicht im Zustand `Active` befinden können.

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a>Grundlegende Änderungen für Compute-Cmdlets

### <a name="set-azurermvmaccessextension"></a>**Set-AzureRmVMAccessExtension**
- Die Parameter „UserName“ und „Password“ werden durch ein PSCredential-Objekt ersetzt.

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>Grundlegende Änderungen für EventHub-Cmdlets

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a>**New-AzureRmEventHubNamespaceAuthorizationRule**
- Das Cmdlet „New-AzureRmEventHubNamespaceAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „New-AzureRmEventHubAuthorizationRule“.
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a>**Get-AzureRmEventHubNamespaceAuthorizationRule**
- Das Cmdlet „Get-AzureRmEventHubNamespaceAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „Get-AzureRmEventHubAuthorizationRule“.
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a>**Set-AzureRmEventHubNamespaceAuthorizationRule**
- Das Cmdlet „Set-AzureRmEventHubNamespaceAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „Set-AzureRmEventHubAuthorizationRule“.
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a>**Remove-AzureRmEventHubNamespaceAuthorizationRule**
- Das Cmdlet „Remove-AzureRmEventHubNamespaceAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „Remove-AzureRmEventHubAuthorizationRule“.
    
### <a name="new-azurermeventhubnamespacekey"></a>**New-AzureRmEventHubNamespaceKey**
- Das Cmdlet „New-AzureRmEventHubNamespaceKey“ wurde entfernt. Verwenden Sie das Cmdlet „New-AzureRmEventHubKey“.
    
### <a name="get-azurermeventhubnamespacekey"></a>**Get-AzureRmEventHubNamespaceKey**
- Das Cmdlet „Get-AzureRmEventHubNamespaceKey“ wurde entfernt. Verwenden Sie das Cmdlet „Get-AzureRmEventHubKey“.
    
### <a name="new-azurermeventhubnamespace"></a>**New-AzureRmEventHubNamespace**
- Die Eigenschaften „Status“ und „Enabled“ aus den Namespaceattributen werden entfernt. 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a>**Get-AzureRmEventHubNamespace**
- Die Eigenschaften „Status“ und „Enabled“ aus den Namespaceattributen werden entfernt. 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a>**Set-AzureRmEventHubNamespace**
- Die Eigenschaften „Status“ und „Enabled“ aus den Namespaceattributen werden entfernt. 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a>**New-AzureRmEventHubConsumerGroup**
- Die Eigenschaft „EventHubPath“ aus den ConsumerGroup-Attributen wird entfernt.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a>**Set-AzureRmEventHubConsumerGroup**
- Die Eigenschaft „EventHubPath“ aus den ConsumerGroup-Attributen wird entfernt.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a>**Get-AzureRmEventHubConsumerGroup**
- Die Eigenschaft „EventHubPath“ aus den ConsumerGroup-Attributen wird entfernt.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a>Grundlegende Änderungen für Insights-Cmdlets

### <a name="add-azurermlogalertrule"></a>**Add-AzureRMLogAlertRule**
- Das Cmdlet **Add-AzureRMLogAlertRule** ist veraltet.
- Nach dem 1. Oktober hat die Verwendung dieses Cmdlets keine Wirkung mehr, da die Funktion in Aktivitätsprotokollwarnungen übertragen wurde. Unter https://aka.ms/migratemealerts finden Sie weitere Informationen.

### <a name="get-azurermusage"></a>**Get-AzureRMUsage**
- Das Cmdlet **Get-AzureRMUsage** ist veraltet.

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a>**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**
- Ausgabeänderung: Das Feld „EventChannels“ aus dem EventData-Objekt (das von diesen Cmdlets zurückgegeben wird) wird ausgemustert, da nun ein konstanter Wert (Administrator, Vorgang) zurückgegeben wird.

### <a name="get-azurermalertrule"></a>**Get-AzureRmAlertRule**
- Ausgabeänderung: Zur Verbesserung der Benutzerfreundlichkeit wird die Ausgabe dieses Cmdlets vereinfacht. (Das Eigenschaftenfeld wird entfernt.)

```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a>**Get-AzureRmAutoscaleSetting**
- Ausgabeänderung: Das Feld „AutoscaleSettingResourceName“ wird ausgemustert, da es immer dem Feld „Name“ entspricht.

```powershell-interactive
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a>**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**
- Ausgabeänderung: Die Art der Ausgabe wird geändert, um ein einzelnes Objekt mit der Anforderungs-ID und dem Statuscode zurückzugeben.

```powershell-interactive
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a>Grundlegende Änderungen für Network-Cmdlets

### <a name="add-azurermapplicationgatewaysslcertificate"></a>**Add-AzureRmApplicationGatewaySslCertificate**
- Der Parameter „Password“ wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a>**New-AzureRmApplicationGatewaySslCertificate**
- Der Parameter „Password“ wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a>**Set-AzureRmApplicationGatewaySslCertificate**
- Der Parameter „Password“ wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a>Grundlegende Änderungen für Resources-Cmdlets

### <a name="new-azurermadappcredential"></a>**New-AzureRmADAppCredential**
- Der Parameter „Password“ wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a>**New-AzureRmADApplication**
- Der Parameter „Password“ wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a>**New-AzureRmADServicePrincipal**
- Der Parameter „Password“ wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a>**New-AzureRmADSpCredential**
- Der Parameter „Password“ wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a>**New-AzureRmADUser**
- Der Parameter „Password“ wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a>**Set-AzureRmADUser**
- Der Parameter „Password“ wird durch ein SecureString-Objekt ersetzt.

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>Grundlegende Änderungen für ServiceBus-Cmdlets

### <a name="get-azurermservicebustopicauthorizationrule"></a>**Get-AzureRmServiceBusTopicAuthorizationRule**
- Das Cmdlet „Get-AzureRmServiceBusTopicAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „Get-AzureRmServiceBusAuthorizationRule“.    

### <a name="get-azurermservicebustopickey"></a>**Get-AzureRmServiceBusTopicKey**
- Das Cmdlet „Get-AzureRmServiceBusTopicKey“ wurde entfernt. Verwenden Sie das Cmdlet „Get-AzureRmServiceBusKey“.

### <a name="new-azurermservicebustopicauthorizationrule"></a>**New-AzureRmServiceBusTopicAuthorizationRule**
- Das Cmdlet „New-AzureRmServiceBusTopicAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „New-AzureRmServiceBusAuthorizationRule“.

### <a name="new-azurermservicebustopickey"></a>**New-AzureRmServiceBusTopicKey**
- Das Cmdlet „New-AzureRmServiceBusTopicKey“ wurde entfernt. Verwenden Sie das Cmdlet „New-AzureRmServiceBusKey“.

### <a name="remove-azurermservicebustopicauthorizationrule"></a>**Remove-AzureRmServiceBusTopicAuthorizationRule**
- Das Cmdlet „Remove-AzureRmServiceBusTopicAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „Remove-AzureRmServiceBusAuthorizationRule“.

### <a name="set-azurermservicebustopicauthorizationrule"></a>**Set-AzureRmServiceBusTopicAuthorizationRule**
- Das Cmdlet „Set-AzureRmServiceBusTopicAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „Set-AzureRmServiceBusAuthorizationRule“.

### <a name="new-azurermservicebusnamespacekey"></a>**New-AzureRmServiceBusNamespaceKey**
- Das Cmdlet „New-AzureRmServiceBusNamespaceKey“ wurde entfernt. Verwenden Sie das Cmdlet „New-AzureRmServiceBusKey“.

### <a name="get-azurermservicebusqueueauthorizationrule"></a>**Get-AzureRmServiceBusQueueAuthorizationRule**
- Das Cmdlet „Get-AzureRmServiceBusQueueAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „Get-AzureRmServiceBusAuthorizationRule“.

### <a name="get-azurermservicebusqueuekey"></a>**Get-AzureRmServiceBusQueueKey**
- Das Cmdlet „Get-AzureRmServiceBusQueueKey“ wurde entfernt. Verwenden Sie das Cmdlet „Get-AzureRmServiceBusKey“.

### <a name="new-azurermservicebusqueueauthorizationrule"></a>**New-AzureRmServiceBusQueueAuthorizationRule**
- Das Cmdlet „New-AzureRmServiceBusQueueAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „New-AzureRmServiceBusAuthorizationRule“.

### <a name="new-azurermservicebusqueuekey"></a>**New-AzureRmServiceBusQueueKey**
- Das Cmdlet „New-AzureRmServiceBusQueueKey“ wurde entfernt. Verwenden Sie das Cmdlet „New-AzureRmServiceBusKey“.

### <a name="remove-azurermservicebusqueueauthorizationrule"></a>**Remove-AzureRmServiceBusQueueAuthorizationRule**
- Das Cmdlet „Remove-AzureRmServiceBusQueueAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „Remove-AzureRmServiceBusAuthorizationRule“.

### <a name="set-azurermservicebusqueueauthorizationrule"></a>**Set-AzureRmServiceBusQueueAuthorizationRule**
- Das Cmdlet „Set-AzureRmServiceBusQueueAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „Set-AzureRmServiceBusAuthorizationRule“.

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a>**Get-AzureRmServiceBusNamespaceAuthorizationRule**
- Das Cmdlet „Get-AzureRmServiceBusNamespaceAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „Get-AzureRmServiceBusAuthorizationRule“.

### <a name="get-azurermservicebusnamespacekey"></a>**Get-AzureRmServiceBusNamespaceKey**
- Das Cmdlet „Get-AzureRmServiceBusNamespaceKey“ wurde entfernt. Verwenden Sie das Cmdlet „Get-AzureRmServiceBusKey“.

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a>**New-AzureRmServiceBusNamespaceAuthorizationRule**
- Das Cmdlet „New-AzureRmServiceBusNamespaceAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „New-AzureRmServiceBusAuthorizationRule“.

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a>**Remove-AzureRmServiceBusNamespaceAuthorizationRule**
- Das Cmdlet „Remove-AzureRmServiceBusNamespaceAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „Remove-AzureRmServiceBusAuthorizationRule“.

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a>**Set-AzureRmServiceBusNamespaceAuthorizationRule**
- Das Cmdlet „Set-AzureRmServiceBusNamespaceAuthorizationRule“ wurde entfernt. Verwenden Sie das Cmdlet „Set-AzureRmServiceBusAuthorizationRule“.

### <a name="type-namespaceattributes"></a>**Typ „NamespaceAttributes“**
- Folgende Eigenschaften wurden entfernt:
    - Aktiviert
    - Status
   
```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a>**Typ „QueueAttribute“**
- Folgende Eigenschaften werden als veraltet markiert:
    - EnableBatchedOperations
    - EntityAvailabilityStatus
    - IsAnonymousAccessible
    - SupportOrdering

```powershell-interactive
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a>**Typ „TopicAttribute“**
- Folgende Eigenschaften werden als veraltet markiert:
    - Standort
    - IsExpress
    - IsAnonymousAccessible
    - FilteringMessagesBeforePublishing
    - EnableSubscriptionPartitioning
    - EntityAvailabilityStatus

```powershell-interactive
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a>**Typ „SubscriptionAttribute“**
- Folgende Eigenschaften werden als veraltet markiert:
    - DeadLetteringOnFilterEvaluationExceptions
    - EntityAvailabilityStatus
    - IsReadOnly
    - Standort
   
```powershell-interactive
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```