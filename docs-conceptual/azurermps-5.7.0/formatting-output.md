---
title: Formatieren der Ausgabe von Azure PowerShell-Cmdlets
description: Anleitung zum Formatieren der Cmdlet-Ausgabe für Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/07/2018
ms.openlocfilehash: 982073768a04bf31c14f9e89665822014cb72a9e
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534746"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="c0704-103">Formatieren der Ausgabe von Azure PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c0704-103">Format AzurePowerShell cmdlet output</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="c0704-104">Zur besseren Lesbarkeit der Ausgabe verfügt jedes Azure PowerShell-Cmdlet standardmäßig über eine vordefinierte Formatierung.</span><span class="sxs-lookup"><span data-stu-id="c0704-104">By default each Azure PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="c0704-105">Mit PowerShell ist es jedoch auch möglich, die Ausgabe anzupassen oder die Cmdlet-Ausgabe in ein anderes Format zu konvertieren. Hierzu stehen folgende Cmdlets zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="c0704-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="c0704-106">Formatierung</span><span class="sxs-lookup"><span data-stu-id="c0704-106">Formatting</span></span>      | <span data-ttu-id="c0704-107">Konvertierung</span><span class="sxs-lookup"><span data-stu-id="c0704-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="c0704-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="c0704-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="c0704-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="c0704-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="c0704-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="c0704-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="c0704-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="c0704-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="c0704-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="c0704-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="c0704-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="c0704-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="c0704-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="c0704-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="c0704-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="c0704-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a><span data-ttu-id="c0704-116">Formatbeispiele</span><span class="sxs-lookup"><span data-stu-id="c0704-116">Format examples</span></span>

<span data-ttu-id="c0704-117">In diesem Beispiel rufen wir eine Liste mit virtuellen Azure-Computern in unserem Standardabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="c0704-117">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="c0704-118">Bei dem Befehl `Get-AzureRmVM` erfolgt die Ausgabe standardmäßig in einem Tabellenformat.</span><span class="sxs-lookup"><span data-stu-id="c0704-118">The `Get-AzureRmVM` command defaults output into a table format.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="c0704-119">Mit dem Cmdlet `Format-Table` können Sie die zurückgegebenen Spalten begrenzen.</span><span class="sxs-lookup"><span data-stu-id="c0704-119">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="c0704-120">Im folgenden Beispiel rufen wir die gleiche Liste mit virtuellen Computern ab, beschränken die Ausgabe aber auf den Namen des virtuellen Computers, die Ressourcengruppe und den Standort des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c0704-120">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="c0704-121">Der Parameter `-Autosize` passt die Größe der Spalten an die Größe der Daten an.</span><span class="sxs-lookup"><span data-stu-id="c0704-121">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="c0704-122">Die Ausgabe kann auch als Liste formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="c0704-122">Output can also be formatted into a list.</span></span> <span data-ttu-id="c0704-123">Das wird im folgenden Beispiel mit dem Cmdlet `Format-List` veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c0704-123">The following example shows this using the`Format-List` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```output
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="convert-to-other-data-types"></a><span data-ttu-id="c0704-124">Konvertieren in andere Datentypen</span><span class="sxs-lookup"><span data-stu-id="c0704-124">Convert to other data types</span></span>

<span data-ttu-id="c0704-125">Die Befehlsausgabe kann von PowerShell auch in mehrere Datenformate konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="c0704-125">PowerShell also allows taking command output and converting it into multiple data formats.</span></span> <span data-ttu-id="c0704-126">Im folgenden Beispiel werden mithilfe des Cmdlets `Select-Object` Attribute der virtuellen Computer in unserem Abonnement abgerufen, und die Ausgabe wird in das CSV-Format konvertiert, um sie problemlos in eine Datenbank oder in eine Tabelle importieren zu können.</span><span class="sxs-lookup"><span data-stu-id="c0704-126">In the following example the `Select-Object` cmdlet is used to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="c0704-127">Die Ausgabe kann auch in das JSON-Format konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="c0704-127">Output can also be converted into the JSON format.</span></span>  <span data-ttu-id="c0704-128">Im folgenden Beispiel wird die gleiche Liste mit virtuellen Computern erstellt, die Ausgabe erfolgt jedoch im JSON-Format.</span><span class="sxs-lookup"><span data-stu-id="c0704-128">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```output
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
