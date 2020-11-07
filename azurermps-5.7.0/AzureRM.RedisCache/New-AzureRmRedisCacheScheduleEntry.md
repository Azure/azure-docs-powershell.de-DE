---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 2f43cfa1e10fe115f8bf5fc94404f532f04f6573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662218"
---
# <span data-ttu-id="4334a-101">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="4334a-101">New-AzureRmRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="4334a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4334a-102">SYNOPSIS</span></span>
<span data-ttu-id="4334a-103">Erstellt einen Terminplan Eintrag.</span><span class="sxs-lookup"><span data-stu-id="4334a-103">Creates a schedule entry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4334a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4334a-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4334a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4334a-105">DESCRIPTION</span></span>
<span data-ttu-id="4334a-106">Mit dem Cmdlet **New-AzureRmRedisCacheScheduleEntry** wird ein **PSScheduleEntry** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="4334a-106">The **New-AzureRmRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="4334a-107">Cmdlets des Azure-Cache-Cache-Patches, wie etwa das Cmdlet New-AzureRmRedisCachePatchSchedule, erfordern zeitplaneintrags Objekte.</span><span class="sxs-lookup"><span data-stu-id="4334a-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzureRmRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="4334a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4334a-108">EXAMPLES</span></span>

### <span data-ttu-id="4334a-109">Beispiel 1: Erstellen eines Terminplan Eintrags für Wochenenden</span><span class="sxs-lookup"><span data-stu-id="4334a-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="4334a-110">Mit diesem Befehl wird ein **PSScheduleEntry** -Objekt erstellt, das einen Wochenend Zeitplan mit der angegebenen Startzeit und dem angegebenen Fenster darstellt.</span><span class="sxs-lookup"><span data-stu-id="4334a-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="4334a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4334a-111">PARAMETERS</span></span>

### <span data-ttu-id="4334a-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="4334a-112">-DayOfWeek</span></span>
<span data-ttu-id="4334a-113">Gibt den Tag der Woche für den Terminplan Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="4334a-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="4334a-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4334a-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4334a-115">Alltags</span><span class="sxs-lookup"><span data-stu-id="4334a-115">Everyday</span></span> 
- <span data-ttu-id="4334a-116">Wochenend</span><span class="sxs-lookup"><span data-stu-id="4334a-116">Weekend</span></span> 
- <span data-ttu-id="4334a-117">Montag</span><span class="sxs-lookup"><span data-stu-id="4334a-117">Monday</span></span> 
- <span data-ttu-id="4334a-118">Dienstag</span><span class="sxs-lookup"><span data-stu-id="4334a-118">Tuesday</span></span> 
- <span data-ttu-id="4334a-119">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="4334a-119">Wednesday</span></span> 
- <span data-ttu-id="4334a-120">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="4334a-120">Thursday</span></span> 
- <span data-ttu-id="4334a-121">Freitag</span><span class="sxs-lookup"><span data-stu-id="4334a-121">Friday</span></span> 
- <span data-ttu-id="4334a-122">Samstag</span><span class="sxs-lookup"><span data-stu-id="4334a-122">Saturday</span></span> 
- <span data-ttu-id="4334a-123">Sonntag</span><span class="sxs-lookup"><span data-stu-id="4334a-123">Sunday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4334a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4334a-124">-DefaultProfile</span></span>
<span data-ttu-id="4334a-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4334a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4334a-126">-MaintenanceWindow "</span><span class="sxs-lookup"><span data-stu-id="4334a-126">-MaintenanceWindow</span></span>
<span data-ttu-id="4334a-127">Gibt an, wie viel Zeitfenster für Updates zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="4334a-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4334a-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="4334a-128">-StartHourUtc</span></span>
<span data-ttu-id="4334a-129">Gibt eine Stunde des Tages an, an dem der Terminplan beginnt.</span><span class="sxs-lookup"><span data-stu-id="4334a-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4334a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4334a-130">CommonParameters</span></span>
<span data-ttu-id="4334a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4334a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4334a-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4334a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4334a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4334a-133">INPUTS</span></span>

### <span data-ttu-id="4334a-134">Keine</span><span class="sxs-lookup"><span data-stu-id="4334a-134">None</span></span>
<span data-ttu-id="4334a-135">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="4334a-135">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="4334a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4334a-136">OUTPUTS</span></span>

### <span data-ttu-id="4334a-137">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="4334a-137">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="4334a-138">Dieses Cmdlet gibt ein Schedule Entry-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4334a-138">This cmdlet returns a schedule entry object.</span></span>

## <span data-ttu-id="4334a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="4334a-139">NOTES</span></span>
* <span data-ttu-id="4334a-140">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="4334a-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="4334a-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4334a-141">RELATED LINKS</span></span>

[<span data-ttu-id="4334a-142">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="4334a-142">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="4334a-143">Neu – AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="4334a-143">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="4334a-144">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="4334a-144">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


