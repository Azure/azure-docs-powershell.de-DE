---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173409"
---
# <span data-ttu-id="211a4-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="211a4-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="211a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="211a4-102">SYNOPSIS</span></span>
<span data-ttu-id="211a4-103">Aktualisiert einen Bandbreiten Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="211a4-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="211a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="211a4-104">SYNTAX</span></span>

### <span data-ttu-id="211a4-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="211a4-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="211a4-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="211a4-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="211a4-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="211a4-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="211a4-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="211a4-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="211a4-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="211a4-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="211a4-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="211a4-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="211a4-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="211a4-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="211a4-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="211a4-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="211a4-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="211a4-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="211a4-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="211a4-114">DESCRIPTION</span></span>
<span data-ttu-id="211a4-115">Das Cmdlet " **Satz-AzStackEdgeBandwidthSchedule** " aktualisiert einen Bandbreiten Zeitplan für ein Stack-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="211a4-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="211a4-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="211a4-116">EXAMPLES</span></span>

### <span data-ttu-id="211a4-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="211a4-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="211a4-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="211a4-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="211a4-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="211a4-119">PARAMETERS</span></span>

### <span data-ttu-id="211a4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="211a4-120">-AsJob</span></span>
<span data-ttu-id="211a4-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="211a4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="211a4-122">-Bandbreite</span><span class="sxs-lookup"><span data-stu-id="211a4-122">-Bandwidth</span></span>
<span data-ttu-id="211a4-123">Bandbreite in Mbit/s</span><span class="sxs-lookup"><span data-stu-id="211a4-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="211a4-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="211a4-124">-DaysOfWeek</span></span>
<span data-ttu-id="211a4-125">Geplanter DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="211a4-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="211a4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="211a4-126">-DefaultProfile</span></span>
<span data-ttu-id="211a4-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="211a4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="211a4-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="211a4-128">-DeviceName</span></span>
<span data-ttu-id="211a4-129">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="211a4-129">Device Name</span></span>

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

### <span data-ttu-id="211a4-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="211a4-130">-InputObject</span></span>
<span data-ttu-id="211a4-131">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="211a4-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="211a4-132">-Name</span><span class="sxs-lookup"><span data-stu-id="211a4-132">-Name</span></span>
<span data-ttu-id="211a4-133">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="211a4-133">Resource Name</span></span>

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

### <span data-ttu-id="211a4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="211a4-134">-ResourceGroupName</span></span>
<span data-ttu-id="211a4-135">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="211a4-135">Resource Group Name</span></span>

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

### <span data-ttu-id="211a4-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="211a4-136">-ResourceId</span></span>
<span data-ttu-id="211a4-137">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="211a4-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="211a4-138">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="211a4-138">-StartTime</span></span>
<span data-ttu-id="211a4-139">Startzeit planen</span><span class="sxs-lookup"><span data-stu-id="211a4-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="211a4-140">-Stoppzeit</span><span class="sxs-lookup"><span data-stu-id="211a4-140">-StopTime</span></span>
<span data-ttu-id="211a4-141">Planen der Endzeit</span><span class="sxs-lookup"><span data-stu-id="211a4-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="211a4-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="211a4-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="211a4-143">Setzt unbegrenzte Bandbreite</span><span class="sxs-lookup"><span data-stu-id="211a4-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="211a4-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="211a4-144">-Confirm</span></span>
<span data-ttu-id="211a4-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="211a4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="211a4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="211a4-146">-WhatIf</span></span>
<span data-ttu-id="211a4-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="211a4-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="211a4-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="211a4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="211a4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="211a4-149">CommonParameters</span></span>
<span data-ttu-id="211a4-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="211a4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="211a4-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="211a4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="211a4-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="211a4-152">INPUTS</span></span>

### <span data-ttu-id="211a4-153">Keine</span><span class="sxs-lookup"><span data-stu-id="211a4-153">None</span></span>

## <span data-ttu-id="211a4-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="211a4-154">OUTPUTS</span></span>

### <span data-ttu-id="211a4-155">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="211a4-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="211a4-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="211a4-156">NOTES</span></span>

## <span data-ttu-id="211a4-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="211a4-157">RELATED LINKS</span></span>
