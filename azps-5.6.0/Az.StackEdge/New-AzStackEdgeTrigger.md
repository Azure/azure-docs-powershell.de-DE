---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
ms.openlocfilehash: 4303e824d218082bfc85391ac834e2764a485fcb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945551"
---
# <span data-ttu-id="f28ca-101">New-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="f28ca-101">New-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="f28ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f28ca-102">SYNOPSIS</span></span>
<span data-ttu-id="f28ca-103">Konfiguriert einen Trigger auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="f28ca-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="f28ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f28ca-104">SYNTAX</span></span>

### <span data-ttu-id="f28ca-105">FileEventTriggerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f28ca-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f28ca-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="f28ca-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>] -Schedule <String>
 -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f28ca-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f28ca-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f28ca-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f28ca-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f28ca-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f28ca-109">DESCRIPTION</span></span>
<span data-ttu-id="f28ca-110">Das **Cmdlet New-AzStackEdgeTrigger** konfiguriert einen Trigger auf dem Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="f28ca-110">The **New-AzStackEdgeTrigger** cmdlet configures a trigger on the Stack Edge device.</span></span> 

## <span data-ttu-id="f28ca-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f28ca-111">EXAMPLES</span></span>

### <span data-ttu-id="f28ca-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f28ca-112">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="f28ca-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f28ca-113">PARAMETERS</span></span>

### <span data-ttu-id="f28ca-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f28ca-114">-AsJob</span></span>
<span data-ttu-id="f28ca-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f28ca-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f28ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f28ca-116">-DefaultProfile</span></span>
<span data-ttu-id="f28ca-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f28ca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f28ca-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f28ca-118">-DeviceName</span></span>
<span data-ttu-id="f28ca-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="f28ca-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f28ca-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="f28ca-120">-FileEvent</span></span>
<span data-ttu-id="f28ca-121">Übergeben Sie diesen Parameter zum Konfigurieren von FileEvent Trigger.</span><span class="sxs-lookup"><span data-stu-id="f28ca-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

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

### <span data-ttu-id="f28ca-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f28ca-122">-Name</span></span>
<span data-ttu-id="f28ca-123">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="f28ca-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f28ca-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="f28ca-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="f28ca-125">Übergeben Sie diesen Parameter zum Konfigurieren des PeriodicTimerEvent-Triggers.</span><span class="sxs-lookup"><span data-stu-id="f28ca-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

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

### <span data-ttu-id="f28ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f28ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="f28ca-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f28ca-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f28ca-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="f28ca-128">-RoleName</span></span>
<span data-ttu-id="f28ca-129">Berechnen Sie die Rolle, anhand derer Ereignisse ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="f28ca-129">Compute role against which events will be raised.</span></span>

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

### <span data-ttu-id="f28ca-130">-Zeitplan</span><span class="sxs-lookup"><span data-stu-id="f28ca-130">-Schedule</span></span>
<span data-ttu-id="f28ca-131">Periodische Häufigkeit, bei der das Timerereignis ausgelöst werden muss.</span><span class="sxs-lookup"><span data-stu-id="f28ca-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="f28ca-132">Geben Sie einen Zeitplan entweder in Tagen (zwischen 1 und 365), Stunden (zwischen 1 und 23) oder Minuten (zwischen 1 und 59) an.</span><span class="sxs-lookup"><span data-stu-id="f28ca-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

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

### <span data-ttu-id="f28ca-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="f28ca-133">-ShareId</span></span>
<span data-ttu-id="f28ca-134">Dateifreigabe-ID, die im FileEvent-Trigger übergeben werden soll</span><span class="sxs-lookup"><span data-stu-id="f28ca-134">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="f28ca-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f28ca-135">-ShareName</span></span>
<span data-ttu-id="f28ca-136">Dateifreigabe-ID, die im FileEvent-Trigger übergeben werden soll</span><span class="sxs-lookup"><span data-stu-id="f28ca-136">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="f28ca-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f28ca-137">-StartTime</span></span>
<span data-ttu-id="f28ca-138">Die Uhrzeit des Tages, die zu einem gültigen Trigger führt.</span><span class="sxs-lookup"><span data-stu-id="f28ca-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="f28ca-139">Der Zeitplan wird mit Bezug auf die bis zu Sekunden angegebene Zeit berechnet.</span><span class="sxs-lookup"><span data-stu-id="f28ca-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="f28ca-140">Wird keine Zeitzone angegeben, wird die Uhrzeit als in der Gerätezeitzone betrachtet.</span><span class="sxs-lookup"><span data-stu-id="f28ca-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="f28ca-141">Der Wert wird immer als UTC-Uhrzeit zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f28ca-141">The value will always be returned as UTC time.</span></span>

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

### <span data-ttu-id="f28ca-142">-Topic</span><span class="sxs-lookup"><span data-stu-id="f28ca-142">-Topic</span></span>
<span data-ttu-id="f28ca-143">Thema, in dem periodische Ereignisse auf einem IoT-Gerät veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="f28ca-143">Topic where periodic events are published to IoT device.</span></span>

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

### <span data-ttu-id="f28ca-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f28ca-144">-Confirm</span></span>
<span data-ttu-id="f28ca-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f28ca-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f28ca-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f28ca-146">-WhatIf</span></span>
<span data-ttu-id="f28ca-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f28ca-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f28ca-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f28ca-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f28ca-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f28ca-149">CommonParameters</span></span>
<span data-ttu-id="f28ca-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f28ca-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f28ca-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f28ca-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f28ca-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f28ca-152">INPUTS</span></span>

### <span data-ttu-id="f28ca-153">Keine</span><span class="sxs-lookup"><span data-stu-id="f28ca-153">None</span></span>

## <span data-ttu-id="f28ca-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f28ca-154">OUTPUTS</span></span>

### <span data-ttu-id="f28ca-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="f28ca-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="f28ca-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f28ca-156">NOTES</span></span>

## <span data-ttu-id="f28ca-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f28ca-157">RELATED LINKS</span></span>
