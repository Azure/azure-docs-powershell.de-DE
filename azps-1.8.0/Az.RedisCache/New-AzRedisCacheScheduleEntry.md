---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: 7f877b929cb5ccd171b76cd9131f33693a5f0906
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659747"
---
# <span data-ttu-id="e7980-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="e7980-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="e7980-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7980-102">SYNOPSIS</span></span>
<span data-ttu-id="e7980-103">Erstellt einen Terminplan Eintrag.</span><span class="sxs-lookup"><span data-stu-id="e7980-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="e7980-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7980-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7980-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7980-105">DESCRIPTION</span></span>
<span data-ttu-id="e7980-106">Mit dem Cmdlet **New-AzRedisCacheScheduleEntry** wird ein **PSScheduleEntry** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="e7980-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="e7980-107">Cmdlets des Azure-Cache-Cache-Patches, wie etwa das Cmdlet New-AzRedisCachePatchSchedule, erfordern zeitplaneintrags Objekte.</span><span class="sxs-lookup"><span data-stu-id="e7980-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="e7980-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7980-108">EXAMPLES</span></span>

### <span data-ttu-id="e7980-109">Beispiel 1: Erstellen eines Terminplan Eintrags für Wochenenden</span><span class="sxs-lookup"><span data-stu-id="e7980-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="e7980-110">Mit diesem Befehl wird ein **PSScheduleEntry** -Objekt erstellt, das einen Wochenend Zeitplan mit der angegebenen Startzeit und dem angegebenen Fenster darstellt.</span><span class="sxs-lookup"><span data-stu-id="e7980-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="e7980-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7980-111">PARAMETERS</span></span>

### <span data-ttu-id="e7980-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="e7980-112">-DayOfWeek</span></span>
<span data-ttu-id="e7980-113">Gibt den Tag der Woche für den Terminplan Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="e7980-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="e7980-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e7980-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7980-115">Alltags</span><span class="sxs-lookup"><span data-stu-id="e7980-115">Everyday</span></span> 
- <span data-ttu-id="e7980-116">Wochenend</span><span class="sxs-lookup"><span data-stu-id="e7980-116">Weekend</span></span> 
- <span data-ttu-id="e7980-117">Montag</span><span class="sxs-lookup"><span data-stu-id="e7980-117">Monday</span></span> 
- <span data-ttu-id="e7980-118">Dienstag</span><span class="sxs-lookup"><span data-stu-id="e7980-118">Tuesday</span></span> 
- <span data-ttu-id="e7980-119">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="e7980-119">Wednesday</span></span> 
- <span data-ttu-id="e7980-120">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="e7980-120">Thursday</span></span> 
- <span data-ttu-id="e7980-121">Freitag</span><span class="sxs-lookup"><span data-stu-id="e7980-121">Friday</span></span> 
- <span data-ttu-id="e7980-122">Samstag</span><span class="sxs-lookup"><span data-stu-id="e7980-122">Saturday</span></span> 
- <span data-ttu-id="e7980-123">Sonntag</span><span class="sxs-lookup"><span data-stu-id="e7980-123">Sunday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7980-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7980-124">-DefaultProfile</span></span>
<span data-ttu-id="e7980-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7980-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7980-126">-MaintenanceWindow "</span><span class="sxs-lookup"><span data-stu-id="e7980-126">-MaintenanceWindow</span></span>
<span data-ttu-id="e7980-127">Gibt an, wie viel Zeitfenster für Updates zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="e7980-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7980-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="e7980-128">-StartHourUtc</span></span>
<span data-ttu-id="e7980-129">Gibt eine Stunde des Tages an, an dem der Terminplan beginnt.</span><span class="sxs-lookup"><span data-stu-id="e7980-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7980-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7980-130">CommonParameters</span></span>
<span data-ttu-id="e7980-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7980-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7980-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7980-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7980-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7980-133">INPUTS</span></span>

### <span data-ttu-id="e7980-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e7980-134">System.String</span></span>

### <span data-ttu-id="e7980-135">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e7980-135">System.Int32</span></span>

### <span data-ttu-id="e7980-136">System. Nullable ' 1 [[System. TimeSpan, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e7980-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e7980-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7980-137">OUTPUTS</span></span>

### <span data-ttu-id="e7980-138">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="e7980-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="e7980-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7980-139">NOTES</span></span>
* <span data-ttu-id="e7980-140">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="e7980-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="e7980-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7980-141">RELATED LINKS</span></span>

[<span data-ttu-id="e7980-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="e7980-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="e7980-143">Neu – AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="e7980-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="e7980-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="e7980-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


