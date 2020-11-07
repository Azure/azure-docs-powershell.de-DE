---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
ms.openlocfilehash: f6d0181562d9d43c12fbcfd046350e9d930f2320
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845124"
---
# <span data-ttu-id="47b1c-101">Get-AzLog</span><span class="sxs-lookup"><span data-stu-id="47b1c-101">Get-AzLog</span></span>

## <span data-ttu-id="47b1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="47b1c-103">Abrufen von Aktivitätsprotokoll Ereignissen</span><span class="sxs-lookup"><span data-stu-id="47b1c-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="47b1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47b1c-104">SYNTAX</span></span>

### <span data-ttu-id="47b1c-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="47b1c-105">GetByCorrelationId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b1c-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="47b1c-106">GetByResourceId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b1c-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="47b1c-107">GetByResourceGroup</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceGroupName] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47b1c-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="47b1c-108">GetByResourceProvider</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47b1c-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="47b1c-109">GetBySubscription</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47b1c-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47b1c-110">DESCRIPTION</span></span>
<span data-ttu-id="47b1c-111">Das Cmdlet " **Get-AzLog** " ruft Aktivitätsprotokoll Ereignisse ab.</span><span class="sxs-lookup"><span data-stu-id="47b1c-111">The **Get-AzLog** cmdlet retrieve Activity Log events.</span></span>
<span data-ttu-id="47b1c-112">Die Ereignisse können der aktuellen Abonnement-ID, Korrelations-ID, Ressourcengruppe, Ressourcen-ID oder dem Ressourcenanbieter zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="47b1c-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="47b1c-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47b1c-113">EXAMPLES</span></span>

### <span data-ttu-id="47b1c-114">Beispiel 1: Abrufen eines Ereignisprotokolls nach Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="47b1c-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzLog
```

<span data-ttu-id="47b1c-115">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="47b1c-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="47b1c-116">Beispiel 2: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="47b1c-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -MaxRecord 100
```

<span data-ttu-id="47b1c-117">Dieser Befehl listet höchstens 100-Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="47b1c-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="47b1c-118">Beispiel 3: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit einer Startzeit</span><span class="sxs-lookup"><span data-stu-id="47b1c-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="47b1c-119">Dieser Befehl listet höchstens 1000-Ereignisse auf, die mit der Abonnement-ID des Benutzers verbunden sind, die am oder nach 2017-06-01T10:30 Ortszeit erfolgt ist, wenn dieses Datum/die Uhrzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="47b1c-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="47b1c-120">Beispiel 4: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="47b1c-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="47b1c-121">Dieser Befehl listet höchstens 1000 der Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die am oder nach 2017-04-01T10:30 Ortszeit und vor 2017-04-14T11:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="47b1c-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="47b1c-122">Beispiel 5: Abrufen eines Ereignisprotokolls nach Korrelations-ID</span><span class="sxs-lookup"><span data-stu-id="47b1c-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="47b1c-123">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="47b1c-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="47b1c-124">**Hinweis** : Dies ist normalerweise nur ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="47b1c-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="47b1c-125">Beispiel 6: Abrufen eines Ereignisprotokolls nach Korrelations-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="47b1c-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="47b1c-126">Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="47b1c-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="47b1c-127">**Hinweis** : Dies ist normalerweise nur ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="47b1c-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="47b1c-128">Beispiel 7: Abrufen eines Ereignisprotokolls nach Korrelations-ID und Startzeit</span><span class="sxs-lookup"><span data-stu-id="47b1c-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="47b1c-129">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit erfolgt ist, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="47b1c-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="47b1c-130">**Hinweis** : Dies ist normalerweise nur ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="47b1c-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="47b1c-131">Beispiel 8: Abrufen eines Ereignisprotokolls nach Korrelations-ID mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="47b1c-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="47b1c-132">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="47b1c-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="47b1c-133">Beispiel 9: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="47b1c-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="47b1c-134">Dieser Befehl listet höchstens 1000 die Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="47b1c-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="47b1c-135">Beispiel 10: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="47b1c-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="47b1c-136">Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="47b1c-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="47b1c-137">Beispiel 11: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe nach Anfangszeit</span><span class="sxs-lookup"><span data-stu-id="47b1c-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="47b1c-138">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit stattfand, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="47b1c-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="47b1c-139">Beispiel 12: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="47b1c-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="47b1c-140">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="47b1c-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="47b1c-141">Beispiel 13: Abrufen eines Ereignisprotokolls nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="47b1c-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="47b1c-142">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="47b1c-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="47b1c-143">Beispiel 14: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="47b1c-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="47b1c-144">Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="47b1c-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="47b1c-145">Beispiel 15: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit einer Startzeit</span><span class="sxs-lookup"><span data-stu-id="47b1c-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="47b1c-146">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit erfolgt, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="47b1c-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="47b1c-147">Beispiel 16: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="47b1c-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="47b1c-148">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="47b1c-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="47b1c-149">Beispiel 17: Abrufen eines Ereignisprotokolls nach dem Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="47b1c-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="47b1c-150">Dieser Befehl listet die meisten 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="47b1c-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="47b1c-151">Beispiel 18: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="47b1c-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="47b1c-152">Dieser Befehl listet die meisten 100-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="47b1c-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="47b1c-153">Beispiel 19: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit einer Startzeit</span><span class="sxs-lookup"><span data-stu-id="47b1c-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="47b1c-154">Dieser Befehl listet höchstens 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der sich am oder nach 2017-05-22T04:30:00 Ortszeit befindet, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="47b1c-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="47b1c-155">Beispiel 20: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="47b1c-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="47b1c-156">Dieser Befehl listet die meisten 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegen, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="47b1c-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="47b1c-157">Parameter</span><span class="sxs-lookup"><span data-stu-id="47b1c-157">PARAMETERS</span></span>

