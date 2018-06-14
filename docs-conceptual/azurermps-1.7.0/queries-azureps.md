---
title: Abfragen von Azure-Ressourcen und Formatieren der Ergebnisse | Microsoft-Dokumentation
description: Hier erfahren Sie, wie Sie in Azure Ressourcenabfragen ausführen und die Ergebnisse formatieren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 1584c8166078b7d7d24ce8748307fde0f565b662
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853507"
---
# <a name="querying-for-azure-resources"></a><span data-ttu-id="613f2-103">Abfragen von Azure-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="613f2-103">Querying for Azure resources</span></span>

<span data-ttu-id="613f2-104">Abfragen können in PowerShell mithilfe integrierter Cmdlets ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="613f2-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="613f2-105">Cmdlet-Namen haben in PowerShell das Format **_Verb-Nomen_**.</span><span class="sxs-lookup"><span data-stu-id="613f2-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="613f2-106">Die Abfrage-Cmdlets sind am Verb **_Get_** zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="613f2-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="613f2-107">Bei den Cmdlet-Nomen handelt es sich um die Arten von Azure-Ressourcen, für die eine dem Cmdlet-Verb entsprechende Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="613f2-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>


## <a name="selecting-simple-properties"></a><span data-ttu-id="613f2-108">Auswählen einfacher Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="613f2-108">Selecting simple properties</span></span>

<span data-ttu-id="613f2-109">In Azure PowerShell ist für jedes Cmdlet eine Standardformatierung definiert.</span><span class="sxs-lookup"><span data-stu-id="613f2-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="613f2-110">Die am häufigsten verwendeten Eigenschaften für die einzelnen Ressourcentypen werden automatisch in einer Tabelle oder Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="613f2-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="613f2-111">Weitere Informationen zum Formatieren der Ausgabe finden Sie unter [Formatieren von Abfrageergebnissen](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="613f2-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="613f2-112">Fragen Sie mithilfe des Cmdlets `Get-AzureRmVM` eine Liste mit virtuellen Computern in Ihrem Konto ab.</span><span class="sxs-lookup"><span data-stu-id="613f2-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```powershell
Get-AzureRmVM
```

<span data-ttu-id="613f2-113">Die Standardausgabe wird automatisch als Tabelle formatiert.</span><span class="sxs-lookup"><span data-stu-id="613f2-113">The default output is automatically formatted as a table.</span></span>

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="613f2-114">Mit dem Cmdlet `Select-Object` können Sie spezifische Eigenschaften auswählen, die für Sie von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="613f2-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```powershell
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="613f2-115">Auswählen komplexer geschachtelter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="613f2-115">Selecting complex nested properties</span></span>

<span data-ttu-id="613f2-116">Wenn sich die Eigenschaft, die Sie auswählen möchten, tief in der Struktur der JSON-Ausgabe befindet, müssen Sie den vollständigen Pfad zu dieser geschachtelten Eigenschaft angeben.</span><span class="sxs-lookup"><span data-stu-id="613f2-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="613f2-117">Das folgende Beispiel zeigt, wie Sie den VM-Namen und den Betriebssystemtyp auf der Grundlage des Cmdlets `Get-AzureRmVM` auswählen.</span><span class="sxs-lookup"><span data-stu-id="613f2-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```powershell
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a><span data-ttu-id="613f2-118">Filtern von Ergebnissen mithilfe des Cmdlets „Where-Object“</span><span class="sxs-lookup"><span data-stu-id="613f2-118">Filter result using the Where-Object cmdlet</span></span>

<span data-ttu-id="613f2-119">Mit dem Cmdlet `Where-Object` können Sie das Ergebnis auf der Grundlage eines beliebigen Eigenschaftswerts filtern.</span><span class="sxs-lookup"><span data-stu-id="613f2-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="613f2-120">Im folgenden Beispiel wählt der Filter nur virtuelle Computer aus, deren Name „RGD“ enthält.</span><span class="sxs-lookup"><span data-stu-id="613f2-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```powershell
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="613f2-121">Im nächsten Beispiel werden die virtuellen Computer zurückgegeben, bei denen „vmSize“ den Wert „Standard_DS1_V2“ besitzt.</span><span class="sxs-lookup"><span data-stu-id="613f2-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```powershell
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
