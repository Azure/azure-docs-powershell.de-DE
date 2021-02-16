---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: ac7fb7d6af2e04387ea4abfa3fe62c4df9271b13
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148316"
---
# <span data-ttu-id="786e9-101">New-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="786e9-101">New-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="786e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="786e9-102">SYNOPSIS</span></span>
<span data-ttu-id="786e9-103">Konfiguriert einen Trigger auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="786e9-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="786e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="786e9-104">SYNTAX</span></span>

### <span data-ttu-id="786e9-105">FileEventTriggerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="786e9-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="786e9-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="786e9-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="786e9-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="786e9-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="786e9-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="786e9-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="786e9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="786e9-109">DESCRIPTION</span></span>
<span data-ttu-id="786e9-110">Das **Cmdlet "New-AzDataBoxEdgeTrigger"** konfiguriert einen Trigger auf dem Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="786e9-110">The **New-AzDataBoxEdgeTrigger** cmdlet configures a trigger on the Data Box Edge device.</span></span> 

## <span data-ttu-id="786e9-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="786e9-111">EXAMPLES</span></span>

### <span data-ttu-id="786e9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="786e9-112">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="786e9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="786e9-113">PARAMETERS</span></span>

### <span data-ttu-id="786e9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="786e9-114">-AsJob</span></span>
<span data-ttu-id="786e9-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="786e9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="786e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="786e9-116">-DefaultProfile</span></span>
<span data-ttu-id="786e9-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="786e9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="786e9-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="786e9-118">-DeviceName</span></span>
<span data-ttu-id="786e9-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="786e9-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786e9-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="786e9-120">-FileEvent</span></span>
<span data-ttu-id="786e9-121">Übergeben sie diesen Parameter zum Konfigurieren des FileEvent-Triggers.</span><span class="sxs-lookup"><span data-stu-id="786e9-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileEventTriggerParameterSet, FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786e9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="786e9-122">-Name</span></span>
<span data-ttu-id="786e9-123">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="786e9-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786e9-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="786e9-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="786e9-125">Übergeben Sie diesen Parameter zum Konfigurieren des PeriodicTimerEvent-Triggers.</span><span class="sxs-lookup"><span data-stu-id="786e9-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="786e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="786e9-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="786e9-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786e9-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="786e9-128">-RoleName</span></span>
<span data-ttu-id="786e9-129">Berechnen sie die Rolle, anhand der Ereignisse ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="786e9-129">Compute role against which events will be raised.</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786e9-130">-Schedule</span><span class="sxs-lookup"><span data-stu-id="786e9-130">-Schedule</span></span>
<span data-ttu-id="786e9-131">Regelmäßige Häufigkeit, mit der ein Timerereignis ausgelöst werden muss.</span><span class="sxs-lookup"><span data-stu-id="786e9-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="786e9-132">Geben Sie einen Zeitplan in Tagen (zwischen 1 und 365), Stunden (zwischen 1 und 23) oder Minuten (zwischen 1 und 59) an.</span><span class="sxs-lookup"><span data-stu-id="786e9-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786e9-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="786e9-133">-ShareId</span></span>
<span data-ttu-id="786e9-134">Im FileEvent Trigger zu übergebende Dateifreigabe-ID</span><span class="sxs-lookup"><span data-stu-id="786e9-134">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786e9-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="786e9-135">-ShareName</span></span>
<span data-ttu-id="786e9-136">Im FileEvent Trigger zu übergebende Dateifreigabe-ID</span><span class="sxs-lookup"><span data-stu-id="786e9-136">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786e9-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="786e9-137">-StartTime</span></span>
<span data-ttu-id="786e9-138">Die Tageszeit, die zu einem gültigen Auslöser führt.</span><span class="sxs-lookup"><span data-stu-id="786e9-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="786e9-139">Der Zeitplan wird mit einem Bezug auf die bis zu Sekunden angegebene Zeit berechnet.</span><span class="sxs-lookup"><span data-stu-id="786e9-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="786e9-140">Wenn keine Zeitzone angegeben wird, wird die Uhrzeit als in der Gerätezeitzone betrachtet.</span><span class="sxs-lookup"><span data-stu-id="786e9-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="786e9-141">Der Wert wird immer als UTC zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="786e9-141">The value will always be returned as UTC time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786e9-142">-Topic</span><span class="sxs-lookup"><span data-stu-id="786e9-142">-Topic</span></span>
<span data-ttu-id="786e9-143">Thema, in dem regelmäßige Ereignisse auf einem IoT-Gerät veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="786e9-143">Topic where periodic events are published to IoT device.</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786e9-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="786e9-144">-Confirm</span></span>
<span data-ttu-id="786e9-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="786e9-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="786e9-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="786e9-146">-WhatIf</span></span>
<span data-ttu-id="786e9-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="786e9-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="786e9-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="786e9-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="786e9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="786e9-149">CommonParameters</span></span>
<span data-ttu-id="786e9-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="786e9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="786e9-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="786e9-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="786e9-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="786e9-152">INPUTS</span></span>

### <span data-ttu-id="786e9-153">Keine</span><span class="sxs-lookup"><span data-stu-id="786e9-153">None</span></span>

## <span data-ttu-id="786e9-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="786e9-154">OUTPUTS</span></span>

### <span data-ttu-id="786e9-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="786e9-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="786e9-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="786e9-156">NOTES</span></span>

## <span data-ttu-id="786e9-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="786e9-157">RELATED LINKS</span></span>