### <span data-ttu-id="47b1c-158">-Anrufer</span><span class="sxs-lookup"><span data-stu-id="47b1c-158">-Caller</span></span>
<span data-ttu-id="47b1c-159">Gibt einen Anrufer an.</span><span class="sxs-lookup"><span data-stu-id="47b1c-159">Specifies a caller.</span></span>

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

### <span data-ttu-id="47b1c-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="47b1c-160">-CorrelationId</span></span>
<span data-ttu-id="47b1c-161">Gibt die Korrelations-ID an.</span><span class="sxs-lookup"><span data-stu-id="47b1c-161">Specifies the correlation ID.</span></span>
<span data-ttu-id="47b1c-162">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47b1c-162">This parameter is required.</span></span>

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

### <span data-ttu-id="47b1c-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b1c-163">-DefaultProfile</span></span>
<span data-ttu-id="47b1c-164">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="47b1c-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47b1c-165">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="47b1c-165">-DetailedOutput</span></span>
<span data-ttu-id="47b1c-166">Gibt an, dass dieses Cmdlet eine detaillierte Ausgabe anzeigt.</span><span class="sxs-lookup"><span data-stu-id="47b1c-166">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="47b1c-167">Standardmäßig wird die Ausgabe zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="47b1c-167">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b1c-168">-EndTime</span><span class="sxs-lookup"><span data-stu-id="47b1c-168">-EndTime</span></span>
<span data-ttu-id="47b1c-169">Gibt die Endzeit der Abfrage in Ortszeit an.</span><span class="sxs-lookup"><span data-stu-id="47b1c-169">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="47b1c-170">Der Standardwert ist die aktuelle Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="47b1c-170">The default value is the current time.</span></span>
<span data-ttu-id="47b1c-171">Der Wert muss nach dem *Start* Zeitpunkt liegen.</span><span class="sxs-lookup"><span data-stu-id="47b1c-171">The value must be later than *StartTime*.</span></span>
<span data-ttu-id="47b1c-172">Sie können das Get-Date-Cmdlet verwenden, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="47b1c-172">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b1c-173">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="47b1c-173">-MaxRecord</span></span>
<span data-ttu-id="47b1c-174">Gibt die Gesamtanzahl der Datensätze an, die für den angegebenen Filter abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47b1c-174">Specifies the total number of records to fetch for the specified filter.</span></span>
<span data-ttu-id="47b1c-175">Der Standardwert ist 1000, und der maximal zulässige Wert ist 100000.</span><span class="sxs-lookup"><span data-stu-id="47b1c-175">The default value is 1000 and the maximum value accepted is 100000.</span></span> <span data-ttu-id="47b1c-176">Negative Werte und 0 werden ignoriert, und der Standardwert wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="47b1c-176">Negative values and 0 are ignored and the default value will be used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b1c-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b1c-177">-ResourceGroupName</span></span>
<span data-ttu-id="47b1c-178">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="47b1c-178">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="47b1c-179">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="47b1c-179">-ResourceId</span></span>
<span data-ttu-id="47b1c-180">Gibt die Ressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="47b1c-180">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="47b1c-181">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="47b1c-181">-ResourceProvider</span></span>
<span data-ttu-id="47b1c-182">Gibt einen Filter nach Ressourcenanbieter an.</span><span class="sxs-lookup"><span data-stu-id="47b1c-182">Specifies a filter by resource provider.</span></span>

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

### <span data-ttu-id="47b1c-183">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="47b1c-183">-StartTime</span></span>
<span data-ttu-id="47b1c-184">Gibt die Startzeit der Abfrage in Ortszeit an.</span><span class="sxs-lookup"><span data-stu-id="47b1c-184">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="47b1c-185">Der Standardwert ist *EndTime* minus sieben Tage.</span><span class="sxs-lookup"><span data-stu-id="47b1c-185">The default value is *EndTime* minus seven days.</span></span>
<span data-ttu-id="47b1c-186">Sie können das Get-Date-Cmdlet verwenden, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="47b1c-186">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b1c-187">-Status</span><span class="sxs-lookup"><span data-stu-id="47b1c-187">-Status</span></span>
<span data-ttu-id="47b1c-188">Gibt den Status an.</span><span class="sxs-lookup"><span data-stu-id="47b1c-188">Specifies the status.</span></span>

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

### <span data-ttu-id="47b1c-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b1c-189">CommonParameters</span></span>
<span data-ttu-id="47b1c-190">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b1c-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b1c-191">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47b1c-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b1c-192">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47b1c-192">INPUTS</span></span>

### <span data-ttu-id="47b1c-193">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="47b1c-193">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="47b1c-194">System. String</span><span class="sxs-lookup"><span data-stu-id="47b1c-194">System.String</span></span>

### <span data-ttu-id="47b1c-195">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="47b1c-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="47b1c-196">System. Int32</span><span class="sxs-lookup"><span data-stu-id="47b1c-196">System.Int32</span></span>

## <span data-ttu-id="47b1c-197">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47b1c-197">OUTPUTS</span></span>

### <span data-ttu-id="47b1c-198">Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="47b1c-198">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="47b1c-199">Notizen</span><span class="sxs-lookup"><span data-stu-id="47b1c-199">NOTES</span></span>

## <span data-ttu-id="47b1c-200">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47b1c-200">RELATED LINKS</span></span>
