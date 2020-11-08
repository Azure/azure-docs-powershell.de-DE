---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
ms.openlocfilehash: d13498df4c91c8d31b8bfe2e19e9f7fa23f99998
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165974"
---
# <span data-ttu-id="a89d0-101">New-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="a89d0-101">New-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="a89d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a89d0-102">SYNOPSIS</span></span>
<span data-ttu-id="a89d0-103">Konfiguriert einen Trigger auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="a89d0-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="a89d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a89d0-104">SYNTAX</span></span>

### <span data-ttu-id="a89d0-105">FileEventTriggerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a89d0-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a89d0-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="a89d0-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>] -Schedule <String>
 -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89d0-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a89d0-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89d0-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a89d0-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a89d0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a89d0-109">DESCRIPTION</span></span>
<span data-ttu-id="a89d0-110">Das Cmdlet **New-AzStackEdgeTrigger** konfiguriert einen Trigger auf dem Stack-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="a89d0-110">The **New-AzStackEdgeTrigger** cmdlet configures a trigger on the Stack Edge device.</span></span> 

## <span data-ttu-id="a89d0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a89d0-111">EXAMPLES</span></span>

### <span data-ttu-id="a89d0-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a89d0-112">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="a89d0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a89d0-113">PARAMETERS</span></span>

### <span data-ttu-id="a89d0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a89d0-114">-AsJob</span></span>
<span data-ttu-id="a89d0-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a89d0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a89d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a89d0-116">-DefaultProfile</span></span>
<span data-ttu-id="a89d0-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a89d0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a89d0-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a89d0-118">-DeviceName</span></span>
<span data-ttu-id="a89d0-119">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="a89d0-119">Device Name</span></span>

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

### <span data-ttu-id="a89d0-120">-Fileevent</span><span class="sxs-lookup"><span data-stu-id="a89d0-120">-FileEvent</span></span>
<span data-ttu-id="a89d0-121">Übergeben Sie diesen Schalterparameter, um fileevent-Trigger zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a89d0-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

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

### <span data-ttu-id="a89d0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a89d0-122">-Name</span></span>
<span data-ttu-id="a89d0-123">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="a89d0-123">Resource Name</span></span>

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

### <span data-ttu-id="a89d0-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="a89d0-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="a89d0-125">Übergeben Sie diesen Schalterparameter, um PeriodicTimerEvent-Trigger zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a89d0-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

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

### <span data-ttu-id="a89d0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a89d0-126">-ResourceGroupName</span></span>
<span data-ttu-id="a89d0-127">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a89d0-127">Resource Group Name</span></span>

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

### <span data-ttu-id="a89d0-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="a89d0-128">-RoleName</span></span>
<span data-ttu-id="a89d0-129">Compute-Rolle, mit der Ereignisse ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="a89d0-129">Compute role against which events will be raised.</span></span>

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

### <span data-ttu-id="a89d0-130">-Terminplan</span><span class="sxs-lookup"><span data-stu-id="a89d0-130">-Schedule</span></span>
<span data-ttu-id="a89d0-131">Regelmäßige Häufigkeit, mit der das Timer-Ereignis ausgelöst werden muss.</span><span class="sxs-lookup"><span data-stu-id="a89d0-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="a89d0-132">Geben Sie einen Terminplan in beiden Tagen (zwischen 1 und 365), Stunden (zwischen 1 und 23) oder Minuten (zwischen 1 und 59) an.</span><span class="sxs-lookup"><span data-stu-id="a89d0-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

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

### <span data-ttu-id="a89d0-133">-Freigabe-Nr</span><span class="sxs-lookup"><span data-stu-id="a89d0-133">-ShareId</span></span>
<span data-ttu-id="a89d0-134">Dateifreigabe-ID, die in fileevent-Trigger übergeben werden soll</span><span class="sxs-lookup"><span data-stu-id="a89d0-134">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="a89d0-135">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="a89d0-135">-ShareName</span></span>
<span data-ttu-id="a89d0-136">Dateifreigabe-ID, die in fileevent-Trigger übergeben werden soll</span><span class="sxs-lookup"><span data-stu-id="a89d0-136">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="a89d0-137">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="a89d0-137">-StartTime</span></span>
<span data-ttu-id="a89d0-138">Die Tageszeit, die zu einem gültigen Trigger führt.</span><span class="sxs-lookup"><span data-stu-id="a89d0-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="a89d0-139">Der Terminplan wird mit Bezug auf die bis zu Sekunden angegebene Zeit berechnet.</span><span class="sxs-lookup"><span data-stu-id="a89d0-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="a89d0-140">Wenn timezone nicht angegeben wird, wird die Zeit in der Geräte Zeitzone berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a89d0-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="a89d0-141">Der Wert wird immer als UTC-Zeit zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a89d0-141">The value will always be returned as UTC time.</span></span>

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

### <span data-ttu-id="a89d0-142">-Topic</span><span class="sxs-lookup"><span data-stu-id="a89d0-142">-Topic</span></span>
<span data-ttu-id="a89d0-143">Thema, in dem Periodische Ereignisse auf dem Gerät "viel" veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="a89d0-143">Topic where periodic events are published to IoT device.</span></span>

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

### <span data-ttu-id="a89d0-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a89d0-144">-Confirm</span></span>
<span data-ttu-id="a89d0-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a89d0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a89d0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a89d0-146">-WhatIf</span></span>
<span data-ttu-id="a89d0-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a89d0-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a89d0-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a89d0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a89d0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89d0-149">CommonParameters</span></span>
<span data-ttu-id="a89d0-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a89d0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89d0-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a89d0-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89d0-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a89d0-152">INPUTS</span></span>

### <span data-ttu-id="a89d0-153">Keine</span><span class="sxs-lookup"><span data-stu-id="a89d0-153">None</span></span>

## <span data-ttu-id="a89d0-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a89d0-154">OUTPUTS</span></span>

### <span data-ttu-id="a89d0-155">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="a89d0-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="a89d0-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="a89d0-156">NOTES</span></span>

## <span data-ttu-id="a89d0-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a89d0-157">RELATED LINKS</span></span>
