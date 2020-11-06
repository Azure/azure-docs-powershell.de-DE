---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 5c4375b4bb325877ec0520e0641496e8adfafec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476626"
---
# <span data-ttu-id="65d8a-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="65d8a-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="65d8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="65d8a-103">Fügt einen Patch-Zeitplan hinzu.</span><span class="sxs-lookup"><span data-stu-id="65d8a-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65d8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65d8a-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65d8a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65d8a-105">DESCRIPTION</span></span>
<span data-ttu-id="65d8a-106">Mit dem Cmdlet " **New-AzureRmRedisCachePatchSchedule** " wird ein Patch-Zeitplan zu einem Cache im Azure-Schlüssel-a-Cache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="65d8a-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="65d8a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65d8a-107">EXAMPLES</span></span>

### <span data-ttu-id="65d8a-108">Beispiel 1: Erstellen und Hinzufügen eines Patch-Zeitplans für einen Cache</span><span class="sxs-lookup"><span data-stu-id="65d8a-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="65d8a-109">Mit diesem Befehl wird dem Cache mit dem Namen RedisCache06 ein Patch-Zeitplan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="65d8a-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="65d8a-110">Der Parameter Entries nimmt als Wert einen Befehl auf, der zum Erstellen eines Zeitplans **New-AzureRmRedisCacheScheduleEntry** verwendet.</span><span class="sxs-lookup"><span data-stu-id="65d8a-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="65d8a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="65d8a-111">PARAMETERS</span></span>

### <span data-ttu-id="65d8a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d8a-112">-DefaultProfile</span></span>
<span data-ttu-id="65d8a-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65d8a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65d8a-114">-Einträge</span><span class="sxs-lookup"><span data-stu-id="65d8a-114">-Entries</span></span>
<span data-ttu-id="65d8a-115">Gibt ein Array von Zeitplänen an, die von diesem Cmdlet für einen Cache festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="65d8a-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="65d8a-116">Verwenden Sie das New-AzureRmRedisCacheScheduleEntry-Cmdlet, um ein **PSScheduleEntry** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="65d8a-116">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d8a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="65d8a-117">-Name</span></span>
<span data-ttu-id="65d8a-118">Gibt den Namen des Caches an.</span><span class="sxs-lookup"><span data-stu-id="65d8a-118">Specifies the name of the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d8a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d8a-119">-ResourceGroupName</span></span>
<span data-ttu-id="65d8a-120">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="65d8a-120">Specifies the name of the resource group which contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d8a-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65d8a-121">-Confirm</span></span>
<span data-ttu-id="65d8a-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65d8a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d8a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d8a-123">-WhatIf</span></span>
<span data-ttu-id="65d8a-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65d8a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65d8a-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65d8a-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d8a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d8a-126">CommonParameters</span></span>
<span data-ttu-id="65d8a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65d8a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d8a-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65d8a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d8a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65d8a-129">INPUTS</span></span>

### <span data-ttu-id="65d8a-130">Keine</span><span class="sxs-lookup"><span data-stu-id="65d8a-130">None</span></span>
<span data-ttu-id="65d8a-131">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="65d8a-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="65d8a-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65d8a-132">OUTPUTS</span></span>

### <span data-ttu-id="65d8a-133">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="65d8a-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="65d8a-134">Dieses Cmdlet gibt den Patch-Terminplan Eintrag zurück, der für den Cache eingestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="65d8a-134">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="65d8a-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="65d8a-135">NOTES</span></span>
* <span data-ttu-id="65d8a-136">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="65d8a-136">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="65d8a-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65d8a-137">RELATED LINKS</span></span>

[<span data-ttu-id="65d8a-138">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="65d8a-138">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="65d8a-139">Neu – AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="65d8a-139">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="65d8a-140">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="65d8a-140">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


