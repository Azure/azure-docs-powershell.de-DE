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
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052514"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="34f99-103">Paralleles Ausführen von Cmdlets mithilfe von PowerShell-Aufträgen</span><span class="sxs-lookup"><span data-stu-id="34f99-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="34f99-104">PowerShell unterstützt asynchrone Aktionen mit [PowerShell-Aufträgen](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="34f99-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="34f99-105">Azure PowerShell muss häufig Netzwerkaufrufe an Azure senden und anschließend warten.</span><span class="sxs-lookup"><span data-stu-id="34f99-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="34f99-106">Es kann häufig vorkommen, dass Sie nicht blockierende Aufrufe durchführen müssen.</span><span class="sxs-lookup"><span data-stu-id="34f99-106">You may often find yourself needing to make non-blocking calls.</span></span> <span data-ttu-id="34f99-107">Azure PowerShell verfügt über erstklassige [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs)-Unterstützung, um diese Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="34f99-107">To address this need, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="34f99-108">Kontextpersistenz und PS-Aufträge</span><span class="sxs-lookup"><span data-stu-id="34f99-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="34f99-109">Da PS-Aufträge (PSJobs) als separate Prozesse ausgeführt werden, muss Ihre Azure-Verbindung dafür freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="34f99-109">Since PSJobs are run as separate processes, your Azure connection must be shared with them.</span></span> <span data-ttu-id="34f99-110">Nachdem Sie sich mit `Connect-AzAccount` an Ihrem Azure-Konto angemeldet haben, können Sie den Kontext an einen Auftrag übergeben.</span><span class="sxs-lookup"><span data-stu-id="34f99-110">After signing in to your Azure account with `Connect-AzAccount`, pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList (Get-AzContext),$creds
```

<span data-ttu-id="34f99-111">Wenn Sie jedoch festgelegt haben, dass der Kontext automatisch mit `Enable-AzContextAutosave` gespeichert wird, wird er automatisch für alle von Ihnen erstellten Aufträge freigegeben.</span><span class="sxs-lookup"><span data-stu-id="34f99-111">However, if you have chosen to have your context automatically saved with `Enable-AzContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin} -ArgumentList $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="34f99-112">Automatische Aufträge mit `-AsJob`</span><span class="sxs-lookup"><span data-stu-id="34f99-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="34f99-113">Zur Vereinfachung steht in Azure PowerShell außerdem ein `-AsJob`-Switch für einige Cmdlets mit langer Ausführungsdauer zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="34f99-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="34f99-114">Der `-AsJob`-Switch macht die Erstellung von PS-Aufträgen noch einfacher.</span><span class="sxs-lookup"><span data-stu-id="34f99-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="34f99-115">Sie können den Auftrag und den Status jederzeit mit `Get-Job` und `Get-AzVM` überprüfen.</span><span class="sxs-lookup"><span data-stu-id="34f99-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzVM`.</span></span>

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

<span data-ttu-id="34f99-116">Nach Abschluss des Auftrags rufen Sie das Ergebnis des Auftrags mit `Receive-Job` ab.</span><span class="sxs-lookup"><span data-stu-id="34f99-116">When the job completes, get the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="34f99-117">`Receive-Job` gibt das Ergebnis vom Cmdlet so zurück, als wäre das Flag `-AsJob` nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="34f99-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="34f99-118">Beispiel: Das Ergebnis `Receive-Job` von `Do-Action -AsJob` ist vom gleichen Typ wie das Ergebnis von `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="34f99-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

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

## <a name="example-scenarios"></a><span data-ttu-id="34f99-119">Beispielszenarien</span><span class="sxs-lookup"><span data-stu-id="34f99-119">Example Scenarios</span></span>

<span data-ttu-id="34f99-120">Gleichzeitiges Erstellen mehrerer virtueller Computer:</span><span class="sxs-lookup"><span data-stu-id="34f99-120">Create several VMs at once:</span></span>

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

<span data-ttu-id="34f99-121">In diesem Beispiel führt das Cmdlet `Wait-Job` dazu, dass das Skript während der Ausführung von Aufträgen angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="34f99-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="34f99-122">Die Ausführung des Skripts wird fortgesetzt, wenn alle Aufträge abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="34f99-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="34f99-123">Mehrere Aufträge werden gleichzeitig ausgeführt, und dann wartet das Skript auf deren Abschluss, bevor fortgefahren wird.</span><span class="sxs-lookup"><span data-stu-id="34f99-123">Several jobs run in parallel then the script waits for completion before continuing.</span></span>

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
