---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: b966f15cc42ffc61f7d88cd5a1855f31564742ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932715"
---
# <span data-ttu-id="f13e4-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="f13e4-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="f13e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f13e4-102">SYNOPSIS</span></span>
<span data-ttu-id="f13e4-103">Abrufen von Aktivitätsprotokollereignissen</span><span class="sxs-lookup"><span data-stu-id="f13e4-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="f13e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f13e4-104">SYNTAX</span></span>

### <span data-ttu-id="f13e4-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="f13e4-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f13e4-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f13e4-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f13e4-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f13e4-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f13e4-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f13e4-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f13e4-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="f13e4-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f13e4-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f13e4-110">DESCRIPTION</span></span>
<span data-ttu-id="f13e4-111">Das Get-AzActivityLog cmdlet ruft Aktivitätsprotokollereignisse ab.</span><span class="sxs-lookup"><span data-stu-id="f13e4-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="f13e4-112">Die Ereignisse können der aktuellen Abonnement-ID, Korrelations-ID, Ressourcengruppe, Ressourcen-ID oder Ressourcenanbieter zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f13e4-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="f13e4-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f13e4-113">EXAMPLES</span></span>

### <span data-ttu-id="f13e4-114">Beispiel 1: Erhalten eines Ereignisprotokolls nach Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="f13e4-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzActivityLog
```

<span data-ttu-id="f13e4-115">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind und 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="f13e4-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f13e4-116">Beispiel 2: Erhalten eines Ereignisprotokolls nach Abonnement-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f13e4-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="f13e4-117">Mit diesem Befehl werden mindestens 100 Ereignisse aufgeführt, die der Abonnement-ID des Benutzers zugeordnet sind und 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="f13e4-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f13e4-118">Beispiel 3: Erhalten eines Ereignisprotokolls nach Abonnement-ID mit einer Startzeit.</span><span class="sxs-lookup"><span data-stu-id="f13e4-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="f13e4-119">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die mit der Abonnement-ID des Benutzers verknüpft sind, die am oder nach dem 06.06.2017 um 10:30 Uhr Ortszeit stattgefunden haben, wenn dieses Datum/diese Uhrzeit nicht älter als 90 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="f13e4-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="f13e4-120">Beispiel 4: Erhalten eines Ereignisprotokolls nach Abonnement-ID mit einer Start- und Endzeit.</span><span class="sxs-lookup"><span data-stu-id="f13e4-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="f13e4-121">Dieser Befehl listet mindestens 1.000 der Ereignisse auf, die mit der Abonnement-ID des Benutzers verbunden sind, die am oder nach dem 04.04.2017 und vor dem 04.04.2017 und nach 2017-14T11:30 Ortszeit stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/uhrzeit ist, d. h.: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="f13e4-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="f13e4-122">Beispiel 5: Erhalten eines Ereignisprotokolls nach Korrelations-ID</span><span class="sxs-lookup"><span data-stu-id="f13e4-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="f13e4-123">Mit diesem Befehl werden mindestens 1.000 Ereignisse aufgeführt, die der angegebenen Korrelations-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="f13e4-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="f13e4-124">**HINWEIS:** Dies ist normalerweise nur ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f13e4-124">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="f13e4-125">Beispiel 6: Erhalten eines Ereignisprotokolls nach Korrelations-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f13e4-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="f13e4-126">Dieser Befehl listet mindestens 100 Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind und 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="f13e4-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="f13e4-127">**HINWEIS:** Dies ist normalerweise nur ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f13e4-127">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="f13e4-128">Beispiel 7: Erhalten eines Ereignisprotokolls nach Korrelations-ID und Startzeit</span><span class="sxs-lookup"><span data-stu-id="f13e4-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="f13e4-129">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach dem 2017-05-22T04:30:00 Ortszeit stattgefunden haben, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="f13e4-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="f13e4-130">**HINWEIS:** Dies ist normalerweise nur ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f13e4-130">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="f13e4-131">Beispiel 8: Erhalten eines Ereignisprotokolls nach Korrelations-ID mit Start- und Endzeit</span><span class="sxs-lookup"><span data-stu-id="f13e4-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="f13e4-132">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach dem 15.04.2017,04:30 Ortszeit, jedoch vor dem 2017-04-25T12:30 Ortszeit stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/Uhrzeit ist, d. h.: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="f13e4-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="f13e4-133">Beispiel 9: Erhalten eines Ereignisprotokolls für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f13e4-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="f13e4-134">Dieser Befehl listet mindestens 1000 Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind und 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="f13e4-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f13e4-135">Beispiel 10: Erhalten eines Ereignisprotokolls für eine Ressourcengruppe mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f13e4-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="f13e4-136">Dieser Befehl listet mindestens 100 Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="f13e4-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f13e4-137">Beispiel 11: Erhalten eines Ereignisprotokolls für eine Ressourcengruppe zur Startzeit</span><span class="sxs-lookup"><span data-stu-id="f13e4-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="f13e4-138">Dieser Befehl listet mindestens 1000 Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach dem 2017-05-22T04:30:00 Ortszeit stattgefunden haben, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="f13e4-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="f13e4-139">Beispiel 12: Erhalten eines Ereignisprotokolls für eine Ressourcengruppe mit einer Start- und Endzeit</span><span class="sxs-lookup"><span data-stu-id="f13e4-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="f13e4-140">Dieser Befehl listet mindestens 1000 Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach dem 04.04.2017,15.04.30 Ortszeit, jedoch vor dem 2017-04-25T12:30 Ortszeit stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/Uhrzeit ist, d. h.: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="f13e4-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="f13e4-141">Beispiel 13: Erhalten eines Ereignisprotokolls nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f13e4-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="f13e4-142">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="f13e4-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f13e4-143">Beispiel 14: Erhalten eines Ereignisprotokolls nach Ressourcen-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f13e4-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="f13e4-144">Dieser Befehl listet mindestens 100 Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="f13e4-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f13e4-145">Beispiel 15: Erhalten eines Ereignisprotokolls nach Ressourcen-ID mit einer Startzeit</span><span class="sxs-lookup"><span data-stu-id="f13e4-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="f13e4-146">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach dem 2017-05-22T04:30:00 Ortszeit stattgefunden haben, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="f13e4-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="f13e4-147">Beispiel 16: Erhalten eines Ereignisprotokolls nach Ressourcen-ID mit einer Start- und Endzeit</span><span class="sxs-lookup"><span data-stu-id="f13e4-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="f13e4-148">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach dem 15.04.2017,04:30 Ortszeit, jedoch vor dem 2017-04-25T12:30 Ortszeit stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/Uhrzeit ist, d. h.: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="f13e4-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="f13e4-149">Beispiel 17: Erhalten eines Ereignisprotokolls nach Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="f13e4-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="f13e4-150">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind und 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="f13e4-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f13e4-151">Beispiel 18: Erhalten eines Ereignisprotokolls nach Ressourcenanbieter mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f13e4-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="f13e4-152">Dieser Befehl listet mindestens 100 Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind und 7 Tage nach dem aktuellen Datum/der aktuellen Uhrzeit stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="f13e4-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f13e4-153">Beispiel 19: Erhalten eines Ereignisprotokolls nach Ressourcenanbieter mit einer Startzeit</span><span class="sxs-lookup"><span data-stu-id="f13e4-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="f13e4-154">Dieser Befehl listet mindestens 1000 Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, die am oder nach dem 2017-05-22T04:30:00 Ortszeit stattgefunden haben, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="f13e4-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="f13e4-155">Beispiel 20: Erhalten eines Ereignisprotokolls nach Ressourcenanbieter mit einer Start- und Endzeit</span><span class="sxs-lookup"><span data-stu-id="f13e4-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="f13e4-156">Dieser Befehl listet mindestens 1.000 Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, die am oder nach dem 15.04.2017,04:30 Ortszeit, jedoch vor dem 2017-04-25T12:30 Ortszeit stattgefunden haben, wenn der gesamte Datums-/Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/Uhrzeit ist, d. h.: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="f13e4-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="f13e4-157">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f13e4-157">PARAMETERS</span></span>

### <span data-ttu-id="f13e4-158">-Anrufer</span><span class="sxs-lookup"><span data-stu-id="f13e4-158">-Caller</span></span>
<span data-ttu-id="f13e4-159">Der Aufrufer der ereignisse, die abgerufen werden müssen</span><span class="sxs-lookup"><span data-stu-id="f13e4-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="f13e4-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="f13e4-160">-CorrelationId</span></span>
<span data-ttu-id="f13e4-161">Die Korrelations-Id</span><span class="sxs-lookup"><span data-stu-id="f13e4-161">The CorrelationId</span></span>

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

### <span data-ttu-id="f13e4-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f13e4-162">-DefaultProfile</span></span>
<span data-ttu-id="f13e4-163">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f13e4-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f13e4-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="f13e4-164">-DetailedOutput</span></span>
<span data-ttu-id="f13e4-165">Rückgabeobjekt mit allen Details der Ereignisse (standardmäßig werden nur einige Attribute, d. h. keine Details, zurückgeben)</span><span class="sxs-lookup"><span data-stu-id="f13e4-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

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

### <span data-ttu-id="f13e4-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f13e4-166">-EndTime</span></span>
<span data-ttu-id="f13e4-167">Die EndZeit der Abfrage</span><span class="sxs-lookup"><span data-stu-id="f13e4-167">The endTime of the query</span></span>

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

### <span data-ttu-id="f13e4-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="f13e4-168">-MaxRecord</span></span>
<span data-ttu-id="f13e4-169">Die maximale Anzahl von Datensätzen, die abgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f13e4-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="f13e4-170">Alias: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="f13e4-170">Alias: MaxRecords, MaxEvents</span></span>

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

### <span data-ttu-id="f13e4-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f13e4-171">-ResourceGroupName</span></span>
<span data-ttu-id="f13e4-172">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f13e4-172">The resource group name</span></span>

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

### <span data-ttu-id="f13e4-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f13e4-173">-ResourceId</span></span>
<span data-ttu-id="f13e4-174">Die ResourceId</span><span class="sxs-lookup"><span data-stu-id="f13e4-174">The ResourceId</span></span>

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

### <span data-ttu-id="f13e4-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f13e4-175">-ResourceProvider</span></span>
<span data-ttu-id="f13e4-176">Name des ResourceProviders</span><span class="sxs-lookup"><span data-stu-id="f13e4-176">The ResourceProvider name</span></span>

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

### <span data-ttu-id="f13e4-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f13e4-177">-StartTime</span></span>
<span data-ttu-id="f13e4-178">Die Korrelations-Id der Abfrage</span><span class="sxs-lookup"><span data-stu-id="f13e4-178">The correlationId of the query</span></span>

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

### <span data-ttu-id="f13e4-179">-Status</span><span class="sxs-lookup"><span data-stu-id="f13e4-179">-Status</span></span>
<span data-ttu-id="f13e4-180">Der Status der zu abrufende Ereignisse</span><span class="sxs-lookup"><span data-stu-id="f13e4-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="f13e4-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f13e4-181">CommonParameters</span></span>
<span data-ttu-id="f13e4-182">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f13e4-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f13e4-183">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f13e4-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f13e4-184">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f13e4-184">INPUTS</span></span>

### <span data-ttu-id="f13e4-185">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f13e4-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f13e4-186">System.String</span><span class="sxs-lookup"><span data-stu-id="f13e4-186">System.String</span></span>

### <span data-ttu-id="f13e4-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f13e4-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f13e4-188">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f13e4-188">System.Int32</span></span>

## <span data-ttu-id="f13e4-189">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f13e4-189">OUTPUTS</span></span>

### <span data-ttu-id="f13e4-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="f13e4-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="f13e4-191">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f13e4-191">NOTES</span></span>

## <span data-ttu-id="f13e4-192">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f13e4-192">RELATED LINKS</span></span>
