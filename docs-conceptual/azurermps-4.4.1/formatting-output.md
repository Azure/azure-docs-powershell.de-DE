---
title: Formatieren von Abfrageergebnissen | Microsoft-Dokumentation
description: Hier erfahren Sie, wie Sie in Azure Ressourcenabfragen ausführen und die Ergebnisse formatieren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 9ae0d661630bf4e080b3bbaa7f357c384ef68cc4
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826560"
---
# <a name="formatting-query-results"></a><span data-ttu-id="1c00e-103">Formatieren von Abfrageergebnissen</span><span class="sxs-lookup"><span data-stu-id="1c00e-103">Formatting query results</span></span>

<span data-ttu-id="1c00e-104">Zur besseren Lesbarkeit der Ausgabe verfügt jedes PowerShell-Cmdlet standardmäßig über eine vordefinierte Formatierung.</span><span class="sxs-lookup"><span data-stu-id="1c00e-104">By default each PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="1c00e-105">Mit PowerShell ist es jedoch auch möglich, die Ausgabe anzupassen oder die Cmdlet-Ausgabe in ein anderes Format zu konvertieren. Hierzu stehen folgende Cmdlets zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="1c00e-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="1c00e-106">Formatierung</span><span class="sxs-lookup"><span data-stu-id="1c00e-106">Formatting</span></span>      | <span data-ttu-id="1c00e-107">Konvertierung</span><span class="sxs-lookup"><span data-stu-id="1c00e-107">Conversion</span></span>       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a><span data-ttu-id="1c00e-108">Formatierungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="1c00e-108">Formatting examples</span></span>

<span data-ttu-id="1c00e-109">In diesem Beispiel rufen wir eine Liste mit virtuellen Azure-Computern in unserem Standardabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="1c00e-109">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="1c00e-110">Bei dem Befehl „Get-AzureRmVM“ erfolgt die Ausgabe standardmäßig in einem Tabellenformat.</span><span class="sxs-lookup"><span data-stu-id="1c00e-110">The Get-AzureRmVM command defaults output into a table format.</span></span>

```powershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="1c00e-111">Mit dem Cmdlet `Format-Table` können Sie die zurückgegebenen Spalten begrenzen.</span><span class="sxs-lookup"><span data-stu-id="1c00e-111">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="1c00e-112">Im folgenden Beispiel rufen wir die gleiche Liste mit virtuellen Computern ab, beschränken die Ausgabe aber auf den Namen des virtuellen Computers, die Ressourcengruppe und den Standort des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="1c00e-112">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="1c00e-113">Der Parameter `-Autosize` passt die Größe der Spalten an die Größe der Daten an.</span><span class="sxs-lookup"><span data-stu-id="1c00e-113">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```powershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="1c00e-114">Informationen können bei Bedarf auch in einem Listenformat angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1c00e-114">If you would prefer you can view information in a list format.</span></span> <span data-ttu-id="1c00e-115">Das wird im folgenden Beispiel mit dem Cmdlet `Format-List` veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1c00e-115">The following example shows this using the`Format-List` cmdlet.</span></span>

```powershell-interactive
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

## <a name="converting-to-other-data-types"></a><span data-ttu-id="1c00e-116">Konvertieren in andere Datentypen</span><span class="sxs-lookup"><span data-stu-id="1c00e-116">Converting to other data types</span></span>

<span data-ttu-id="1c00e-117">PowerShell bietet außerdem mehrere Ausgabeformate für verschiedenste Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="1c00e-117">PowerShell also offers multiple output format you can use to meet your needs.</span></span>  <span data-ttu-id="1c00e-118">Im folgenden Beispiel rufen wir mithilfe des Cmdlets `Select-Object` Attribute der virtuellen Computer in unserem Abonnement ab und konvertieren die Ausgabe in das CSV-Format, um sie problemlos in eine Datenbank oder in eine Tabelle importieren zu können.</span><span class="sxs-lookup"><span data-stu-id="1c00e-118">In the following example we use the `Select-Object` cmdlet to get attributes of the virtual machines in our subscription and and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```powershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="1c00e-119">Die Ausgabe kann auch in das JSON-Format konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="1c00e-119">You can also convert the output into JSON format.</span></span>  <span data-ttu-id="1c00e-120">Im folgenden Beispiel wird die gleiche Liste mit virtuellen Computern erstellt, die Ausgabe erfolgt jedoch im JSON-Format.</span><span class="sxs-lookup"><span data-stu-id="1c00e-120">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```powershell-interactive
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
