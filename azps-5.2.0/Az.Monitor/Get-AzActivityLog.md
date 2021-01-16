---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300064"
---
# <span data-ttu-id="78a40-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="78a40-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="78a40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78a40-102">SYNOPSIS</span></span>
<span data-ttu-id="78a40-103">Rufen Sie Aktivitätsprotokollereignisse ab.</span><span class="sxs-lookup"><span data-stu-id="78a40-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="78a40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78a40-104">SYNTAX</span></span>

### <span data-ttu-id="78a40-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="78a40-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78a40-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="78a40-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78a40-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="78a40-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78a40-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="78a40-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78a40-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="78a40-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78a40-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78a40-110">DESCRIPTION</span></span>
<span data-ttu-id="78a40-111">Das Get-AzActivityLog cmdlet ruft Aktivitätsprotokollereignisse ab.</span><span class="sxs-lookup"><span data-stu-id="78a40-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="78a40-112">Die Ereignisse können der aktuellen Abonnement-ID, Korrelations-ID, Ressourcengruppe, Ressourcen-ID oder Ressourcenanbieter zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="78a40-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="78a40-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="78a40-113">EXAMPLES</span></span>

### <span data-ttu-id="78a40-114">Beispiel 1: Erhalten eines Ereignisprotokolls nach Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="78a40-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="78a40-115">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind und sieben Tage ab dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="78a40-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="78a40-116">Beispiel 2: Erhalten eines Ereignisprotokolls nach Abonnement-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="78a40-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="78a40-117">Dieser Befehl listet mindestens 100 Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind und sieben Tage ab dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="78a40-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="78a40-118">Beispiel 3: Erhalten eines Ereignisprotokolls nach Abonnement-ID mit einer Startzeit.</span><span class="sxs-lookup"><span data-stu-id="78a40-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="78a40-119">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die mit der Abonnement-ID des Benutzers verbunden sind, die am oder nach dem 06.06.2010:30 Ortszeit stattgefunden haben, wenn dieses Datum/diese Uhrzeit nicht mehr als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit liegt.</span><span class="sxs-lookup"><span data-stu-id="78a40-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="78a40-120">Beispiel 4: Erhalten eines Ereignisprotokolls nach Abonnement-ID mit einer Start- und Endzeit.</span><span class="sxs-lookup"><span data-stu-id="78a40-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="78a40-121">Dieser Befehl listet mindestens 1.000 der Ereignisse im Zusammenhang mit der Abonnement-ID des Benutzers auf, die am oder nach dem 04.04.2010:30 (Ortszeit) und vor dem 04.04.2017 und 14.04.2013 (Ortszeit) stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, d. h. der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="78a40-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="78a40-122">Beispiel 5: Erhalten eines Ereignisprotokolls nach Korrelations-ID</span><span class="sxs-lookup"><span data-stu-id="78a40-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="78a40-123">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="78a40-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="78a40-124">**HINWEIS:** Dies ist normalerweise nur ein Einziges Ereignis.</span><span class="sxs-lookup"><span data-stu-id="78a40-124">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="78a40-125">Beispiel 6: Erhalten eines Ereignisprotokolls nach Korrelations-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="78a40-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="78a40-126">Dieser Befehl listet mindestens 100 Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind und sieben Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="78a40-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="78a40-127">**HINWEIS:** Dies ist normalerweise nur ein Einziges Ereignis.</span><span class="sxs-lookup"><span data-stu-id="78a40-127">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="78a40-128">Beispiel 7: Erhalten eines Ereignisprotokolls nach Korrelations-ID und Startzeit</span><span class="sxs-lookup"><span data-stu-id="78a40-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="78a40-129">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach dem 05.05.2004:30:00 Ortszeit stattgefunden haben, wenn die Startzeit nicht mehr als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit liegt.</span><span class="sxs-lookup"><span data-stu-id="78a40-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="78a40-130">**HINWEIS:** Dies ist normalerweise nur ein Einziges Ereignis.</span><span class="sxs-lookup"><span data-stu-id="78a40-130">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="78a40-131">Beispiel 8: Erhalten eines Ereignisprotokolls nach Korrelations-ID mit Start- und Endzeit</span><span class="sxs-lookup"><span data-stu-id="78a40-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="78a40-132">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach 2017-04-15T04:30 lokaler Zeit, aber vor dem 04.04.2012:30, stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, d. h. der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="78a40-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="78a40-133">Beispiel 9: Erhalten eines Ereignisprotokolls für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="78a40-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="78a40-134">Dieser Befehl listet mindestens 1.000 Der angegebenen Ressourcengruppe zugeordnete Ereignisse auf, die 7 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="78a40-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="78a40-135">Beispiel 10: Erhalten eines Ereignisprotokolls für eine Ressourcengruppe mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="78a40-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="78a40-136">Dieser Befehl listet mindestens 100 Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind und 7 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="78a40-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="78a40-137">Beispiel 11: Erhalten eines Ereignisprotokolls für eine Ressourcengruppe nach Startzeit</span><span class="sxs-lookup"><span data-stu-id="78a40-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="78a40-138">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind und die am oder nach dem 05.05.2004:30:00 Ortszeit stattgefunden haben, wenn die Startzeit nicht mehr als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit liegt.</span><span class="sxs-lookup"><span data-stu-id="78a40-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="78a40-139">Beispiel 12: Erhalten eines Ereignisprotokolls für eine Ressourcengruppe mit einer Start- und Endzeit</span><span class="sxs-lookup"><span data-stu-id="78a40-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="78a40-140">Dieser Befehl listet die meisten 1.000 Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind und die am oder nach dem 04.04.2017,15T04:30 lokal, jedoch vor dem 04.04.2012:30, stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, d. h. der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="78a40-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="78a40-141">Beispiel 13: Erhalten eines Ereignisprotokolls nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="78a40-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="78a40-142">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="78a40-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="78a40-143">Beispiel 14: Erhalten eines Ereignisprotokolls nach Ressourcen-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="78a40-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="78a40-144">Dieser Befehl listet mindestens 100 Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="78a40-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="78a40-145">Beispiel 15: Erhalten eines Ereignisprotokolls nach Ressourcen-ID mit Einer Startzeit</span><span class="sxs-lookup"><span data-stu-id="78a40-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="78a40-146">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach dem 05.05.2004:30:00 Ortszeit stattgefunden haben, wenn die Startzeit nicht mehr als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit liegt.</span><span class="sxs-lookup"><span data-stu-id="78a40-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="78a40-147">Beispiel 16: Erhalten eines Ereignisprotokolls nach Ressourcen-ID mit einer Start- und Endzeit</span><span class="sxs-lookup"><span data-stu-id="78a40-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="78a40-148">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach 2017-04-15T04:30 lokaler Zeit, aber vor dem 04.04.2012:30, stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, d. h. der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="78a40-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="78a40-149">Beispiel 17: Erhalten eines Ereignisprotokolls nach Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="78a40-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="78a40-150">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind und 7 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="78a40-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="78a40-151">Beispiel 18: Erhalten eines Ereignisprotokolls nach Ressourcenanbieter mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="78a40-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="78a40-152">Dieser Befehl listet mindestens 100 Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind und 7 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="78a40-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="78a40-153">Beispiel 19: Erhalten eines Ereignisprotokolls nach Ressourcenanbieter mit einer Startzeit</span><span class="sxs-lookup"><span data-stu-id="78a40-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="78a40-154">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind und die am oder nach dem 05.05.2004:30:00 Ortszeit stattgefunden haben, wenn die Startzeit nicht mehr als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit liegt.</span><span class="sxs-lookup"><span data-stu-id="78a40-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="78a40-155">Beispiel 20: Erhalten eines Ereignisprotokolls nach Ressourcenanbieter mit einer Start- und Endzeit</span><span class="sxs-lookup"><span data-stu-id="78a40-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="78a40-156">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, die am oder nach dem 04.04.2017,15T04:30 lokal, jedoch vor dem 04.04.2012:30, stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, d. h. der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="78a40-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="78a40-157">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78a40-157">PARAMETERS</span></span>

