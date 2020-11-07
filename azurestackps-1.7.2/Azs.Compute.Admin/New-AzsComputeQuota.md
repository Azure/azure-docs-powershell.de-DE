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
ms.locfileid: "93826156"
---
# <span data-ttu-id="dfa40-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="dfa40-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="dfa40-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dfa40-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa40-103">Erstellen Sie ein neues Compute-Kontingent, das zum Begrenzen von Compute-Ressourcen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dfa40-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="dfa40-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfa40-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfa40-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfa40-105">DESCRIPTION</span></span>
<span data-ttu-id="dfa40-106">Erstellen Sie ein neues Compute-Kontingent.</span><span class="sxs-lookup"><span data-stu-id="dfa40-106">Create a new compute quota.</span></span>

## <span data-ttu-id="dfa40-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dfa40-107">EXAMPLES</span></span>

### <span data-ttu-id="dfa40-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dfa40-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="dfa40-109">Erstellen Sie ein neues Compute-Kontingent.</span><span class="sxs-lookup"><span data-stu-id="dfa40-109">Create a new compute quota.</span></span>

## <span data-ttu-id="dfa40-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfa40-110">PARAMETERS</span></span>

### <span data-ttu-id="dfa40-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="dfa40-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="dfa40-112">Die Anzahl der zulässigen Verfügbarkeits Sätze.</span><span class="sxs-lookup"><span data-stu-id="dfa40-112">Number  of availability sets allowed.</span></span>

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

### <span data-ttu-id="dfa40-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="dfa40-113">-CoresCount</span></span>
<span data-ttu-id="dfa40-114">Die Anzahl der zulässigen Kerne.</span><span class="sxs-lookup"><span data-stu-id="dfa40-114">Number  of cores allowed.</span></span>

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

### <span data-ttu-id="dfa40-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="dfa40-115">-Location</span></span>
<span data-ttu-id="dfa40-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="dfa40-116">Location of the resource.</span></span>

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

### <span data-ttu-id="dfa40-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dfa40-117">-Name</span></span>
<span data-ttu-id="dfa40-118">Der Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="dfa40-118">Name of the quota.</span></span>

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

### <span data-ttu-id="dfa40-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="dfa40-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="dfa40-120">Die Größe für standardmäßig verwaltete Festplatten und Snapshots ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="dfa40-120">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="dfa40-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="dfa40-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="dfa40-122">Die Größe für standardmäßig verwaltete Festplatten und Snapshots ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="dfa40-122">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="dfa40-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="dfa40-123">-VirtualMachineCount</span></span>
<span data-ttu-id="dfa40-124">Die Anzahl der zulässigen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="dfa40-124">Number  of virtual machines allowed.</span></span>

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

### <span data-ttu-id="dfa40-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="dfa40-125">-VmScaleSetCount</span></span>
<span data-ttu-id="dfa40-126">Die Anzahl der zulässigen Skalensätze.</span><span class="sxs-lookup"><span data-stu-id="dfa40-126">Number  of scale sets allowed.</span></span>

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

### <span data-ttu-id="dfa40-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dfa40-127">-Confirm</span></span>
<span data-ttu-id="dfa40-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dfa40-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfa40-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfa40-129">-WhatIf</span></span>
<span data-ttu-id="dfa40-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfa40-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfa40-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dfa40-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfa40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa40-132">CommonParameters</span></span>
<span data-ttu-id="dfa40-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfa40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa40-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfa40-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa40-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dfa40-135">INPUTS</span></span>

## <span data-ttu-id="dfa40-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dfa40-136">OUTPUTS</span></span>

### <span data-ttu-id="dfa40-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="dfa40-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="dfa40-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="dfa40-138">NOTES</span></span>

## <span data-ttu-id="dfa40-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dfa40-139">RELATED LINKS</span></span>

