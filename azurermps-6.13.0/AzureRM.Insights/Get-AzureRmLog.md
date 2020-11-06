---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
ms.openlocfilehash: 90f65c7e3db862ca4d24b67187f587511593be4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496101"
---
# <span data-ttu-id="7ea56-101">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="7ea56-101">Get-AzureRmLog</span></span>

## <span data-ttu-id="7ea56-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ea56-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea56-103">Ruft ein Protokoll von Ereignissen ab.</span><span class="sxs-lookup"><span data-stu-id="7ea56-103">Gets a log of events.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea56-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ea56-104">SYNTAX</span></span>

### <span data-ttu-id="7ea56-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="7ea56-105">GetByCorrelationId</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ea56-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7ea56-106">GetByResourceId</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ea56-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7ea56-107">GetByResourceGroup</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ea56-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="7ea56-108">GetByResourceProvider</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ea56-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="7ea56-109">GetBySubscription</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ea56-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ea56-110">DESCRIPTION</span></span>
<span data-ttu-id="7ea56-111">Das Cmdlet " **Get-AzureRmLog** " Ruft ein Protokoll von Ereignissen ab.</span><span class="sxs-lookup"><span data-stu-id="7ea56-111">The **Get-AzureRmLog** cmdlet gets a log of events.</span></span>
<span data-ttu-id="7ea56-112">Die Ereignisse können der aktuellen Abonnement-ID, Korrelations-ID, Ressourcengruppe, Ressourcen-ID oder dem Ressourcenanbieter zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="7ea56-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="7ea56-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ea56-113">EXAMPLES</span></span>

### <span data-ttu-id="7ea56-114">Beispiel 1: Abrufen eines Ereignisprotokolls nach Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="7ea56-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzureRmLog
```

<span data-ttu-id="7ea56-115">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="7ea56-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="7ea56-116">Beispiel 2: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="7ea56-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -MaxEvents 100
```

<span data-ttu-id="7ea56-117">Dieser Befehl listet höchstens 100-Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="7ea56-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="7ea56-118">Beispiel 3: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit einer Startzeit</span><span class="sxs-lookup"><span data-stu-id="7ea56-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzureRmLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="7ea56-119">Dieser Befehl listet höchstens 1000-Ereignisse auf, die mit der Abonnement-ID des Benutzers verbunden sind, die am oder nach 2017-06-01T10:30 Ortszeit erfolgt ist, wenn dieses Datum/die Uhrzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="7ea56-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="7ea56-120">Beispiel 4: Abrufen eines Ereignisprotokolls nach Abonnement-ID mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="7ea56-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzureRmLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="7ea56-121">Dieser Befehl listet höchstens 1000 der Ereignisse auf, die der Abonnement-ID des Benutzers zugeordnet sind, die am oder nach 2017-04-01T10:30 Ortszeit und vor 2017-04-14T11:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="7ea56-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="7ea56-122">Beispiel 5: Abrufen eines Ereignisprotokolls nach Korrelations-ID</span><span class="sxs-lookup"><span data-stu-id="7ea56-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="7ea56-123">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="7ea56-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="7ea56-124">**Hinweis** : Dies ist normalerweise nur ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7ea56-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="7ea56-125">Beispiel 6: Abrufen eines Ereignisprotokolls nach Korrelations-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="7ea56-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxEvents 100
```

<span data-ttu-id="7ea56-126">Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="7ea56-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="7ea56-127">**Hinweis** : Dies ist normalerweise nur ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7ea56-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="7ea56-128">Beispiel 7: Abrufen eines Ereignisprotokolls nach Korrelations-ID und Startzeit</span><span class="sxs-lookup"><span data-stu-id="7ea56-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="7ea56-129">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit erfolgt ist, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="7ea56-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="7ea56-130">**Hinweis** : Dies ist normalerweise nur ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7ea56-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="7ea56-131">Beispiel 8: Abrufen eines Ereignisprotokolls nach Korrelations-ID mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="7ea56-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="7ea56-132">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Korrelations-ID zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="7ea56-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="7ea56-133">Beispiel 9: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7ea56-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="7ea56-134">Dieser Befehl listet höchstens 1000 die Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="7ea56-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="7ea56-135">Beispiel 10: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="7ea56-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -MaxEvents 100
```