### <span data-ttu-id="78a40-158">-Caller</span><span class="sxs-lookup"><span data-stu-id="78a40-158">-Caller</span></span>
<span data-ttu-id="78a40-159">Der Aufrufer der zu rufende Ereignisse</span><span class="sxs-lookup"><span data-stu-id="78a40-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="78a40-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="78a40-160">-CorrelationId</span></span>
<span data-ttu-id="78a40-161">Die Korrelations-ID</span><span class="sxs-lookup"><span data-stu-id="78a40-161">The CorrelationId</span></span>

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

### <span data-ttu-id="78a40-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a40-162">-DefaultProfile</span></span>
<span data-ttu-id="78a40-163">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78a40-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78a40-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="78a40-164">-DetailedOutput</span></span>
<span data-ttu-id="78a40-165">Rückgabeobjekt mit allen Details der Ereignisse (standardmäßig werden nur einige Attribute, d. h. keine Details, zurückgeben)</span><span class="sxs-lookup"><span data-stu-id="78a40-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

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

### <span data-ttu-id="78a40-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="78a40-166">-EndTime</span></span>
<span data-ttu-id="78a40-167">Die EndZeit der Abfrage</span><span class="sxs-lookup"><span data-stu-id="78a40-167">The endTime of the query</span></span>

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

