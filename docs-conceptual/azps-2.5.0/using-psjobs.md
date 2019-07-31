---
title: Paralleles Ausführen von Cmdlets mithilfe von PowerShell-Aufträgen
description: Hier erfahren Sie, wie Sie Cmdlets mithilfe des Parameters „-AsJob“ parallel ausführen.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 825a07e01194a07b747712a62384c7f162e63d7d
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657874"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a>Paralleles Ausführen von Cmdlets mithilfe von PowerShell-Aufträgen

PowerShell unterstützt asynchrone Aktionen mit [PowerShell-Aufträgen](/powershell/module/microsoft.powershell.core/about/about_jobs).
Azure PowerShell muss häufig Netzwerkaufrufe an Azure senden und anschließend warten. Es kann häufig vorkommen, dass Sie nicht blockierende Aufrufe durchführen müssen. Azure PowerShell verfügt über erstklassige [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs)-Unterstützung, um diese Anforderung zu erfüllen.

## <a name="context-persistence-and-psjobs"></a>Kontextpersistenz und PS-Aufträge

Da PS-Aufträge (PSJobs) als separate Prozesse ausgeführt werden, muss Ihre Azure-Verbindung dafür freigegeben werden. Nachdem Sie sich mit `Connect-AzAccount` an Ihrem Azure-Konto angemeldet haben, können Sie den Kontext an einen Auftrag übergeben.

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList (Get-AzContext),$creds
```

Wenn Sie jedoch festgelegt haben, dass der Kontext automatisch mit `Enable-AzContextAutosave` gespeichert wird, wird er automatisch für alle von Ihnen erstellten Aufträge freigegeben.

```azurepowershell-interactive
Enable-AzContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin} -ArgumentList $creds
```

## <a name="automatic-jobs-with--asjob"></a>Automatische Aufträge mit `-AsJob`

Zur Vereinfachung steht in Azure PowerShell außerdem ein `-AsJob`-Switch für einige Cmdlets mit langer Ausführungsdauer zur Verfügung.
Der `-AsJob`-Switch macht die Erstellung von PS-Aufträgen noch einfacher.

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzVM -Name MyVm -Credential $creds -AsJob
```

Sie können den Auftrag und den Status jederzeit mit `Get-Job` und `Get-AzVM` überprüfen.

```azurepowershell-interactive
Get-Job $job
Get-AzVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzVM' AzureLongRunningJob`1 Running True        localhost New-AzVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

Nach Abschluss des Auftrags rufen Sie das Ergebnis des Auftrags mit `Receive-Job` ab.

> [!NOTE]
> `Receive-Job` gibt das Ergebnis vom Cmdlet so zurück, als wäre das Flag `-AsJob` nicht vorhanden.
> Beispiel: Das Ergebnis `Receive-Job` von `Do-Action -AsJob` ist vom gleichen Typ wie das Ergebnis von `Do-Action`.

```azurepowershell-interactive
$vm = Receive-Job $job
$vm
```

```output
ResourceGroupName        : MyVm
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyVm/providers/Microsoft.Compute/virtualMachines/MyVm
VmId                     : dff1f79e-a8f7-4664-ab72-0ec28b9fbb5b
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvmmyvm.eastus.cloudapp.azure.com
```

## <a name="example-scenarios"></a>Beispielszenarien

Gleichzeitiges Erstellen mehrerer virtueller Computer:

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzVM
```

In diesem Beispiel führt das Cmdlet `Wait-Job` dazu, dass das Skript während der Ausführung von Aufträgen angehalten wird. Die Ausführung des Skripts wird fortgesetzt, wenn alle Aufträge abgeschlossen sind. Mehrere Aufträge werden gleichzeitig ausgeführt, und dann wartet das Skript auf deren Abschluss, bevor fortgefahren wird.

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
All Jobs completed.

ResourceGroupName        Name   Location          VmSize  OsType           NIC ProvisioningState Zone
-----------------        ----   --------          ------  ------           --- ----------------- ----
MYVM                     MyVm     eastus Standard_DS1_v2 Windows          MyVm         Succeeded
MYVM0                   MyVm0     eastus Standard_DS1_v2 Windows         MyVm0         Succeeded
MYVM1                   MyVm1     eastus Standard_DS1_v2 Windows         MyVm1         Succeeded
MYVM2                   MyVm2     eastus Standard_DS1_v2 Windows         MyVm2         Succeeded
MYVM3                   MyVm3     eastus Standard_DS1_v2 Windows         MyVm3         Succeeded
MYVM4                   MyVm4     eastus Standard_DS1_v2 Windows         MyVm4         Succeeded
MYVM5                   MyVm5     eastus Standard_DS1_v2 Windows         MyVm5         Succeeded
MYVM6                   MyVm6     eastus Standard_DS1_v2 Windows         MyVm6         Succeeded
MYVM7                   MyVm7     eastus Standard_DS1_v2 Windows         MyVm7         Succeeded
MYVM8                   MyVm8     eastus Standard_DS1_v2 Windows         MyVm8         Succeeded
MYVM9                   MyVm9     eastus Standard_DS1_v2 Windows         MyVm9         Succeeded
```
