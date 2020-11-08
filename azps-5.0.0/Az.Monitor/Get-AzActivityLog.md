---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178818"
---
# <span data-ttu-id="d626f-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="d626f-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="d626f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d626f-102">SYNOPSIS</span></span>
<span data-ttu-id="d626f-103">Abrufen von Aktivitätsprotokoll Ereignissen</span><span class="sxs-lookup"><span data-stu-id="d626f-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="d626f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d626f-104">SYNTAX</span></span>

### <span data-ttu-id="d626f-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="d626f-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d626f-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d626f-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d626f-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d626f-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d626f-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d626f-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d626f-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="d626f-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d626f-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d626f-110">DESCRIPTION</span></span>
<span data-ttu-id="d626f-111">Das Get-AzActivityLog-Cmdlet ruft Aktivitätsprotokoll Ereignisse ab.</span><span class="sxs-lookup"><span data-stu-id="d626f-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="d626f-112">Die Ereignisse können der aktuellen Abonnement-ID, Korrelations-ID, Ressourcengruppe, Ressourcen-ID oder dem Ressourcenanbieter zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="d626f-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="d626f-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d626f-113">EXAMPLES</span></span>

### <span data-ttu-id="d626f-114">Beispiel 1: Abrufen eines Ereignisprotokolls nach Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="d626f-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="d626f-115">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="d626f-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d626f-116">Beispiel 2: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="d626f-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="d626f-117">Dieser Befehl listet höchstens 100-Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="d626f-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d626f-118">Beispiel 3: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit einer Startzeit</span><span class="sxs-lookup"><span data-stu-id="d626f-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="d626f-119">Dieser Befehl listet höchstens 1000-Ereignisse auf, die mit der Abonnement-ID des Benutzers verbunden sind, die am oder nach 2017-06-01T10:30 Ortszeit erfolgt ist, wenn dieses Datum/die Uhrzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="d626f-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="d626f-120">Beispiel 4: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="d626f-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="d626f-121">Dieser Befehl listet höchstens 1000 der Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die am oder nach 2017-04-01T10:30 Ortszeit und vor 2017-04-14T11:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="d626f-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="d626f-122">Beispiel 5: Abrufen eines Ereignisprotokolls nach Korrelations-ID</span><span class="sxs-lookup"><span data-stu-id="d626f-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="d626f-123">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="d626f-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="d626f-124">**Hinweis** : Dies ist normalerweise nur ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d626f-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="d626f-125">Beispiel 6: Abrufen eines Ereignisprotokolls nach Korrelations-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="d626f-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="d626f-126">Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="d626f-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="d626f-127">**Hinweis** : Dies ist normalerweise nur ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d626f-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="d626f-128">Beispiel 7: Abrufen eines Ereignisprotokolls nach Korrelations-ID und Startzeit</span><span class="sxs-lookup"><span data-stu-id="d626f-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="d626f-129">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit erfolgt ist, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="d626f-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="d626f-130">**Hinweis** : Dies ist normalerweise nur ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d626f-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="d626f-131">Beispiel 8: Abrufen eines Ereignisprotokolls nach Korrelations-ID mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="d626f-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="d626f-132">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="d626f-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="d626f-133">Beispiel 9: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d626f-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="d626f-134">Dieser Befehl listet höchstens 1000 die Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="d626f-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d626f-135">Beispiel 10: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="d626f-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="d626f-136">Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="d626f-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d626f-137">Beispiel 11: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe nach Anfangszeit</span><span class="sxs-lookup"><span data-stu-id="d626f-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="d626f-138">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit stattfand, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="d626f-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="d626f-139">Beispiel 12: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="d626f-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="d626f-140">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="d626f-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="d626f-141">Beispiel 13: Abrufen eines Ereignisprotokolls nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d626f-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="d626f-142">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="d626f-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d626f-143">Beispiel 14: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="d626f-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="d626f-144">Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="d626f-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d626f-145">Beispiel 15: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit einer Startzeit</span><span class="sxs-lookup"><span data-stu-id="d626f-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="d626f-146">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit erfolgt, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="d626f-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="d626f-147">Beispiel 16: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="d626f-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="d626f-148">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="d626f-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="d626f-149">Beispiel 17: Abrufen eines Ereignisprotokolls nach dem Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="d626f-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="d626f-150">Dieser Befehl listet die meisten 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="d626f-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d626f-151">Beispiel 18: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="d626f-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="d626f-152">Dieser Befehl listet die meisten 100-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="d626f-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d626f-153">Beispiel 19: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit einer Startzeit</span><span class="sxs-lookup"><span data-stu-id="d626f-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="d626f-154">Dieser Befehl listet höchstens 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der sich am oder nach 2017-05-22T04:30:00 Ortszeit befindet, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="d626f-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="d626f-155">Beispiel 20: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="d626f-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="d626f-156">Dieser Befehl listet die meisten 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegen, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="d626f-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="d626f-157">Parameter</span><span class="sxs-lookup"><span data-stu-id="d626f-157">PARAMETERS</span></span>

