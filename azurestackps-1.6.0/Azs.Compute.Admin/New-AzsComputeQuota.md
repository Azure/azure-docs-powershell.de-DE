---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc92bcc617c771c15330d1a24e8ed24466f7ffc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474637"
---
# <span data-ttu-id="111fa-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="111fa-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="111fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="111fa-102">SYNOPSIS</span></span>
<span data-ttu-id="111fa-103">Erstellen Sie ein neues Compute-Kontingent, das zum Begrenzen von Compute-Ressourcen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="111fa-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="111fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="111fa-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="111fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="111fa-105">DESCRIPTION</span></span>
<span data-ttu-id="111fa-106">Erstellen Sie ein neues Compute-Kontingent.</span><span class="sxs-lookup"><span data-stu-id="111fa-106">Create a new compute quota.</span></span>

## <span data-ttu-id="111fa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="111fa-107">EXAMPLES</span></span>

### <span data-ttu-id="111fa-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="111fa-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="111fa-109">Erstellen Sie ein neues Compute-Kontingent.</span><span class="sxs-lookup"><span data-stu-id="111fa-109">Create a new compute quota.</span></span>

## <span data-ttu-id="111fa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="111fa-110">PARAMETERS</span></span>

### <span data-ttu-id="111fa-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="111fa-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="111fa-112">Die Anzahl der zulässigen Verfügbarkeits Sätze.</span><span class="sxs-lookup"><span data-stu-id="111fa-112">Number  of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="111fa-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="111fa-113">-CoresCount</span></span>
<span data-ttu-id="111fa-114">Die Anzahl der zulässigen Kerne.</span><span class="sxs-lookup"><span data-stu-id="111fa-114">Number  of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: 3
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="111fa-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="111fa-115">-Location</span></span>
<span data-ttu-id="111fa-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="111fa-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="111fa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="111fa-117">-Name</span></span>
<span data-ttu-id="111fa-118">Der Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="111fa-118">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="111fa-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="111fa-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="111fa-120">Die Größe für standardmäßig verwaltete Festplatten und Snapshots ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="111fa-120">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="111fa-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="111fa-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="111fa-122">Die Größe für standardmäßig verwaltete Festplatten und Snapshots ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="111fa-122">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="111fa-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="111fa-123">-VirtualMachineCount</span></span>
<span data-ttu-id="111fa-124">Die Anzahl der zulässigen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="111fa-124">Number  of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="111fa-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="111fa-125">-VmScaleSetCount</span></span>
<span data-ttu-id="111fa-126">Die Anzahl der zulässigen Skalensätze.</span><span class="sxs-lookup"><span data-stu-id="111fa-126">Number  of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="111fa-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="111fa-127">-Confirm</span></span>
<span data-ttu-id="111fa-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="111fa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="111fa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="111fa-129">-WhatIf</span></span>
<span data-ttu-id="111fa-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="111fa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="111fa-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="111fa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="111fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="111fa-132">CommonParameters</span></span>
<span data-ttu-id="111fa-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="111fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="111fa-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="111fa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="111fa-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="111fa-135">INPUTS</span></span>

## <span data-ttu-id="111fa-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="111fa-136">OUTPUTS</span></span>

### <span data-ttu-id="111fa-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="111fa-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="111fa-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="111fa-138">NOTES</span></span>

## <span data-ttu-id="111fa-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="111fa-139">RELATED LINKS</span></span>

