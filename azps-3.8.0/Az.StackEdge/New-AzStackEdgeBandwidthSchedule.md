---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995700"
---
# <span data-ttu-id="68e54-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="68e54-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="68e54-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68e54-102">SYNOPSIS</span></span>
<span data-ttu-id="68e54-103">Erstellt einen neuen Bandbreiten Zeitplan</span><span class="sxs-lookup"><span data-stu-id="68e54-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="68e54-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68e54-104">SYNTAX</span></span>

### <span data-ttu-id="68e54-105">UnlimitedBandwidthParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="68e54-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68e54-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="68e54-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68e54-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68e54-107">DESCRIPTION</span></span>
<span data-ttu-id="68e54-108">Das Cmdlet **New-AzStackEdgeBandwidthSchedule** erstellt einen neuen Bandbreiten Zeitplan für ein Stack-Edge-Gerät, um die Bandbreitennutzung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="68e54-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="68e54-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68e54-109">EXAMPLES</span></span>

### <span data-ttu-id="68e54-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="68e54-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="68e54-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="68e54-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="68e54-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="68e54-112">PARAMETERS</span></span>

### <span data-ttu-id="68e54-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68e54-113">-AsJob</span></span>
<span data-ttu-id="68e54-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="68e54-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68e54-115">-Bandbreite</span><span class="sxs-lookup"><span data-stu-id="68e54-115">-Bandwidth</span></span>
<span data-ttu-id="68e54-116">Bandbreite in Mbit/s</span><span class="sxs-lookup"><span data-stu-id="68e54-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="68e54-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="68e54-117">-DaysOfWeek</span></span>
<span data-ttu-id="68e54-118">Geplanter DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="68e54-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="68e54-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e54-119">-DefaultProfile</span></span>
<span data-ttu-id="68e54-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="68e54-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68e54-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="68e54-121">-DeviceName</span></span>
<span data-ttu-id="68e54-122">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="68e54-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e54-123">-Name</span><span class="sxs-lookup"><span data-stu-id="68e54-123">-Name</span></span>
<span data-ttu-id="68e54-124">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="68e54-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e54-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68e54-125">-ResourceGroupName</span></span>
<span data-ttu-id="68e54-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="68e54-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e54-127">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="68e54-127">-StartTime</span></span>
<span data-ttu-id="68e54-128">Startzeit planen</span><span class="sxs-lookup"><span data-stu-id="68e54-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="68e54-129">-Stoppzeit</span><span class="sxs-lookup"><span data-stu-id="68e54-129">-StopTime</span></span>
<span data-ttu-id="68e54-130">Planen der Endzeit</span><span class="sxs-lookup"><span data-stu-id="68e54-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="68e54-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="68e54-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="68e54-132">Setzt die Bandbreite als unbegrenzt ein</span><span class="sxs-lookup"><span data-stu-id="68e54-132">Will Set Bandwidth as Unlimited</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e54-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="68e54-133">-Confirm</span></span>
<span data-ttu-id="68e54-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68e54-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68e54-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68e54-135">-WhatIf</span></span>
<span data-ttu-id="68e54-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68e54-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68e54-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68e54-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68e54-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e54-138">CommonParameters</span></span>
<span data-ttu-id="68e54-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68e54-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e54-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68e54-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e54-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68e54-141">INPUTS</span></span>

### <span data-ttu-id="68e54-142">Keine</span><span class="sxs-lookup"><span data-stu-id="68e54-142">None</span></span>

## <span data-ttu-id="68e54-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68e54-143">OUTPUTS</span></span>

### <span data-ttu-id="68e54-144">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="68e54-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="68e54-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="68e54-145">NOTES</span></span>

## <span data-ttu-id="68e54-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68e54-146">RELATED LINKS</span></span>
