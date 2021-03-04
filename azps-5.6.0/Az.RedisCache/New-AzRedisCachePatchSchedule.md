---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: ebc51005bcffdde2ad5f64764e90440e8d1e7583
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923475"
---
# <span data-ttu-id="d30e6-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d30e6-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="d30e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d30e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d30e6-103">Fügt einen Patchplan hinzu.</span><span class="sxs-lookup"><span data-stu-id="d30e6-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="d30e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d30e6-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d30e6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d30e6-105">DESCRIPTION</span></span>
<span data-ttu-id="d30e6-106">Das **Cmdlet New-AzRedisCachePatchSchedule** fügt einem Cache in Azure Redis Cache einen Patchplan hinzu.</span><span class="sxs-lookup"><span data-stu-id="d30e6-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="d30e6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d30e6-107">EXAMPLES</span></span>

### <span data-ttu-id="d30e6-108">Beispiel 1: Erstellen und Hinzufügen eines Patchzeitplans in einem Cache</span><span class="sxs-lookup"><span data-stu-id="d30e6-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="d30e6-109">Mit diesem Befehl wird dem Cache mit dem Namen RedisCache06 ein Patchzeitplan hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="d30e6-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="d30e6-110">Der Parameter Entries verwendet als Wert einen Befehl, der **New-AzRedisCacheScheduleEntry** zum Erstellen eines Zeitplans verwendet.</span><span class="sxs-lookup"><span data-stu-id="d30e6-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="d30e6-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d30e6-111">PARAMETERS</span></span>

### <span data-ttu-id="d30e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d30e6-112">-DefaultProfile</span></span>
<span data-ttu-id="d30e6-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d30e6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d30e6-114">-Einträge</span><span class="sxs-lookup"><span data-stu-id="d30e6-114">-Entries</span></span>
<span data-ttu-id="d30e6-115">Gibt ein Array von Zeitplänen an, die von diesem Cmdlet für einen Cache festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d30e6-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="d30e6-116">Um ein **PSScheduleEntry-Objekt zu** erhalten, verwenden Sie das New-AzRedisCacheScheduleEntry Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d30e6-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="d30e6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d30e6-117">-Name</span></span>
<span data-ttu-id="d30e6-118">Gibt den Namen des Caches an.</span><span class="sxs-lookup"><span data-stu-id="d30e6-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="d30e6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d30e6-119">-ResourceGroupName</span></span>
<span data-ttu-id="d30e6-120">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="d30e6-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="d30e6-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d30e6-121">-Confirm</span></span>
<span data-ttu-id="d30e6-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d30e6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d30e6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d30e6-123">-WhatIf</span></span>
<span data-ttu-id="d30e6-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d30e6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d30e6-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d30e6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d30e6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d30e6-126">CommonParameters</span></span>
<span data-ttu-id="d30e6-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d30e6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d30e6-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d30e6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d30e6-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d30e6-129">INPUTS</span></span>

### <span data-ttu-id="d30e6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d30e6-130">System.String</span></span>

### <span data-ttu-id="d30e6-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span><span class="sxs-lookup"><span data-stu-id="d30e6-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="d30e6-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d30e6-132">OUTPUTS</span></span>

### <span data-ttu-id="d30e6-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="d30e6-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="d30e6-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d30e6-134">NOTES</span></span>
* <span data-ttu-id="d30e6-135">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="d30e6-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="d30e6-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d30e6-136">RELATED LINKS</span></span>

[<span data-ttu-id="d30e6-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d30e6-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="d30e6-138">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="d30e6-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="d30e6-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d30e6-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


