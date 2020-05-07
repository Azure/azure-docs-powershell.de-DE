---
title: Paralleles Ausführen von Cmdlets mithilfe von PowerShell-Aufträgen
description: Hier erfahren Sie, wie Sie Cmdlets mithilfe des Parameters „-AsJob“ parallel ausführen.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: d2ffd6cc4c5e70c53ab60b1280384faac9b45867
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534726"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a>Paralleles Ausführen von Cmdlets mithilfe von PowerShell-Aufträgen

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

PowerShell unterstützt asynchrone Aktionen mit [PowerShell-Aufträgen](/powershell/module/microsoft.powershell.core/about/about_jobs).
Azure PowerShell muss häufig Netzwerkaufrufe an Azure senden und anschließend warten. Als Entwickler versuchen Sie unter Umständen häufig, mehrere nicht blockierende Aufrufe von Azure in einem Skript auszuführen, oder Sie möchten Azure-Ressourcen in der REPL erstellen, ohne die aktuelle Sitzung zu blockieren. Azure PowerShell bietet erstklassige Unterstützung für [PS-Aufträge](/powershell/module/microsoft.powershell.core/about/about_jobs), um diese Anforderungen zu erfüllen.

## <a name="context-persistence-and-psjobs"></a>Kontextpersistenz und PS-Aufträge

PowerShell-Aufträge werden in separaten Prozessen ausgeführt. Das bedeutet, dass Informationen zu Ihrer Azure-Verbindung ordnungsgemäß für die von Ihnen erstellten Aufträge freigegeben werden müssen. Beim Herstellen einer Verbindung zwischen Ihrem Azure-Konto und der PowerShell-Sitzung mit `Connect-AzureRmAccount` können Sie den Kontext an einen Auftrag übergeben.

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

Wenn Sie jedoch festgelegt haben, dass der Kontext automatisch mit `Enable-AzureRmContextAutosave` gespeichert wird, wird er automatisch für alle von Ihnen erstellten Aufträge freigegeben.

```azurepowershell-interactive
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a>Automatische Aufträge mit `-AsJob`

Zur Vereinfachung steht in Azure PowerShell außerdem ein `-AsJob`-Switch für einige Cmdlets mit langer Ausführungsdauer zur Verfügung.
Der `-AsJob`-Switch macht die Erstellung von PS-Aufträgen noch einfacher.

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

Sie können den Auftrag und den Status jederzeit mit `Get-Job` und `Get-AzureRmVM` überprüfen.

```azurepowershell-interactive
Get-Job $job
Get-AzureRmVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

Anschließend können Sie nach Abschluss des Vorgangs das Ergebnis des Auftrags mit `Receive-Job` abrufen.

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

Erstellen Sie mehrere virtuelle Computer auf einmal.

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzureRmVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzureRmVM
```

In diesem Beispiel führt das Cmdlet `Wait-Job` dazu, dass das Skript während der Ausführung von Aufträgen angehalten wird. Die Ausführung des Skripts wird fortgesetzt, wenn alle Aufträge abgeschlossen sind. Dadurch ist es möglich, mehrere Aufträge zu erstellen, die parallel ausgeführt werden, und auf ihren Abschluss zu warten, bevor der Vorgang fortgesetzt wird.

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
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