### <span data-ttu-id="78a40-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="78a40-168">-MaxRecord</span></span>
<span data-ttu-id="78a40-169">Die maximale Anzahl von datensätzen, die abgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="78a40-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="78a40-170">Alias: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="78a40-170">Alias: MaxRecords, MaxEvents</span></span>

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

### <span data-ttu-id="78a40-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a40-171">-ResourceGroupName</span></span>
<span data-ttu-id="78a40-172">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="78a40-172">The resource group name</span></span>

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

### <span data-ttu-id="78a40-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78a40-173">-ResourceId</span></span>
<span data-ttu-id="78a40-174">Die ResourceId</span><span class="sxs-lookup"><span data-stu-id="78a40-174">The ResourceId</span></span>

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

### <span data-ttu-id="78a40-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="78a40-175">-ResourceProvider</span></span>
<span data-ttu-id="78a40-176">Der Name von "ResourceProvider"</span><span class="sxs-lookup"><span data-stu-id="78a40-176">The ResourceProvider name</span></span>

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

### <span data-ttu-id="78a40-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="78a40-177">-StartTime</span></span>
<span data-ttu-id="78a40-178">Die Korrelations-ID der Abfrage</span><span class="sxs-lookup"><span data-stu-id="78a40-178">The correlationId of the query</span></span>

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

### <span data-ttu-id="78a40-179">-Status</span><span class="sxs-lookup"><span data-stu-id="78a40-179">-Status</span></span>
<span data-ttu-id="78a40-180">Der Status der zu rufende Ereignisse</span><span class="sxs-lookup"><span data-stu-id="78a40-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="78a40-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a40-181">CommonParameters</span></span>
<span data-ttu-id="78a40-182">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a40-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a40-183">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78a40-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a40-184">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="78a40-184">INPUTS</span></span>

### <span data-ttu-id="78a40-185">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="78a40-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="78a40-186">System.String</span><span class="sxs-lookup"><span data-stu-id="78a40-186">System.String</span></span>

### <span data-ttu-id="78a40-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="78a40-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="78a40-188">System.Int32</span><span class="sxs-lookup"><span data-stu-id="78a40-188">System.Int32</span></span>

## <span data-ttu-id="78a40-189">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="78a40-189">OUTPUTS</span></span>

### <span data-ttu-id="78a40-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="78a40-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="78a40-191">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="78a40-191">NOTES</span></span>

## <span data-ttu-id="78a40-192">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="78a40-192">RELATED LINKS</span></span>
