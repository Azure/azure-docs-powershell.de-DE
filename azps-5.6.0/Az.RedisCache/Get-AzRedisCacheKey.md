---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 1d5f230070f8b8c269137e07b04af970f314d564
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936619"
---
# <span data-ttu-id="203e2-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="203e2-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="203e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="203e2-102">SYNOPSIS</span></span>
<span data-ttu-id="203e2-103">Ruft die Zugriffstasten für einen Redis-Cache ab.</span><span class="sxs-lookup"><span data-stu-id="203e2-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="203e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="203e2-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="203e2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="203e2-105">DESCRIPTION</span></span>
<span data-ttu-id="203e2-106">Das **Get-AzRedisCacheKey-Cmdlet** ruft die Zugriffstasten für einen Azure Redis-Cache ab.</span><span class="sxs-lookup"><span data-stu-id="203e2-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="203e2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="203e2-107">EXAMPLES</span></span>

### <span data-ttu-id="203e2-108">Beispiel 1: Erhalten der Zugriffstasten für einen Redis-Cache</span><span class="sxs-lookup"><span data-stu-id="203e2-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="203e2-109">Dieser Befehl ruft die Zugriffstasten mit dem Namen MyCacheKey ab.</span><span class="sxs-lookup"><span data-stu-id="203e2-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="203e2-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="203e2-110">PARAMETERS</span></span>

### <span data-ttu-id="203e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="203e2-111">-DefaultProfile</span></span>
<span data-ttu-id="203e2-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="203e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="203e2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="203e2-113">-Name</span></span>
<span data-ttu-id="203e2-114">Gibt den Namen eines Redis-Caches an.</span><span class="sxs-lookup"><span data-stu-id="203e2-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="203e2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="203e2-115">-ResourceGroupName</span></span>
<span data-ttu-id="203e2-116">Gibt den Namen der Ressourcengruppe an, die den Redis-Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="203e2-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="203e2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="203e2-117">CommonParameters</span></span>
<span data-ttu-id="203e2-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="203e2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="203e2-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="203e2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="203e2-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="203e2-120">INPUTS</span></span>

### <span data-ttu-id="203e2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="203e2-121">System.String</span></span>

## <span data-ttu-id="203e2-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="203e2-122">OUTPUTS</span></span>

### <span data-ttu-id="203e2-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="203e2-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="203e2-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="203e2-124">NOTES</span></span>

## <span data-ttu-id="203e2-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="203e2-125">RELATED LINKS</span></span>

[<span data-ttu-id="203e2-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="203e2-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


