---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 297966fe0ad59948fd321ec52cf066ad5caa3d43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946944"
---
# <span data-ttu-id="dc9a1-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="dc9a1-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="dc9a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="dc9a1-103">Ruft einen Patchplan ab.</span><span class="sxs-lookup"><span data-stu-id="dc9a1-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="dc9a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc9a1-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc9a1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc9a1-105">DESCRIPTION</span></span>
<span data-ttu-id="dc9a1-106">Das **Get-AzRedisCachePatchSchedule-Cmdlet** ruft einen Patchplan für einen Cache in Azure Redis Cache ab.</span><span class="sxs-lookup"><span data-stu-id="dc9a1-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="dc9a1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dc9a1-107">EXAMPLES</span></span>

### <span data-ttu-id="dc9a1-108">Beispiel 1: Erhalten des Patchzeitplans</span><span class="sxs-lookup"><span data-stu-id="dc9a1-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="dc9a1-109">Dieser Befehl ruft den Patchzeitplan aus dem Cache mit dem Namen RedisCache06 ab.</span><span class="sxs-lookup"><span data-stu-id="dc9a1-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="dc9a1-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dc9a1-110">PARAMETERS</span></span>

### <span data-ttu-id="dc9a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc9a1-111">-DefaultProfile</span></span>
<span data-ttu-id="dc9a1-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc9a1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc9a1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="dc9a1-113">-Name</span></span>
<span data-ttu-id="dc9a1-114">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="dc9a1-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="dc9a1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc9a1-115">-ResourceGroupName</span></span>
<span data-ttu-id="dc9a1-116">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="dc9a1-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="dc9a1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc9a1-117">CommonParameters</span></span>
<span data-ttu-id="dc9a1-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc9a1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc9a1-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc9a1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc9a1-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dc9a1-120">INPUTS</span></span>

### <span data-ttu-id="dc9a1-121">System.String</span><span class="sxs-lookup"><span data-stu-id="dc9a1-121">System.String</span></span>

## <span data-ttu-id="dc9a1-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dc9a1-122">OUTPUTS</span></span>

### <span data-ttu-id="dc9a1-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="dc9a1-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="dc9a1-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dc9a1-124">NOTES</span></span>
* <span data-ttu-id="dc9a1-125">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="dc9a1-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="dc9a1-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dc9a1-126">RELATED LINKS</span></span>

[<span data-ttu-id="dc9a1-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="dc9a1-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="dc9a1-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="dc9a1-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="dc9a1-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="dc9a1-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


