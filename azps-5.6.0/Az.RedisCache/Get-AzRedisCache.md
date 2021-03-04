---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: 8423c098542a621ec66a5de3255ccf62c3e8ec94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918107"
---
# <span data-ttu-id="4ee17-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4ee17-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="4ee17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ee17-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee17-103">Ruft einen Redis-Cache ab.</span><span class="sxs-lookup"><span data-stu-id="4ee17-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="4ee17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ee17-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ee17-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ee17-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee17-106">Das **Get-AzRedisCache-Cmdlet** ruft den angegebenen Azure Redis-Cache ab.</span><span class="sxs-lookup"><span data-stu-id="4ee17-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="4ee17-107">Wenn Sie keine Parameter angeben, ruft dieser Vorgang jeden Redis-Cache für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="4ee17-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="4ee17-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ee17-108">EXAMPLES</span></span>

### <span data-ttu-id="4ee17-109">Beispiel 1: Erhalten eines Redis-Caches nach Name</span><span class="sxs-lookup"><span data-stu-id="4ee17-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzRedisCache -Name "myexists"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="4ee17-110">Dieser Befehl ruft den Redis-Cache mit dem Namen myexists ab.</span><span class="sxs-lookup"><span data-stu-id="4ee17-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="4ee17-111">Beispiel 2: Jeden Redis-Cache in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="4ee17-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzRedisCache -ResourceGroupName "myGroup"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="4ee17-112">Dieser Befehl ruft jeden Redis-Cache in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="4ee17-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="4ee17-113">Beispiel 3: Jeden Redis-Cache im aktuellen Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="4ee17-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzRedisCache

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup2
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup2/providers/Microsoft.Cache/Redis/myearlier2
        Location           : North Central US
        Name               : myearlier2
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier2.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="4ee17-114">Dieser Befehl ruft jeden Redis-Cache im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="4ee17-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="4ee17-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4ee17-115">PARAMETERS</span></span>

### <span data-ttu-id="4ee17-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee17-116">-DefaultProfile</span></span>
<span data-ttu-id="4ee17-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ee17-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ee17-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4ee17-118">-Name</span></span>
<span data-ttu-id="4ee17-119">Gibt den Namen des zu erhaltenden Redis-Caches an.</span><span class="sxs-lookup"><span data-stu-id="4ee17-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="4ee17-120">Verwenden Sie den *Parameter ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="4ee17-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="4ee17-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee17-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ee17-122">Gibt den Namen der Ressourcengruppe an, die den zu erhaltenden Redis-Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="4ee17-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="4ee17-123">Wenn Sie nur den *Parameter ResourceGroupName angeben,* ruft dieser Vorgang jeden Redis-Cache in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="4ee17-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="4ee17-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee17-124">CommonParameters</span></span>
<span data-ttu-id="4ee17-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee17-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee17-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee17-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee17-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ee17-127">INPUTS</span></span>

### <span data-ttu-id="4ee17-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4ee17-128">System.String</span></span>

## <span data-ttu-id="4ee17-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ee17-129">OUTPUTS</span></span>

### <span data-ttu-id="4ee17-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="4ee17-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="4ee17-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4ee17-131">NOTES</span></span>

## <span data-ttu-id="4ee17-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4ee17-132">RELATED LINKS</span></span>

[<span data-ttu-id="4ee17-133">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4ee17-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="4ee17-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4ee17-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="4ee17-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4ee17-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


