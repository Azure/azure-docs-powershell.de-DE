---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 68522dbd90593bdbc37afe333144431b997cc70c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298791"
---
# <span data-ttu-id="2636a-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="2636a-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="2636a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2636a-102">SYNOPSIS</span></span>
<span data-ttu-id="2636a-103">Erstellt einen neuen Bandbreiten Zeitplan</span><span class="sxs-lookup"><span data-stu-id="2636a-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="2636a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2636a-104">SYNTAX</span></span>

### <span data-ttu-id="2636a-105">BandwidthParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2636a-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2636a-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="2636a-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2636a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2636a-107">DESCRIPTION</span></span>
<span data-ttu-id="2636a-108">Das Cmdlet **New-AzDataBoxEdgeBandwidthSchedule** erstellt einen neuen Bandbreiten Zeitplan für ein Edge-Gerät für Datenfelder, um die Bandbreitennutzung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="2636a-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="2636a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2636a-109">EXAMPLES</span></span>

### <span data-ttu-id="2636a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2636a-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="2636a-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2636a-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="2636a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2636a-112">PARAMETERS</span></span>

### <span data-ttu-id="2636a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2636a-113">-AsJob</span></span>
<span data-ttu-id="2636a-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2636a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2636a-115">-Bandbreite</span><span class="sxs-lookup"><span data-stu-id="2636a-115">-Bandwidth</span></span>
<span data-ttu-id="2636a-116">Bandbreite in Mbit/s</span><span class="sxs-lookup"><span data-stu-id="2636a-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="2636a-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="2636a-117">-DaysOfWeek</span></span>
<span data-ttu-id="2636a-118">Geplanter DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="2636a-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="2636a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2636a-119">-DefaultProfile</span></span>
<span data-ttu-id="2636a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2636a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2636a-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2636a-121">-DeviceName</span></span>
<span data-ttu-id="2636a-122">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="2636a-122">Device Name</span></span>

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

### <span data-ttu-id="2636a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2636a-123">-Name</span></span>
<span data-ttu-id="2636a-124">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="2636a-124">Resource Name</span></span>

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

### <span data-ttu-id="2636a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2636a-125">-ResourceGroupName</span></span>
<span data-ttu-id="2636a-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2636a-126">Resource Group Name</span></span>

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

### <span data-ttu-id="2636a-127">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="2636a-127">-StartTime</span></span>
<span data-ttu-id="2636a-128">Startzeit planen</span><span class="sxs-lookup"><span data-stu-id="2636a-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="2636a-129">-Stoppzeit</span><span class="sxs-lookup"><span data-stu-id="2636a-129">-StopTime</span></span>
<span data-ttu-id="2636a-130">Planen der Endzeit</span><span class="sxs-lookup"><span data-stu-id="2636a-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="2636a-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="2636a-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="2636a-132">Unbegrenzte Bandbreite festlegen, wenn auf "false" festgelegt ist, wird der Standardwert 20 Mbit/s festgelegt</span><span class="sxs-lookup"><span data-stu-id="2636a-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

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

### <span data-ttu-id="2636a-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2636a-133">-Confirm</span></span>
<span data-ttu-id="2636a-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2636a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2636a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2636a-135">-WhatIf</span></span>
<span data-ttu-id="2636a-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2636a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2636a-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2636a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2636a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2636a-138">CommonParameters</span></span>
<span data-ttu-id="2636a-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2636a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2636a-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2636a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2636a-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2636a-141">INPUTS</span></span>

### <span data-ttu-id="2636a-142">Keine</span><span class="sxs-lookup"><span data-stu-id="2636a-142">None</span></span>

## <span data-ttu-id="2636a-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2636a-143">OUTPUTS</span></span>

### <span data-ttu-id="2636a-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="2636a-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="2636a-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="2636a-145">NOTES</span></span>

## <span data-ttu-id="2636a-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2636a-146">RELATED LINKS</span></span>
