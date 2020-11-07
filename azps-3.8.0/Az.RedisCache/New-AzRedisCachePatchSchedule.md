---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 4215cf8450922a03f061abcc04022ee4e20950b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846955"
---
# <span data-ttu-id="0d794-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0d794-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="0d794-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d794-102">SYNOPSIS</span></span>
<span data-ttu-id="0d794-103">Fügt einen Patch-Zeitplan hinzu.</span><span class="sxs-lookup"><span data-stu-id="0d794-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="0d794-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d794-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d794-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d794-105">DESCRIPTION</span></span>
<span data-ttu-id="0d794-106">Mit dem Cmdlet " **New-AzRedisCachePatchSchedule** " wird ein Patch-Zeitplan zu einem Cache im Azure-Schlüssel-a-Cache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0d794-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="0d794-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d794-107">EXAMPLES</span></span>

### <span data-ttu-id="0d794-108">Beispiel 1: Erstellen und Hinzufügen eines Patch-Zeitplans für einen Cache</span><span class="sxs-lookup"><span data-stu-id="0d794-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="0d794-109">Mit diesem Befehl wird dem Cache mit dem Namen RedisCache06 ein Patch-Zeitplan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0d794-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="0d794-110">Der Parameter Entries nimmt als Wert einen Befehl auf, der zum Erstellen eines Zeitplans **New-AzRedisCacheScheduleEntry** verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d794-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="0d794-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d794-111">PARAMETERS</span></span>

### <span data-ttu-id="0d794-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d794-112">-DefaultProfile</span></span>
<span data-ttu-id="0d794-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d794-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d794-114">-Einträge</span><span class="sxs-lookup"><span data-stu-id="0d794-114">-Entries</span></span>
<span data-ttu-id="0d794-115">Gibt ein Array von Zeitplänen an, die von diesem Cmdlet für einen Cache festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0d794-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="0d794-116">Verwenden Sie das New-AzRedisCacheScheduleEntry-Cmdlet, um ein **PSScheduleEntry** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0d794-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d794-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0d794-117">-Name</span></span>
<span data-ttu-id="0d794-118">Gibt den Namen des Caches an.</span><span class="sxs-lookup"><span data-stu-id="0d794-118">Specifies the name of the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d794-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d794-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d794-120">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="0d794-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="0d794-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d794-121">-Confirm</span></span>
<span data-ttu-id="0d794-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d794-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d794-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d794-123">-WhatIf</span></span>
<span data-ttu-id="0d794-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d794-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d794-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d794-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d794-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d794-126">CommonParameters</span></span>
<span data-ttu-id="0d794-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d794-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d794-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d794-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d794-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d794-129">INPUTS</span></span>

### <span data-ttu-id="0d794-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0d794-130">System.String</span></span>

### <span data-ttu-id="0d794-131">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry []</span><span class="sxs-lookup"><span data-stu-id="0d794-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="0d794-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d794-132">OUTPUTS</span></span>

### <span data-ttu-id="0d794-133">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="0d794-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="0d794-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d794-134">NOTES</span></span>
* <span data-ttu-id="0d794-135">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="0d794-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="0d794-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d794-136">RELATED LINKS</span></span>

[<span data-ttu-id="0d794-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0d794-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="0d794-138">Neu – AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="0d794-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="0d794-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0d794-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


