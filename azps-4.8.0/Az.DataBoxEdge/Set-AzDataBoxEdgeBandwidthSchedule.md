---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174794"
---
# <span data-ttu-id="b047e-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b047e-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="b047e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b047e-102">SYNOPSIS</span></span>
<span data-ttu-id="b047e-103">Aktualisiert einen Bandbreiten Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="b047e-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="b047e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b047e-104">SYNTAX</span></span>

### <span data-ttu-id="b047e-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b047e-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b047e-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b047e-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b047e-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b047e-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b047e-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b047e-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b047e-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b047e-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b047e-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b047e-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b047e-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b047e-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b047e-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b047e-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b047e-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b047e-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b047e-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b047e-114">DESCRIPTION</span></span>
<span data-ttu-id="b047e-115">Mit dem Cmdlet " **festlegen-AzDataBoxEdgeBandwidthSchedule** " wird ein Bandbreiten Zeitplan für ein Daten Feld Edge-Gerät aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b047e-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="b047e-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b047e-116">EXAMPLES</span></span>

### <span data-ttu-id="b047e-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b047e-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="b047e-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b047e-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="b047e-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="b047e-119">PARAMETERS</span></span>

### <span data-ttu-id="b047e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b047e-120">-AsJob</span></span>
<span data-ttu-id="b047e-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b047e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b047e-122">-Bandbreite</span><span class="sxs-lookup"><span data-stu-id="b047e-122">-Bandwidth</span></span>
<span data-ttu-id="b047e-123">Bandbreite in Mbit/s</span><span class="sxs-lookup"><span data-stu-id="b047e-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="b047e-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="b047e-124">-DaysOfWeek</span></span>
<span data-ttu-id="b047e-125">Geplanter DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="b047e-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="b047e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b047e-126">-DefaultProfile</span></span>
<span data-ttu-id="b047e-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b047e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b047e-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b047e-128">-DeviceName</span></span>
<span data-ttu-id="b047e-129">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="b047e-129">Device Name</span></span>

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

### <span data-ttu-id="b047e-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b047e-130">-InputObject</span></span>
<span data-ttu-id="b047e-131">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="b047e-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="b047e-132">-Name</span><span class="sxs-lookup"><span data-stu-id="b047e-132">-Name</span></span>
<span data-ttu-id="b047e-133">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="b047e-133">Resource Name</span></span>

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

### <span data-ttu-id="b047e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b047e-134">-ResourceGroupName</span></span>
<span data-ttu-id="b047e-135">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b047e-135">Resource Group Name</span></span>

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

### <span data-ttu-id="b047e-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b047e-136">-ResourceId</span></span>
<span data-ttu-id="b047e-137">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="b047e-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="b047e-138">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="b047e-138">-StartTime</span></span>
<span data-ttu-id="b047e-139">Startzeit planen</span><span class="sxs-lookup"><span data-stu-id="b047e-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="b047e-140">-Stoppzeit</span><span class="sxs-lookup"><span data-stu-id="b047e-140">-StopTime</span></span>
<span data-ttu-id="b047e-141">Planen der Endzeit</span><span class="sxs-lookup"><span data-stu-id="b047e-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="b047e-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="b047e-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="b047e-143">Setzt unbegrenzte Bandbreite</span><span class="sxs-lookup"><span data-stu-id="b047e-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="b047e-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b047e-144">-Confirm</span></span>
<span data-ttu-id="b047e-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b047e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b047e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b047e-146">-WhatIf</span></span>
<span data-ttu-id="b047e-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b047e-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b047e-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b047e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b047e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b047e-149">CommonParameters</span></span>
<span data-ttu-id="b047e-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b047e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b047e-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b047e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b047e-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b047e-152">INPUTS</span></span>

### <span data-ttu-id="b047e-153">Keine</span><span class="sxs-lookup"><span data-stu-id="b047e-153">None</span></span>

## <span data-ttu-id="b047e-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b047e-154">OUTPUTS</span></span>

### <span data-ttu-id="b047e-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b047e-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="b047e-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="b047e-156">NOTES</span></span>

## <span data-ttu-id="b047e-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b047e-157">RELATED LINKS</span></span>
