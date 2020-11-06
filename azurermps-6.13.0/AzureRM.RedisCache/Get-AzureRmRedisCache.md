---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: ee4d5980743e5a78205c6e1f78cb55fa9b2f6496
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503426"
---
# <span data-ttu-id="b1a75-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b1a75-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="b1a75-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1a75-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a75-103">Ruft einen Zwischenspeicher mit einem Zwischenspeicher ab.</span><span class="sxs-lookup"><span data-stu-id="b1a75-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1a75-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1a75-104">SYNTAX</span></span>

```
Get-AzureRmRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1a75-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1a75-105">DESCRIPTION</span></span>
<span data-ttu-id="b1a75-106">Das Cmdlet " **Get-AzureRmRedisCache** " Ruft den angegebenen Azure-a/a-Cache ab.</span><span class="sxs-lookup"><span data-stu-id="b1a75-106">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="b1a75-107">Wenn Sie keine Parameter angeben, ruft dieser Vorgang jeden für das aktuelle Abonnement festgelegten Zwischenspeicher für den Zwischenspeicher ab.</span><span class="sxs-lookup"><span data-stu-id="b1a75-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="b1a75-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1a75-108">EXAMPLES</span></span>

### <span data-ttu-id="b1a75-109">Beispiel 1: Abrufen eines Zeichenfolgen-Caches mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="b1a75-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -Name "myexists"

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

<span data-ttu-id="b1a75-110">Dieser Befehl ruft den Zwischenspeicher mit dem Namen "myexists" ab.</span><span class="sxs-lookup"><span data-stu-id="b1a75-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="b1a75-111">Beispiel 2: Abrufen aller Zwischenspeicher in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b1a75-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup"

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

<span data-ttu-id="b1a75-112">Dieser Befehl ruft jeden Zwischenspeicher in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b1a75-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="b1a75-113">Beispiel 3: Abrufen aller Zwischenspeicher für die Zeichenfolgen im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="b1a75-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzureRmRedisCache

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

<span data-ttu-id="b1a75-114">Mit diesem Befehl wird jeder im-Cache des aktuellen Abonnements abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b1a75-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="b1a75-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1a75-115">PARAMETERS</span></span>

### <span data-ttu-id="b1a75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a75-116">-DefaultProfile</span></span>
<span data-ttu-id="b1a75-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1a75-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a75-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b1a75-118">-Name</span></span>
<span data-ttu-id="b1a75-119">Gibt den Namen des abzurufenden zu benennbaren Speichers an.</span><span class="sxs-lookup"><span data-stu-id="b1a75-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="b1a75-120">Verwendung mit dem *ResourceGroupName* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="b1a75-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="b1a75-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a75-121">-ResourceGroupName</span></span>
<span data-ttu-id="b1a75-122">Gibt den Namen der Ressourcengruppe an, die den zu bearbeitenden zu enthaltenden "a-Cache" enthält.</span><span class="sxs-lookup"><span data-stu-id="b1a75-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="b1a75-123">Wenn Sie nur den *ResourceGroupName* -Parameter angeben, wird für diesen Vorgang jeder Zwischenspeicher in der angegebenen Ressourcengruppe abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b1a75-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="b1a75-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a75-124">CommonParameters</span></span>
<span data-ttu-id="b1a75-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a75-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a75-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a75-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a75-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1a75-127">INPUTS</span></span>

### <span data-ttu-id="b1a75-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b1a75-128">System.String</span></span>

## <span data-ttu-id="b1a75-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1a75-129">OUTPUTS</span></span>

### <span data-ttu-id="b1a75-130">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="b1a75-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="b1a75-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1a75-131">NOTES</span></span>

## <span data-ttu-id="b1a75-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1a75-132">RELATED LINKS</span></span>

[<span data-ttu-id="b1a75-133">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b1a75-133">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="b1a75-134">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b1a75-134">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="b1a75-135">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b1a75-135">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


