---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azscomputequota
schema: 2.0.0
ms.openlocfilehash: efbd141d5ba41afa51c57f05df96840a81ab4fa1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844868"
---
# <span data-ttu-id="41e67-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="41e67-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="41e67-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41e67-102">SYNOPSIS</span></span>
<span data-ttu-id="41e67-103">Erstellt oder aktualisiert ein Compute-Kontingent mit den bereitgestellten Kontingent Parametern.</span><span class="sxs-lookup"><span data-stu-id="41e67-103">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="41e67-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41e67-104">SYNTAX</span></span>

### <span data-ttu-id="41e67-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="41e67-105">CreateExpanded (Default)</span></span>
```
New-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="41e67-106">Erstellen</span><span class="sxs-lookup"><span data-stu-id="41e67-106">Create</span></span>
```
New-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41e67-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41e67-107">DESCRIPTION</span></span>
<span data-ttu-id="41e67-108">Erstellt oder aktualisiert ein Compute-Kontingent mit den bereitgestellten Kontingent Parametern.</span><span class="sxs-lookup"><span data-stu-id="41e67-108">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="41e67-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41e67-109">EXAMPLES</span></span>

### <span data-ttu-id="41e67-110">Beispiel 1: Erstellen eines Compute-Kontingents mit Standardparametern</span><span class="sxs-lookup"><span data-stu-id="41e67-110">Example 1: Create a Compute Quota with Default Parameters</span></span>
```powershell
PS C:\> New-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="41e67-111">Alle Parameter, die nicht angegeben werden, werden auf Ihren Standardparameter festgelegt (siehe oben).</span><span class="sxs-lookup"><span data-stu-id="41e67-111">Any parameters that are not specified will be set to their default parameter, shown above.</span></span>

### <span data-ttu-id="41e67-112">Beispiel 2: Erstellen eines Compute-Kontingents mit benutzerdefinierten Parametern</span><span class="sxs-lookup"><span data-stu-id="41e67-112">Example 2: Create a Compute Quota with Custom Parameters</span></span>
```powershell
PS C:\>  New-AzsComputeQuota -Name ExampleComputeQuotaWithCustomParameters -Location local -AvailabilitySetCount 9 -CoresCount 99 -PremiumManagedDiskAndSnapshotSize 1024 -StandardManagedDiskAndSnapshotSize 1024 -VirtualMachineCount 99 -VMScaleSetCount 2

AvailabilitySetCount               : 9
CoresLimit                         : 99
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locat
                                     ions/local/quotas/ExampleComputeQuotaWithCustomParameters