<span data-ttu-id="7ea56-136">Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="7ea56-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="7ea56-137">Beispiel 11: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe nach Anfangszeit</span><span class="sxs-lookup"><span data-stu-id="7ea56-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="7ea56-138">Dieser Befehl listet höchstens 1000 Evetns auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit erfolgt, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="7ea56-138">This command lists at most 1000 evetns associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="7ea56-139">Beispiel 12: Abrufen eines Ereignisprotokolls für eine Ressourcengruppe mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="7ea56-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="7ea56-140">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcengruppe zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="7ea56-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="7ea56-141">Beispiel 13: Abrufen eines Ereignisprotokolls nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="7ea56-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="7ea56-142">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="7ea56-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="7ea56-143">Beispiel 14: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="7ea56-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxEvents 100
```

<span data-ttu-id="7ea56-144">Dieser Befehl listet höchstens 100-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="7ea56-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="7ea56-145">Beispiel 15: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit einer Startzeit</span><span class="sxs-lookup"><span data-stu-id="7ea56-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="7ea56-146">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach 2017-05-22T04:30:00 Ortszeit erfolgt, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="7ea56-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="7ea56-147">Beispiel 16: Abrufen eines Ereignisprotokolls nach Ressourcen-ID mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="7ea56-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="7ea56-148">Dieser Befehl listet höchstens 1000-Ereignisse auf, die der angegebenen Ressourcen-ID zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegt, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="7ea56-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="7ea56-149">Beispiel 17: Abrufen eines Ereignisprotokolls nach dem Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="7ea56-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="7ea56-150">Dieser Befehl listet die meisten 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="7ea56-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="7ea56-151">Beispiel 18: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit einer maximalen Anzahl von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="7ea56-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -MaxEvents 100
```

<span data-ttu-id="7ea56-152">Dieser Befehl listet die meisten 100-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der 7 Tage nach dem aktuellen Datum/der Uhrzeit stattfand.</span><span class="sxs-lookup"><span data-stu-id="7ea56-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="7ea56-153">Beispiel 19: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit einer Startzeit</span><span class="sxs-lookup"><span data-stu-id="7ea56-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="7ea56-154">Dieser Befehl listet höchstens 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, der sich am oder nach 2017-05-22T04:30:00 Ortszeit befindet, wenn die Startzeit nicht älter als 90 Tage ab dem aktuellen Datum/der Uhrzeit ist.</span><span class="sxs-lookup"><span data-stu-id="7ea56-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="7ea56-155">Beispiel 20: Abrufen eines Ereignisprotokolls nach Ressourcenanbieter mit Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="7ea56-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="7ea56-156">Dieser Befehl listet die meisten 1000-Ereignisse auf, die dem angegebenen Ressourcenanbieter zugeordnet sind, die am oder nach 2017-04-15T04:30 Ortszeit, aber vor 2017-04-25T12:30 Ortszeit liegen, wenn der gesamte Datums-und Uhrzeitbereich nicht älter als 90 Tage ab dem aktuellen Datum/der aktuellen Uhrzeit ist, also: der Aufbewahrungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="7ea56-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="7ea56-157">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ea56-157">PARAMETERS</span></span>

### <span data-ttu-id="7ea56-158">-Anrufer</span><span class="sxs-lookup"><span data-stu-id="7ea56-158">-Caller</span></span>
<span data-ttu-id="7ea56-159">Gibt einen Anrufer an.</span><span class="sxs-lookup"><span data-stu-id="7ea56-159">Specifies a caller.</span></span>

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

### <span data-ttu-id="7ea56-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="7ea56-160">-CorrelationId</span></span>
<span data-ttu-id="7ea56-161">Gibt die Korrelations-ID an.</span><span class="sxs-lookup"><span data-stu-id="7ea56-161">Specifies the correlation ID.</span></span>
<span data-ttu-id="7ea56-162">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7ea56-162">This parameter is required.</span></span>

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

### <span data-ttu-id="7ea56-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea56-163">-DefaultProfile</span></span>
<span data-ttu-id="7ea56-164">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7ea56-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea56-165">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="7ea56-165">-DetailedOutput</span></span>
<span data-ttu-id="7ea56-166">Gibt an, dass dieses Cmdlet eine detaillierte Ausgabe anzeigt.</span><span class="sxs-lookup"><span data-stu-id="7ea56-166">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="7ea56-167">Standardmäßig wird die Ausgabe zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="7ea56-167">By default, output is summarized.</span></span>

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

