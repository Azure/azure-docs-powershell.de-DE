---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 9b1957054c243de8776f0063e236f9e19980af54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933760"
---
# <span data-ttu-id="59105-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="59105-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="59105-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59105-102">SYNOPSIS</span></span>
<span data-ttu-id="59105-103">Link zur Georeplikation für Den Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="59105-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="59105-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59105-104">SYNTAX</span></span>

### <span data-ttu-id="59105-105">AllLinksForCache (Standard)</span><span class="sxs-lookup"><span data-stu-id="59105-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59105-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="59105-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59105-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="59105-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59105-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="59105-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59105-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59105-109">DESCRIPTION</span></span>
<span data-ttu-id="59105-110">Es gibt vier verschiedene Möglichkeiten zum Erhalten von Linkdetails für die Georeplikation.</span><span class="sxs-lookup"><span data-stu-id="59105-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="59105-111">Geben Sie entweder den Parameter Name oder PrimaryServerName und/oder SecondaryServerName an.</span><span class="sxs-lookup"><span data-stu-id="59105-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="59105-112">Der Name wird angegeben, und alle Verknüpfungen, für die cache vorhanden ist, werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="59105-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="59105-113">Wenn nur PrimaryServerName angegeben wird, werden alle Links zurückgegeben, für die der Cache primär ist.</span><span class="sxs-lookup"><span data-stu-id="59105-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="59105-114">Wenn nur SecondaryServerName angegeben wird, werden alle Links zurückgegeben, für die der Cache sekundär ist.</span><span class="sxs-lookup"><span data-stu-id="59105-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="59105-115">Wenn PrimaryServerName und SecondaryServerName beide angegeben werden, wird ein bestimmter Link mit der richtigen Rolle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="59105-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="59105-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59105-116">EXAMPLES</span></span>

### <span data-ttu-id="59105-117">Beispiel 1: Verwenden des Parametersatzs AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="59105-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="59105-118">Dieser Befehl ruft alle Georeplikationslinks für Den Redis Cache mit dem Namen mycache1 ab.</span><span class="sxs-lookup"><span data-stu-id="59105-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="59105-119">Beispiel 2: Verwenden des Parametersatzs AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="59105-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="59105-120">Dieser Befehl ruft Georeplikationslinks ab, bei denen der Redis Cache mit dem Namen mycache1 primär ist.</span><span class="sxs-lookup"><span data-stu-id="59105-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="59105-121">Beispiel 3: Verwenden des Parametersatzs AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="59105-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="59105-122">Dieser Befehl ruft Verknüpfungen zur Georeplikation ab, wobei der Redis Cache mit dem Namen mycache2 sekundär ist.</span><span class="sxs-lookup"><span data-stu-id="59105-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="59105-123">Beispiel 4: Verwenden des Parametersatzs SingleLink</span><span class="sxs-lookup"><span data-stu-id="59105-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="59105-124">Dieser Befehl ruft eine einzelne Georeplikationsverknüpfung ab, wobei der Redis Cache mit dem Namen mycache1 primär und der Redis Cache mit dem Namen mycache2 sekundär ist.</span><span class="sxs-lookup"><span data-stu-id="59105-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="59105-125">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="59105-125">PARAMETERS</span></span>

### <span data-ttu-id="59105-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59105-126">-DefaultProfile</span></span>
<span data-ttu-id="59105-127">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59105-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59105-128">-Name</span><span class="sxs-lookup"><span data-stu-id="59105-128">-Name</span></span>
<span data-ttu-id="59105-129">Name des Redis-Caches.</span><span class="sxs-lookup"><span data-stu-id="59105-129">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59105-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="59105-130">-PrimaryServerName</span></span>
<span data-ttu-id="59105-131">Name des primären Redis-Caches in Link.</span><span class="sxs-lookup"><span data-stu-id="59105-131">Name of primary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59105-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="59105-132">-SecondaryServerName</span></span>
<span data-ttu-id="59105-133">Name des sekundären Redis-Caches in Link.</span><span class="sxs-lookup"><span data-stu-id="59105-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59105-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59105-134">CommonParameters</span></span>
<span data-ttu-id="59105-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59105-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59105-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59105-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59105-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59105-137">INPUTS</span></span>

### <span data-ttu-id="59105-138">System.String</span><span class="sxs-lookup"><span data-stu-id="59105-138">System.String</span></span>

## <span data-ttu-id="59105-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59105-139">OUTPUTS</span></span>

### <span data-ttu-id="59105-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="59105-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="59105-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="59105-141">NOTES</span></span>

## <span data-ttu-id="59105-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="59105-142">RELATED LINKS</span></span>

[<span data-ttu-id="59105-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="59105-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="59105-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="59105-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="59105-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="59105-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="59105-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="59105-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="59105-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="59105-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="59105-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="59105-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)