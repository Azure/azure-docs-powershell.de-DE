---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 2c83773ba08c2fefe9404fa69861518d00d4d936
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942619"
---
# <span data-ttu-id="0b959-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0b959-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="0b959-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b959-102">SYNOPSIS</span></span>
<span data-ttu-id="0b959-103">Erstellt einen neuen Bandbreitenplan</span><span class="sxs-lookup"><span data-stu-id="0b959-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="0b959-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b959-104">SYNTAX</span></span>

### <span data-ttu-id="0b959-105">BandwidthParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b959-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b959-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b959-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b959-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b959-107">DESCRIPTION</span></span>
<span data-ttu-id="0b959-108">Das **Cmdlet New-AzDataBoxEdgeBandwidthSchedule** erstellt einen neuen Bandbreitenplan für ein Data Box Edge-Gerät, um die Bandbreitennutzung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="0b959-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="0b959-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b959-109">EXAMPLES</span></span>

### <span data-ttu-id="0b959-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0b959-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="0b959-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0b959-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="0b959-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0b959-112">PARAMETERS</span></span>

### <span data-ttu-id="0b959-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b959-113">-AsJob</span></span>
<span data-ttu-id="0b959-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0b959-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b959-115">-Bandbreite</span><span class="sxs-lookup"><span data-stu-id="0b959-115">-Bandwidth</span></span>
<span data-ttu-id="0b959-116">Bandbreite in Mbit/s</span><span class="sxs-lookup"><span data-stu-id="0b959-116">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: BandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b959-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0b959-117">-DaysOfWeek</span></span>
<span data-ttu-id="0b959-118">Scheduled DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0b959-118">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b959-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b959-119">-DefaultProfile</span></span>
<span data-ttu-id="0b959-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b959-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b959-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0b959-121">-DeviceName</span></span>
<span data-ttu-id="0b959-122">Gerätename</span><span class="sxs-lookup"><span data-stu-id="0b959-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b959-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0b959-123">-Name</span></span>
<span data-ttu-id="0b959-124">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="0b959-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b959-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b959-125">-ResourceGroupName</span></span>
<span data-ttu-id="0b959-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="0b959-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b959-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0b959-127">-StartTime</span></span>
<span data-ttu-id="0b959-128">Planen der Startzeit</span><span class="sxs-lookup"><span data-stu-id="0b959-128">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b959-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="0b959-129">-StopTime</span></span>
<span data-ttu-id="0b959-130">Planen der Stoppzeit</span><span class="sxs-lookup"><span data-stu-id="0b959-130">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b959-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="0b959-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="0b959-132">Wird Unbegrenzte Bandbreite festgelegt, wenn auf "false" festgelegt wird, wird der Standardwert auf 20 Mbit/s festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0b959-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b959-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b959-133">-Confirm</span></span>
<span data-ttu-id="0b959-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b959-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b959-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b959-135">-WhatIf</span></span>
<span data-ttu-id="0b959-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b959-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b959-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b959-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b959-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b959-138">CommonParameters</span></span>
<span data-ttu-id="0b959-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b959-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b959-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b959-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b959-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b959-141">INPUTS</span></span>

### <span data-ttu-id="0b959-142">Keine</span><span class="sxs-lookup"><span data-stu-id="0b959-142">None</span></span>

## <span data-ttu-id="0b959-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b959-143">OUTPUTS</span></span>

### <span data-ttu-id="0b959-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0b959-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="0b959-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0b959-145">NOTES</span></span>

## <span data-ttu-id="0b959-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0b959-146">RELATED LINKS</span></span>