### <span data-ttu-id="7ea56-168">-EndTime</span><span class="sxs-lookup"><span data-stu-id="7ea56-168">-EndTime</span></span>
<span data-ttu-id="7ea56-169">Gibt die Endzeit der Abfrage in Ortszeit an.</span><span class="sxs-lookup"><span data-stu-id="7ea56-169">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="7ea56-170">Der Standardwert ist die aktuelle Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="7ea56-170">The default value is the current time.</span></span>
<span data-ttu-id="7ea56-171">Der Wert muss nach dem *Start* Zeitpunkt liegen.</span><span class="sxs-lookup"><span data-stu-id="7ea56-171">The value must be later than *StartTime*.</span></span>
<span data-ttu-id="7ea56-172">Sie können das Get-Date-Cmdlet verwenden, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7ea56-172">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

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

### <span data-ttu-id="7ea56-173">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="7ea56-173">-MaxRecord</span></span>
<span data-ttu-id="7ea56-174">Gibt die Gesamtanzahl der Datensätze an, die für den angegebenen Filter abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ea56-174">Specifies the total number of records to fetch for the specified filter.</span></span>
<span data-ttu-id="7ea56-175">Der Standardwert ist 1000, und der maximal zulässige Wert ist 100000.</span><span class="sxs-lookup"><span data-stu-id="7ea56-175">The default value is 1000 and the maximum value accepted is 100000.</span></span> <span data-ttu-id="7ea56-176">Negative Werte und 0 werden ignoriert, und der Standardwert wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ea56-176">Negative values and 0 are ignored and the default value will be used.</span></span>

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

### <span data-ttu-id="7ea56-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea56-177">-ResourceGroupName</span></span>
<span data-ttu-id="7ea56-178">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7ea56-178">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7ea56-179">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7ea56-179">-ResourceId</span></span>
<span data-ttu-id="7ea56-180">Gibt die Ressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="7ea56-180">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="7ea56-181">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="7ea56-181">-ResourceProvider</span></span>
<span data-ttu-id="7ea56-182">Gibt einen Filter nach Ressourcenanbieter an.</span><span class="sxs-lookup"><span data-stu-id="7ea56-182">Specifies a filter by resource provider.</span></span>

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

### <span data-ttu-id="7ea56-183">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="7ea56-183">-StartTime</span></span>
<span data-ttu-id="7ea56-184">Gibt die Startzeit der Abfrage in Ortszeit an.</span><span class="sxs-lookup"><span data-stu-id="7ea56-184">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="7ea56-185">Der Standardwert ist *EndTime* minus sieben Tage.</span><span class="sxs-lookup"><span data-stu-id="7ea56-185">The default value is *EndTime* minus seven days.</span></span>
<span data-ttu-id="7ea56-186">Sie können das Get-Date-Cmdlet verwenden, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7ea56-186">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

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

### <span data-ttu-id="7ea56-187">-Status</span><span class="sxs-lookup"><span data-stu-id="7ea56-187">-Status</span></span>
<span data-ttu-id="7ea56-188">Gibt den Status an.</span><span class="sxs-lookup"><span data-stu-id="7ea56-188">Specifies the status.</span></span>

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

### <span data-ttu-id="7ea56-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea56-189">CommonParameters</span></span>
<span data-ttu-id="7ea56-190">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea56-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea56-191">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea56-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea56-192">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ea56-192">INPUTS</span></span>

### <span data-ttu-id="7ea56-193">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7ea56-193">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7ea56-194">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea56-194">System.String</span></span>

### <span data-ttu-id="7ea56-195">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="7ea56-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7ea56-196">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7ea56-196">System.Int32</span></span>

## <span data-ttu-id="7ea56-197">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ea56-197">OUTPUTS</span></span>

### <span data-ttu-id="7ea56-198">Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="7ea56-198">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="7ea56-199">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ea56-199">NOTES</span></span>

## <span data-ttu-id="7ea56-200">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ea56-200">RELATED LINKS</span></span>
