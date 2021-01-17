---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 4215cf8450922a03f061abcc04022ee4e20950b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459651"
---
# <span data-ttu-id="9ec68-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9ec68-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="9ec68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ec68-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec68-103">Fügt einen Patchzeitplan hinzu.</span><span class="sxs-lookup"><span data-stu-id="9ec68-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="9ec68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ec68-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ec68-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ec68-105">DESCRIPTION</span></span>
<span data-ttu-id="9ec68-106">Das **Cmdlet "New-AzRedisCachePatchSchedule"** fügt einem Cache in Azure Redis Cache einen Patchzeitplan hinzu.</span><span class="sxs-lookup"><span data-stu-id="9ec68-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="9ec68-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ec68-107">EXAMPLES</span></span>

### <span data-ttu-id="9ec68-108">Beispiel 1: Erstellen und Hinzufügen eines Patchzeitplans in einem Cache</span><span class="sxs-lookup"><span data-stu-id="9ec68-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="9ec68-109">Mit diesem Befehl wird dem Cache mit dem Namen "RedisCache06" ein Patchzeitplan hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="9ec68-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="9ec68-110">Der Parameter "Entries" verwendet als Wert einen Befehl, der **"New-AzRedisCacheScheduleEntry"** zum Erstellen eines Zeitplans verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ec68-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="9ec68-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ec68-111">PARAMETERS</span></span>

### <span data-ttu-id="9ec68-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ec68-112">-DefaultProfile</span></span>
<span data-ttu-id="9ec68-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ec68-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ec68-114">-Entries</span><span class="sxs-lookup"><span data-stu-id="9ec68-114">-Entries</span></span>
<span data-ttu-id="9ec68-115">Gibt ein Array von Zeitplänen an, das von diesem Cmdlet für einen Cache festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9ec68-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="9ec68-116">Um ein **"PSScheduleEntry"-Objekt** zu erhalten, verwenden Sie das New-AzRedisCacheScheduleEntry-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ec68-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="9ec68-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9ec68-117">-Name</span></span>
<span data-ttu-id="9ec68-118">Gibt den Namen des Caches an.</span><span class="sxs-lookup"><span data-stu-id="9ec68-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="9ec68-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec68-119">-ResourceGroupName</span></span>
<span data-ttu-id="9ec68-120">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="9ec68-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="9ec68-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ec68-121">-Confirm</span></span>
<span data-ttu-id="9ec68-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ec68-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ec68-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9ec68-123">-WhatIf</span></span>
<span data-ttu-id="9ec68-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ec68-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ec68-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ec68-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ec68-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ec68-126">CommonParameters</span></span>
<span data-ttu-id="9ec68-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ec68-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ec68-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ec68-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ec68-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ec68-129">INPUTS</span></span>

### <span data-ttu-id="9ec68-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9ec68-130">System.String</span></span>

### <span data-ttu-id="9ec68-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span><span class="sxs-lookup"><span data-stu-id="9ec68-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="9ec68-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ec68-132">OUTPUTS</span></span>

### <span data-ttu-id="9ec68-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="9ec68-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="9ec68-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9ec68-134">NOTES</span></span>
* <span data-ttu-id="9ec68-135">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="9ec68-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="9ec68-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9ec68-136">RELATED LINKS</span></span>

[<span data-ttu-id="9ec68-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9ec68-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="9ec68-138">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="9ec68-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="9ec68-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9ec68-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


