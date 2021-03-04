---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 17221e2d4f88e2f59ee13f73fb18132c01f6632e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940811"
---
# <span data-ttu-id="3bc82-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="3bc82-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="3bc82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bc82-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc82-103">Aktualisiert einen Bandbreitenplan.</span><span class="sxs-lookup"><span data-stu-id="3bc82-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="3bc82-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3bc82-104">SYNTAX</span></span>

### <span data-ttu-id="3bc82-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3bc82-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc82-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc82-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc82-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="3bc82-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc82-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="3bc82-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc82-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc82-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc82-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="3bc82-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc82-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="3bc82-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc82-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="3bc82-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc82-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="3bc82-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bc82-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3bc82-114">DESCRIPTION</span></span>
<span data-ttu-id="3bc82-115">Das **Cmdlet Set-AzStackEdgeBandwidthSchedule** aktualisiert einen Bandbreitenplan für ein Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="3bc82-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="3bc82-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3bc82-116">EXAMPLES</span></span>

### <span data-ttu-id="3bc82-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3bc82-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="3bc82-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3bc82-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="3bc82-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3bc82-119">PARAMETERS</span></span>

### <span data-ttu-id="3bc82-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3bc82-120">-AsJob</span></span>
<span data-ttu-id="3bc82-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3bc82-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc82-122">-Bandbreite</span><span class="sxs-lookup"><span data-stu-id="3bc82-122">-Bandwidth</span></span>
<span data-ttu-id="3bc82-123">Bandbreite in Mbit/s</span><span class="sxs-lookup"><span data-stu-id="3bc82-123">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateByResourceIdParameterBandwidthSet, UpdateByInputObjectParameterBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc82-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="3bc82-124">-DaysOfWeek</span></span>
<span data-ttu-id="3bc82-125">Scheduled DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="3bc82-125">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc82-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc82-126">-DefaultProfile</span></span>
<span data-ttu-id="3bc82-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3bc82-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc82-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3bc82-128">-DeviceName</span></span>
<span data-ttu-id="3bc82-129">Gerätename</span><span class="sxs-lookup"><span data-stu-id="3bc82-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc82-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bc82-130">-InputObject</span></span>
<span data-ttu-id="3bc82-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bc82-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc82-132">-Name</span><span class="sxs-lookup"><span data-stu-id="3bc82-132">-Name</span></span>
<span data-ttu-id="3bc82-133">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="3bc82-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc82-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc82-134">-ResourceGroupName</span></span>
<span data-ttu-id="3bc82-135">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3bc82-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc82-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bc82-136">-ResourceId</span></span>
<span data-ttu-id="3bc82-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bc82-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc82-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3bc82-138">-StartTime</span></span>
<span data-ttu-id="3bc82-139">Planen der Startzeit</span><span class="sxs-lookup"><span data-stu-id="3bc82-139">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc82-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="3bc82-140">-StopTime</span></span>
<span data-ttu-id="3bc82-141">Planen der Stoppzeit</span><span class="sxs-lookup"><span data-stu-id="3bc82-141">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc82-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="3bc82-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="3bc82-143">Wird unbegrenzte Bandbreite festgelegt</span><span class="sxs-lookup"><span data-stu-id="3bc82-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc82-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3bc82-144">-Confirm</span></span>
<span data-ttu-id="3bc82-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3bc82-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bc82-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bc82-146">-WhatIf</span></span>
<span data-ttu-id="3bc82-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3bc82-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bc82-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bc82-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bc82-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc82-149">CommonParameters</span></span>
<span data-ttu-id="3bc82-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc82-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc82-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bc82-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc82-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3bc82-152">INPUTS</span></span>

### <span data-ttu-id="3bc82-153">Keine</span><span class="sxs-lookup"><span data-stu-id="3bc82-153">None</span></span>

## <span data-ttu-id="3bc82-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3bc82-154">OUTPUTS</span></span>

### <span data-ttu-id="3bc82-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="3bc82-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="3bc82-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3bc82-156">NOTES</span></span>

## <span data-ttu-id="3bc82-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3bc82-157">RELATED LINKS</span></span>
