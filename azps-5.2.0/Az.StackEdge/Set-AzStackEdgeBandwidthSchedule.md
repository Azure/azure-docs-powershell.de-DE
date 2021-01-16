---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358684"
---
# <span data-ttu-id="0cc98-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0cc98-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="0cc98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cc98-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc98-103">Aktualisiert einen Bandbreitenplan.</span><span class="sxs-lookup"><span data-stu-id="0cc98-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="0cc98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cc98-104">SYNTAX</span></span>

### <span data-ttu-id="0cc98-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0cc98-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cc98-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cc98-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0cc98-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0cc98-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cc98-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0cc98-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cc98-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cc98-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cc98-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0cc98-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cc98-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0cc98-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cc98-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0cc98-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cc98-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0cc98-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cc98-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0cc98-114">DESCRIPTION</span></span>
<span data-ttu-id="0cc98-115">Das **Cmdlet Set-AzStackEdgeBandwidthSchedule** aktualisiert einen Bandbreitenzeitplan für ein Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="0cc98-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="0cc98-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0cc98-116">EXAMPLES</span></span>

### <span data-ttu-id="0cc98-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0cc98-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="0cc98-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0cc98-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="0cc98-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cc98-119">PARAMETERS</span></span>

### <span data-ttu-id="0cc98-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cc98-120">-AsJob</span></span>
<span data-ttu-id="0cc98-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0cc98-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0cc98-122">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="0cc98-122">-Bandwidth</span></span>
<span data-ttu-id="0cc98-123">Bandbreite in Mbit/s</span><span class="sxs-lookup"><span data-stu-id="0cc98-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="0cc98-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0cc98-124">-DaysOfWeek</span></span>
<span data-ttu-id="0cc98-125">Scheduled DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0cc98-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="0cc98-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc98-126">-DefaultProfile</span></span>
<span data-ttu-id="0cc98-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0cc98-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cc98-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0cc98-128">-DeviceName</span></span>
<span data-ttu-id="0cc98-129">Gerätename</span><span class="sxs-lookup"><span data-stu-id="0cc98-129">Device Name</span></span>

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

### <span data-ttu-id="0cc98-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cc98-130">-InputObject</span></span>
<span data-ttu-id="0cc98-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cc98-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="0cc98-132">-Name</span><span class="sxs-lookup"><span data-stu-id="0cc98-132">-Name</span></span>
<span data-ttu-id="0cc98-133">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="0cc98-133">Resource Name</span></span>

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

### <span data-ttu-id="0cc98-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cc98-134">-ResourceGroupName</span></span>
<span data-ttu-id="0cc98-135">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="0cc98-135">Resource Group Name</span></span>

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

### <span data-ttu-id="0cc98-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cc98-136">-ResourceId</span></span>
<span data-ttu-id="0cc98-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cc98-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="0cc98-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0cc98-138">-StartTime</span></span>
<span data-ttu-id="0cc98-139">Planen der Startzeit</span><span class="sxs-lookup"><span data-stu-id="0cc98-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="0cc98-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="0cc98-140">-StopTime</span></span>
<span data-ttu-id="0cc98-141">Planen der Stoppzeit</span><span class="sxs-lookup"><span data-stu-id="0cc98-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="0cc98-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="0cc98-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="0cc98-143">"Unbegrenzte Bandbreite festlegen"</span><span class="sxs-lookup"><span data-stu-id="0cc98-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="0cc98-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0cc98-144">-Confirm</span></span>
<span data-ttu-id="0cc98-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0cc98-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cc98-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0cc98-146">-WhatIf</span></span>
<span data-ttu-id="0cc98-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0cc98-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0cc98-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0cc98-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cc98-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc98-149">CommonParameters</span></span>
<span data-ttu-id="0cc98-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cc98-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc98-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cc98-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc98-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0cc98-152">INPUTS</span></span>

### <span data-ttu-id="0cc98-153">Keine</span><span class="sxs-lookup"><span data-stu-id="0cc98-153">None</span></span>

## <span data-ttu-id="0cc98-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0cc98-154">OUTPUTS</span></span>

### <span data-ttu-id="0cc98-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0cc98-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="0cc98-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0cc98-156">NOTES</span></span>

## <span data-ttu-id="0cc98-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0cc98-157">RELATED LINKS</span></span>
