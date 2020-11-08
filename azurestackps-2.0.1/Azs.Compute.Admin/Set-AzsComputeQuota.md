---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/set-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 3229a6383d7159b31bf542add7374326d0de4ac4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005566"
---
# <span data-ttu-id="30ea5-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="30ea5-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="30ea5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30ea5-102">SYNOPSIS</span></span>


## <span data-ttu-id="30ea5-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="30ea5-103">SYNTAX</span></span>

### <span data-ttu-id="30ea5-104">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="30ea5-104">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30ea5-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="30ea5-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -NewQuota <IQuota> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30ea5-106">UpdateExpanded</span><span class="sxs-lookup"><span data-stu-id="30ea5-106">UpdateExpanded</span></span>
```
Set-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```
## <span data-ttu-id="30ea5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30ea5-107">DESCRIPTION</span></span>
<span data-ttu-id="30ea5-108">Aktualisieren eines Compute-Kontingents</span><span class="sxs-lookup"><span data-stu-id="30ea5-108">Update a Compute Quota</span></span>

## <span data-ttu-id="30ea5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30ea5-109">EXAMPLES</span></span>

### <span data-ttu-id="30ea5-110">Beispiel 1: Festlegung von Eigenschaften für ein vorhandenes Compute-Kontingent</span><span class="sxs-lookup"><span data-stu-id="30ea5-110">Example 1: Set Properties on an Existing Compute Quota</span></span>
```powershell
PS C:\> $myComputeQuota = Get-AzsComputeQuota -Name MyComputeQuota

PS C:\> $myComputeQuota.CoresLimit = 99; 

PS C:\> Set-AzsComputeQuota -NewQuota $myComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 99
Id                                 : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/northwest/quotas/MyComputeQuota
Location                           : northwest
Name                               : MyComputeQuota
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="30ea5-111">Setzen Sie die Parameter, die in der Befehlszeile angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="30ea5-111">Set the parameters specified on the command line.</span></span>
<span data-ttu-id="30ea5-112">Parameter, die nicht gesetzt sind, werden standardmäßig auf 0 gesetzt.</span><span class="sxs-lookup"><span data-stu-id="30ea5-112">Any parameters not set will default to 0</span></span>

## <span data-ttu-id="30ea5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="30ea5-113">PARAMETERS</span></span>

### <span data-ttu-id="30ea5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ea5-114">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30ea5-115">-Neukontingent</span><span class="sxs-lookup"><span data-stu-id="30ea5-115">-NewQuota</span></span>
<span data-ttu-id="30ea5-116">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Eigenschaften von "neu Kontingent" und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="30ea5-116">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="30ea5-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="30ea5-117">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30ea5-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="30ea5-118">-Confirm</span></span>
<span data-ttu-id="30ea5-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="30ea5-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30ea5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30ea5-120">-WhatIf</span></span>
<span data-ttu-id="30ea5-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="30ea5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30ea5-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30ea5-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30ea5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ea5-123">CommonParameters</span></span>
<span data-ttu-id="30ea5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30ea5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ea5-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30ea5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ea5-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30ea5-126">INPUTS</span></span>

### <span data-ttu-id="30ea5-127">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="30ea5-127">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="30ea5-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30ea5-128">OUTPUTS</span></span>

### <span data-ttu-id="30ea5-129">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="30ea5-129">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="30ea5-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="30ea5-130">NOTES</span></span>

<span data-ttu-id="30ea5-131">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="30ea5-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30ea5-132">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="30ea5-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="30ea5-133">Neukontingent <IQuota> :</span><span class="sxs-lookup"><span data-stu-id="30ea5-133">NEWQUOTA <IQuota>:</span></span> 
  - <span data-ttu-id="30ea5-134">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="30ea5-134">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="30ea5-135">`[AvailabilitySetCount <Int32?>]`: Maximale Anzahl zulässiger Verfügbarkeits Sätze.</span><span class="sxs-lookup"><span data-stu-id="30ea5-135">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="30ea5-136">`[CoresLimit <Int32?>]`: Maximal zulässige Anzahl von Kernen.</span><span class="sxs-lookup"><span data-stu-id="30ea5-136">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="30ea5-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximale Anzahl von verwalteten Datenträgern und Snapshots des Typs "Premium" zulässig.</span><span class="sxs-lookup"><span data-stu-id="30ea5-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="30ea5-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximale Anzahl von verwalteten Datenträgern und Snapshots des Typs Standard zulässig.</span><span class="sxs-lookup"><span data-stu-id="30ea5-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="30ea5-139">`[VMScaleSetCount <Int32?>]`: Maximale Anzahl von Skalen Sätzen zulässig.</span><span class="sxs-lookup"><span data-stu-id="30ea5-139">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="30ea5-140">`[VirtualMachineCount <Int32?>]`: Maximale Anzahl der zulässigen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="30ea5-140">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="30ea5-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30ea5-141">RELATED LINKS</span></span>

