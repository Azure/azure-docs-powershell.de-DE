---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: d96ccfb2160d7121ffda4802a0fd8afa43ea4589
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936616"
---
# <span data-ttu-id="9f9d2-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="9f9d2-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="9f9d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f9d2-102">SYNOPSIS</span></span>
<span data-ttu-id="9f9d2-103">Erstellt einen Zeitplaneintrag.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="9f9d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f9d2-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f9d2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f9d2-105">DESCRIPTION</span></span>
<span data-ttu-id="9f9d2-106">Das **Cmdlet New-AzRedisCacheScheduleEntry** erstellt ein **PSScheduleEntry-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="9f9d2-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="9f9d2-107">Azure Redis Cache patch schedule cmdlets, z. B. das New-AzRedisCachePatchSchedule cmdlet, erfordern Die Zeitplanungseingabeobjekte.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="9f9d2-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f9d2-108">EXAMPLES</span></span>

### <span data-ttu-id="9f9d2-109">Beispiel 1: Erstellen eines Zeitplaneintrags für Wochenenden</span><span class="sxs-lookup"><span data-stu-id="9f9d2-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="9f9d2-110">Mit diesem Befehl wird ein **PSScheduleEntry-Objekt** erstellt, das einen Wochenendzeitplan darstellt, der die angegebene Startzeit und das angegebene Fenster enthält.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="9f9d2-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9f9d2-111">PARAMETERS</span></span>

### <span data-ttu-id="9f9d2-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="9f9d2-112">-DayOfWeek</span></span>
<span data-ttu-id="9f9d2-113">Gibt den Wochentag für den Terminplaneintrag an.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="9f9d2-114">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="9f9d2-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f9d2-115">Jeden Tag</span><span class="sxs-lookup"><span data-stu-id="9f9d2-115">Everyday</span></span> 
- <span data-ttu-id="9f9d2-116">Wochenende</span><span class="sxs-lookup"><span data-stu-id="9f9d2-116">Weekend</span></span> 
- <span data-ttu-id="9f9d2-117">Montag</span><span class="sxs-lookup"><span data-stu-id="9f9d2-117">Monday</span></span> 
- <span data-ttu-id="9f9d2-118">Dienstag</span><span class="sxs-lookup"><span data-stu-id="9f9d2-118">Tuesday</span></span> 
- <span data-ttu-id="9f9d2-119">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="9f9d2-119">Wednesday</span></span> 
- <span data-ttu-id="9f9d2-120">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="9f9d2-120">Thursday</span></span> 
- <span data-ttu-id="9f9d2-121">Freitag</span><span class="sxs-lookup"><span data-stu-id="9f9d2-121">Friday</span></span> 
- <span data-ttu-id="9f9d2-122">Samstag</span><span class="sxs-lookup"><span data-stu-id="9f9d2-122">Saturday</span></span> 
- <span data-ttu-id="9f9d2-123">Sonntag</span><span class="sxs-lookup"><span data-stu-id="9f9d2-123">Sunday</span></span>

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

### <span data-ttu-id="9f9d2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f9d2-124">-DefaultProfile</span></span>
<span data-ttu-id="9f9d2-125">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f9d2-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="9f9d2-126">-MaintenanceWindow</span></span>
<span data-ttu-id="9f9d2-127">Gibt den Zeitraum an, der für Updates zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-127">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="9f9d2-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="9f9d2-128">-StartHourUtc</span></span>
<span data-ttu-id="9f9d2-129">Gibt eine Stunde des Tages an, an dem der Zeitplan beginnt.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-129">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="9f9d2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f9d2-130">CommonParameters</span></span>
<span data-ttu-id="9f9d2-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f9d2-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f9d2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f9d2-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f9d2-133">INPUTS</span></span>

### <span data-ttu-id="9f9d2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9f9d2-134">System.String</span></span>

### <span data-ttu-id="9f9d2-135">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9f9d2-135">System.Int32</span></span>

### <span data-ttu-id="9f9d2-136">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9f9d2-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9f9d2-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f9d2-137">OUTPUTS</span></span>

### <span data-ttu-id="9f9d2-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="9f9d2-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="9f9d2-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9f9d2-139">NOTES</span></span>
* <span data-ttu-id="9f9d2-140">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="9f9d2-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="9f9d2-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9f9d2-141">RELATED LINKS</span></span>

[<span data-ttu-id="9f9d2-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9f9d2-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="9f9d2-143">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9f9d2-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="9f9d2-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9f9d2-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