Location                           : local
Name                               : ExampleComputeQuotaWithCustomParameters
PremiumManagedDiskAndSnapshotSize  : 1024
StandardManagedDiskAndSnapshotSize : 1024
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 2
VirtualMachineCount                : 99
```

<span data-ttu-id="41e67-113">Anpassen von Kontingenten mit Parametern</span><span class="sxs-lookup"><span data-stu-id="41e67-113">Customize Quota with parameters.</span></span> <span data-ttu-id="41e67-114">Alle Parameter, die nicht angegeben werden, haben den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="41e67-114">Any parameters not specified will have default value.</span></span>

## <span data-ttu-id="41e67-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="41e67-115">PARAMETERS</span></span>

### <span data-ttu-id="41e67-116">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="41e67-116">-AvailabilitySetCount</span></span>
<span data-ttu-id="41e67-117">Maximale Anzahl zulässiger Verfügbarkeits Sätze</span><span class="sxs-lookup"><span data-stu-id="41e67-117">Maximum number of availability sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e67-118">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="41e67-118">-CoresCount</span></span>
<span data-ttu-id="41e67-119">Die maximal zulässige Anzahl von Kernen.</span><span class="sxs-lookup"><span data-stu-id="41e67-119">Maximum number of cores allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases: CoresLimit

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e67-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e67-120">-DefaultProfile</span></span>
<span data-ttu-id="41e67-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="41e67-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41e67-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="41e67-122">-Location</span></span>
<span data-ttu-id="41e67-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="41e67-123">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e67-124">-Location1</span><span class="sxs-lookup"><span data-stu-id="41e67-124">-Location1</span></span>
<span data-ttu-id="41e67-125">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="41e67-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e67-126">-Name</span><span class="sxs-lookup"><span data-stu-id="41e67-126">-Name</span></span>
<span data-ttu-id="41e67-127">Der Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="41e67-127">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e67-128">-Neukontingent</span><span class="sxs-lookup"><span data-stu-id="41e67-128">-NewQuota</span></span>
<span data-ttu-id="41e67-129">Enthält Informationen zum Compute-Kontingent, die zur Steuerung der Ressourcenzuteilung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41e67-129">Holds Compute quota information used to control resource allocation.</span></span>
<span data-ttu-id="41e67-130">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Eigenschaften von "neu Kontingent" und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="41e67-130">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="41e67-131">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="41e67-131">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="41e67-132">Maximale Anzahl von verwalteten Datenträgern und Snapshots des Typs "Premium" zulässig.</span><span class="sxs-lookup"><span data-stu-id="41e67-132">Maximum number of managed disks and snapshots of type premium allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e67-133">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="41e67-133">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="41e67-134">Maximale Anzahl von verwalteten Datenträgern und Snapshots des Typs Standard zulässig.</span><span class="sxs-lookup"><span data-stu-id="41e67-134">Maximum number of managed disks and snapshots of type standard allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e67-135">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="41e67-135">-SubscriptionId</span></span>
<span data-ttu-id="41e67-136">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="41e67-136">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="41e67-137">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="41e67-137">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="41e67-138">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="41e67-138">-VirtualMachineCount</span></span>
<span data-ttu-id="41e67-139">Die maximale Anzahl der zulässigen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="41e67-139">Maximum number of virtual machines allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e67-140">-VMScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="41e67-140">-VMScaleSetCount</span></span>
<span data-ttu-id="41e67-141">Die maximal zulässige Anzahl von Skalen Sätzen.</span><span class="sxs-lookup"><span data-stu-id="41e67-141">Maximum number of scale sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e67-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="41e67-142">-Confirm</span></span>
<span data-ttu-id="41e67-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41e67-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41e67-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41e67-144">-WhatIf</span></span>
<span data-ttu-id="41e67-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41e67-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41e67-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41e67-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41e67-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e67-147">CommonParameters</span></span>
<span data-ttu-id="41e67-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41e67-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e67-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41e67-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e67-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41e67-150">INPUTS</span></span>

### <span data-ttu-id="41e67-151">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="41e67-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="41e67-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41e67-152">OUTPUTS</span></span>

### <span data-ttu-id="41e67-153">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="41e67-153">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="41e67-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="41e67-154">NOTES</span></span>

<span data-ttu-id="41e67-155">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="41e67-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41e67-156">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="41e67-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="41e67-157">Neu quota <IQuota> : enthält Compute Quota-Informationen, die zur Steuerung der Ressourcenzuteilung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41e67-157">NEWQUOTA <IQuota>: Holds Compute quota information used to control resource allocation.</span></span>
  - <span data-ttu-id="41e67-158">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="41e67-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="41e67-159">`[AvailabilitySetCount <Int32?>]`: Maximale Anzahl zulässiger Verfügbarkeits Sätze.</span><span class="sxs-lookup"><span data-stu-id="41e67-159">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="41e67-160">`[CoresLimit <Int32?>]`: Maximal zulässige Anzahl von Kernen.</span><span class="sxs-lookup"><span data-stu-id="41e67-160">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="41e67-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximale Anzahl von verwalteten Datenträgern und Snapshots des Typs "Premium" zulässig.</span><span class="sxs-lookup"><span data-stu-id="41e67-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="41e67-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximale Anzahl von verwalteten Datenträgern und Snapshots des Typs Standard zulässig.</span><span class="sxs-lookup"><span data-stu-id="41e67-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="41e67-163">`[VMScaleSetCount <Int32?>]`: Maximale Anzahl von Skalen Sätzen zulässig.</span><span class="sxs-lookup"><span data-stu-id="41e67-163">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="41e67-164">`[VirtualMachineCount <Int32?>]`: Maximale Anzahl der zulässigen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="41e67-164">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="41e67-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41e67-165">RELATED LINKS</span></span>

