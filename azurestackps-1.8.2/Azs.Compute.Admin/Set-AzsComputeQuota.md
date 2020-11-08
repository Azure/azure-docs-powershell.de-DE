---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8da912ed9751231a44c34b27df36abc62d55c4ab
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006990"
---
# <span data-ttu-id="da4e5-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="da4e5-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="da4e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da4e5-102">SYNOPSIS</span></span>
<span data-ttu-id="da4e5-103">Aktualisieren eines vorhandenen Compute-Kontingents mit den bereitgestellten Parametern</span><span class="sxs-lookup"><span data-stu-id="da4e5-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="da4e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da4e5-104">SYNTAX</span></span>

### <span data-ttu-id="da4e5-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="da4e5-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da4e5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="da4e5-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da4e5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="da4e5-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da4e5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da4e5-108">DESCRIPTION</span></span>
<span data-ttu-id="da4e5-109">Aktualisieren eines vorhandenen Compute-Kontingents</span><span class="sxs-lookup"><span data-stu-id="da4e5-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="da4e5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da4e5-110">EXAMPLES</span></span>

### <span data-ttu-id="da4e5-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="da4e5-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="da4e5-112">Aktualisieren eines Compute-Kontingents</span><span class="sxs-lookup"><span data-stu-id="da4e5-112">Update a compute quota.</span></span>

## <span data-ttu-id="da4e5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="da4e5-113">PARAMETERS</span></span>

### <span data-ttu-id="da4e5-114">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="da4e5-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="da4e5-115">Die Anzahl der zulässigen Verfügbarkeits Sätze.</span><span class="sxs-lookup"><span data-stu-id="da4e5-115">Number of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4e5-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="da4e5-116">-CoresCount</span></span>
<span data-ttu-id="da4e5-117">Die Anzahl der zulässigen Kerne.</span><span class="sxs-lookup"><span data-stu-id="da4e5-117">Number of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4e5-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="da4e5-118">-InputObject</span></span>
<span data-ttu-id="da4e5-119">Möglicherweise geändertes Compute-Kontingent hat das Formular Get-AzsComputeQuota zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="da4e5-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

```yaml
Type: ComputeQuotaObject
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da4e5-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="da4e5-120">-Location</span></span>
<span data-ttu-id="da4e5-121">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="da4e5-121">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4e5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="da4e5-122">-Name</span></span>
<span data-ttu-id="da4e5-123">Der Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="da4e5-123">The name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4e5-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="da4e5-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="da4e5-125">Die Größe für standardmäßig verwaltete Festplatten und Snapshots ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="da4e5-125">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4e5-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="da4e5-126">-ResourceId</span></span>
<span data-ttu-id="da4e5-127">Die ID des Arm-Compute-Kontingents.</span><span class="sxs-lookup"><span data-stu-id="da4e5-127">The ARM compute quota id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da4e5-128">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="da4e5-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="da4e5-129">Die Größe für standardmäßig verwaltete Festplatten und Snapshots ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="da4e5-129">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4e5-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="da4e5-130">-VirtualMachineCount</span></span>
<span data-ttu-id="da4e5-131">Die Anzahl der zulässigen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="da4e5-131">Number of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4e5-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="da4e5-132">-VmScaleSetCount</span></span>
<span data-ttu-id="da4e5-133">Die Anzahl der zulässigen Skalensätze.</span><span class="sxs-lookup"><span data-stu-id="da4e5-133">Number of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4e5-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="da4e5-134">-Confirm</span></span>
<span data-ttu-id="da4e5-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da4e5-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4e5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da4e5-136">-WhatIf</span></span>
<span data-ttu-id="da4e5-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da4e5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da4e5-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da4e5-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4e5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da4e5-139">CommonParameters</span></span>
<span data-ttu-id="da4e5-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da4e5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da4e5-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da4e5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da4e5-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da4e5-142">INPUTS</span></span>

## <span data-ttu-id="da4e5-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da4e5-143">OUTPUTS</span></span>

### <span data-ttu-id="da4e5-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="da4e5-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="da4e5-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="da4e5-145">NOTES</span></span>

## <span data-ttu-id="da4e5-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da4e5-146">RELATED LINKS</span></span>