### <span data-ttu-id="d626f-158">-Anrufer</span><span class="sxs-lookup"><span data-stu-id="d626f-158">-Caller</span></span>
<span data-ttu-id="d626f-159">Der Aufrufer des abzurufenden Ereignisses</span><span class="sxs-lookup"><span data-stu-id="d626f-159">The caller of the events to fetch</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d626f-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="d626f-160">-CorrelationId</span></span>
<span data-ttu-id="d626f-161">Die CorrelationId</span><span class="sxs-lookup"><span data-stu-id="d626f-161">The CorrelationId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d626f-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d626f-162">-DefaultProfile</span></span>
<span data-ttu-id="d626f-163">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d626f-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d626f-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="d626f-164">-DetailedOutput</span></span>
<span data-ttu-id="d626f-165">Gibt das Objekt mit allen Details der Ereignisse zurück (der Standardwert ist, nur einige Attribute zurückzugeben, also keine Details).</span><span class="sxs-lookup"><span data-stu-id="d626f-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d626f-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d626f-166">-EndTime</span></span>
<span data-ttu-id="d626f-167">Die EndTime der Abfrage</span><span class="sxs-lookup"><span data-stu-id="d626f-167">The endTime of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d626f-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="d626f-168">-MaxRecord</span></span>
<span data-ttu-id="d626f-169">Die maximale Anzahl von Datensätzen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d626f-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="d626f-170">Alias: maxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="d626f-170">Alias: MaxRecords, MaxEvents</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d626f-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d626f-171">-ResourceGroupName</span></span>
<span data-ttu-id="d626f-172">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d626f-172">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d626f-173">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d626f-173">-ResourceId</span></span>
<span data-ttu-id="d626f-174">Die Resourcen--Nr</span><span class="sxs-lookup"><span data-stu-id="d626f-174">The ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d626f-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d626f-175">-ResourceProvider</span></span>
<span data-ttu-id="d626f-176">Der Name des ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d626f-176">The ResourceProvider name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d626f-177">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="d626f-177">-StartTime</span></span>
<span data-ttu-id="d626f-178">Die CorrelationId der Abfrage</span><span class="sxs-lookup"><span data-stu-id="d626f-178">The correlationId of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d626f-179">-Status</span><span class="sxs-lookup"><span data-stu-id="d626f-179">-Status</span></span>
<span data-ttu-id="d626f-180">Der Status der abzurufenden Ereignisse</span><span class="sxs-lookup"><span data-stu-id="d626f-180">The status of the events to fetch</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d626f-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d626f-181">CommonParameters</span></span>
<span data-ttu-id="d626f-182">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d626f-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d626f-183">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d626f-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d626f-184">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d626f-184">INPUTS</span></span>

### <span data-ttu-id="d626f-185">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d626f-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d626f-186">System. String</span><span class="sxs-lookup"><span data-stu-id="d626f-186">System.String</span></span>

### <span data-ttu-id="d626f-187">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="d626f-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d626f-188">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d626f-188">System.Int32</span></span>

## <span data-ttu-id="d626f-189">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d626f-189">OUTPUTS</span></span>

### <span data-ttu-id="d626f-190">Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="d626f-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="d626f-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="d626f-191">NOTES</span></span>

## <span data-ttu-id="d626f-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d626f-192">RELATED LINKS</span></span>
