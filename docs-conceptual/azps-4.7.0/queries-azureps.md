---
title: Abfragen der Ausgabe von Azure PowerShell-Cmdlets
description: Hier erfahren Sie, wie Sie in Azure Ressourcenabfragen ausführen und die Ergebnisse formatieren.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2754df5132ca9d528217fa5caad95b7f59cc8215
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "90928132"
---
# <a name="query-output-of-azure-powershell"></a><span data-ttu-id="01b5f-103">Abfrageausgabe von Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="01b5f-103">Query output of Azure PowerShell</span></span> 

<span data-ttu-id="01b5f-104">Das Ergebnis eines Azure PowerShell-Cmdlets ist ein Azure PowerShell-Objekt.</span><span class="sxs-lookup"><span data-stu-id="01b5f-104">The results of each Azure PowerShell cmdlet are an Azure PowerShell object.</span></span> <span data-ttu-id="01b5f-105">Auch Cmdlets, die keine expliziten `Get-`-Vorgänge sind, können einen Wert zurückgeben, der überprüft werden kann, um Informationen zu einer erstellten oder geänderten Ressource zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="01b5f-105">Even cmdlets that aren't explicitly `Get-` operations might return a value that can be inspected, to give information about a resource that was created or modified.</span></span> <span data-ttu-id="01b5f-106">Die meisten Cmdlets geben ein einzelnes Objekt zurück. Manche Cmdlets geben jedoch ein Array zurück, das durchlaufen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="01b5f-106">While most cmdlets return a single object, some return an array that should be iterated through.</span></span>

<span data-ttu-id="01b5f-107">In fast allen Fällen wird die Abfrageausgabe von Azure PowerShell mit dem Cmdlet [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) zu `select` abgekürzt.</span><span class="sxs-lookup"><span data-stu-id="01b5f-107">In almost all cases, you query output from Azure PowerShell with the [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet, often abbreviated to `select`.</span></span> <span data-ttu-id="01b5f-108">Die Ausgabe kann mit [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) oder dem entsprechenden Alias `where` gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="01b5f-108">Output can be filtered with [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), or its alias `where`.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="01b5f-109">Auswählen einfacher Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="01b5f-109">Select simple properties</span></span>

<span data-ttu-id="01b5f-110">Im Standardtabellenformat zeigen Azure PowerShell-Cmdlets nicht alle verfügbaren Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="01b5f-110">In the default table format, Azure PowerShell cmdlets don't display all of their available properties.</span></span> <span data-ttu-id="01b5f-111">Sie können die vollständigen Eigenschaften mithilfe des Cmdlets [Format-List](/powershell/module/microsoft.powershell.utility/format-list) oder durch Weiterleiten der Ausgabe an `Select-Object *` abrufen:</span><span class="sxs-lookup"><span data-stu-id="01b5f-111">You can get the full properties by using the [Format-List](/powershell/module/microsoft.powershell.utility/format-list) cmdlet, or by piping output to `Select-Object *`:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

<span data-ttu-id="01b5f-112">Wenn Ihnen die Namen der für Sie relevanten Eigenschaften bekannt sind, können Sie diese Eigenschaftennamen mit `Select-Object` verwenden, um sie direkt abzurufen:</span><span class="sxs-lookup"><span data-stu-id="01b5f-112">Once you know the names of the properties that you're interested in, you can use those property names with `Select-Object` to get them directly:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

<span data-ttu-id="01b5f-113">Die Ausgabe für `Select-Object` ist immer zur Anzeige der angeforderten Informationen formatiert.</span><span class="sxs-lookup"><span data-stu-id="01b5f-113">Output from using `Select-Object` is always formatted to display the requested information.</span></span> <span data-ttu-id="01b5f-114">Informationen zur Verwendung der Formatierung beim Abfragen von Cmdlet-Ergebnissen finden Sie unter [Format Azure PowerShell cmdlet output](formatting-output.md) (Formatieren der Ausgabe von Azure PowerShell-Cmdlets).</span><span class="sxs-lookup"><span data-stu-id="01b5f-114">To learn about using formatting as part of querying cmdlet results, see [Format Azure PowerShell cmdlet output](formatting-output.md).</span></span>

## <a name="select-nested-properties"></a><span data-ttu-id="01b5f-115">Auswählen geschachtelter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="01b5f-115">Select nested properties</span></span>

<span data-ttu-id="01b5f-116">Einige Eigenschaften in der Ausgabe von Azure PowerShell-Cmdlets verwenden geschachtelte Objekte, z. B. die `StorageProfile`-Eigenschaft der Ausgabe von `Get-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="01b5f-116">Some properties in Azure PowerShell cmdlet output use nested objects, like the `StorageProfile` property of `Get-AzVM` output.</span></span> <span data-ttu-id="01b5f-117">Um einen Wert aus einer geschachtelten Eigenschaft abzurufen, geben Sie einen Anzeigenamen und den vollständigen Pfad des Werts an, den Sie als Teil eines Wörterbucharguments für `Select-Object` überprüfen möchten:</span><span class="sxs-lookup"><span data-stu-id="01b5f-117">To get a value from a nested property, provide a display name and the full path to the value you want to inspect as part of a dictionary argument to `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

<span data-ttu-id="01b5f-118">Jedes Wörterbuchargument wählt eine Eigenschaft des Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="01b5f-118">Each dictionary argument selects one property from the object.</span></span> <span data-ttu-id="01b5f-119">Die zu extrahierende Eigenschaft muss Teil eines Ausdrucks sein.</span><span class="sxs-lookup"><span data-stu-id="01b5f-119">The property to extract must be part of an expression.</span></span>

## <a name="filter-results"></a><span data-ttu-id="01b5f-120">Ergebnisse filtern</span><span class="sxs-lookup"><span data-stu-id="01b5f-120">Filter results</span></span> 

<span data-ttu-id="01b5f-121">Mit dem Cmdlet `Where-Object` können Sie das Ergebnis auf der Grundlage eines beliebigen Eigenschaftswerts filtern (einschließlich geschachtelter Eigenschaften).</span><span class="sxs-lookup"><span data-stu-id="01b5f-121">The `Where-Object` cmdlet allows you to filter the result based on any property value, including nested properties.</span></span> <span data-ttu-id="01b5f-122">Das nächste Beispiel zeigt, wie Sie mit `Where-Object` nach den Linux-VMs in einer Ressourcengruppe suchen.</span><span class="sxs-lookup"><span data-stu-id="01b5f-122">The next example shows how to use `Where-Object` to find the Linux VMs in a resource group.</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

<span data-ttu-id="01b5f-123">Die Ergebnisse von `Select-Object` und `Where-Object` können aneinander weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="01b5f-123">You can pipe the results of `Select-Object` and `Where-Object` to each other.</span></span> <span data-ttu-id="01b5f-124">Aus Leistungsgründen wird empfohlen, den `Where-Object`-Vorgang immer vor `Select-Object` zu platzieren:</span><span class="sxs-lookup"><span data-stu-id="01b5f-124">For performance purposes, it's always recommended to put the `Where-Object` operation before `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```
