---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472703"
---
# <span data-ttu-id="de16f-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="de16f-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="de16f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de16f-102">SYNOPSIS</span></span>
<span data-ttu-id="de16f-103">Aktualisiert einen Bandbreitenzeitplan.</span><span class="sxs-lookup"><span data-stu-id="de16f-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="de16f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de16f-104">SYNTAX</span></span>

### <span data-ttu-id="de16f-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="de16f-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de16f-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de16f-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de16f-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="de16f-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de16f-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="de16f-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de16f-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de16f-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de16f-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="de16f-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de16f-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="de16f-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de16f-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="de16f-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de16f-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="de16f-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de16f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de16f-114">DESCRIPTION</span></span>
<span data-ttu-id="de16f-115">Das **Cmdlet Set-AzDataBoxEdgeBandwidthSchedule** aktualisiert einen Bandbreitenzeitplan für ein Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="de16f-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="de16f-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="de16f-116">EXAMPLES</span></span>

### <span data-ttu-id="de16f-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="de16f-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="de16f-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="de16f-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="de16f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de16f-119">PARAMETERS</span></span>

### <span data-ttu-id="de16f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de16f-120">-AsJob</span></span>
<span data-ttu-id="de16f-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="de16f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de16f-122">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="de16f-122">-Bandwidth</span></span>
<span data-ttu-id="de16f-123">Bandbreite in Mbit/s</span><span class="sxs-lookup"><span data-stu-id="de16f-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="de16f-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="de16f-124">-DaysOfWeek</span></span>
<span data-ttu-id="de16f-125">Scheduled DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="de16f-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="de16f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de16f-126">-DefaultProfile</span></span>
<span data-ttu-id="de16f-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de16f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de16f-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="de16f-128">-DeviceName</span></span>
<span data-ttu-id="de16f-129">Gerätename</span><span class="sxs-lookup"><span data-stu-id="de16f-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de16f-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de16f-130">-InputObject</span></span>
<span data-ttu-id="de16f-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="de16f-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de16f-132">-Name</span><span class="sxs-lookup"><span data-stu-id="de16f-132">-Name</span></span>
<span data-ttu-id="de16f-133">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="de16f-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de16f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de16f-134">-ResourceGroupName</span></span>
<span data-ttu-id="de16f-135">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="de16f-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de16f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de16f-136">-ResourceId</span></span>
<span data-ttu-id="de16f-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="de16f-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de16f-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="de16f-138">-StartTime</span></span>
<span data-ttu-id="de16f-139">Planen der Startzeit</span><span class="sxs-lookup"><span data-stu-id="de16f-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="de16f-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="de16f-140">-StopTime</span></span>
<span data-ttu-id="de16f-141">Planen der Stoppzeit</span><span class="sxs-lookup"><span data-stu-id="de16f-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="de16f-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="de16f-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="de16f-143">"Unbegrenzte Bandbreite festlegen"</span><span class="sxs-lookup"><span data-stu-id="de16f-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de16f-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de16f-144">-Confirm</span></span>
<span data-ttu-id="de16f-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de16f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de16f-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="de16f-146">-WhatIf</span></span>
<span data-ttu-id="de16f-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de16f-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de16f-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de16f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de16f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de16f-149">CommonParameters</span></span>
<span data-ttu-id="de16f-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de16f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de16f-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de16f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de16f-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="de16f-152">INPUTS</span></span>

### <span data-ttu-id="de16f-153">Keine</span><span class="sxs-lookup"><span data-stu-id="de16f-153">None</span></span>

## <span data-ttu-id="de16f-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="de16f-154">OUTPUTS</span></span>

### <span data-ttu-id="de16f-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="de16f-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="de16f-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="de16f-156">NOTES</span></span>

## <span data-ttu-id="de16f-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="de16f-157">RELATED LINKS</span></span>
