---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295990"
---
# <span data-ttu-id="15b8d-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="15b8d-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="15b8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="15b8d-103">Laden Sie die Verknüpfung für die Georeplikation für den Redis Cache ab.</span><span class="sxs-lookup"><span data-stu-id="15b8d-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="15b8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15b8d-104">SYNTAX</span></span>

### <span data-ttu-id="15b8d-105">AllLinksForCache (Standard)</span><span class="sxs-lookup"><span data-stu-id="15b8d-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15b8d-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="15b8d-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15b8d-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="15b8d-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15b8d-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="15b8d-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15b8d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15b8d-109">DESCRIPTION</span></span>
<span data-ttu-id="15b8d-110">Es gibt vier verschiedene Möglichkeiten zum Erhalten von Details für die Verknüpfung mit der Georeplikation.</span><span class="sxs-lookup"><span data-stu-id="15b8d-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="15b8d-111">Geben Sie entweder den Parameter "Name" oder "PrimaryServerName" und/oder "SecondaryServerName" an.</span><span class="sxs-lookup"><span data-stu-id="15b8d-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="15b8d-112">Der Name wird dann für den Link zurückgegeben, in dem der Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="15b8d-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="15b8d-113">Wenn nur "PrimaryServerName" angegeben wird, werden alle Links zurückgegeben, für die der primäre Cache besteht.</span><span class="sxs-lookup"><span data-stu-id="15b8d-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="15b8d-114">Wenn nur "SecondaryServerName" angegeben wird, werden alle Links zurückgegeben, bei denen der Cache sekundär ist.</span><span class="sxs-lookup"><span data-stu-id="15b8d-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="15b8d-115">Wenn beide Namen "PrimaryServerName" und "SecondaryServerName" angegeben werden, wird ein bestimmter Link mit der richtigen Rolle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="15b8d-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="15b8d-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="15b8d-116">EXAMPLES</span></span>

### <span data-ttu-id="15b8d-117">Beispiel 1: Get using parameter set AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="15b8d-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="15b8d-118">Dieser Befehl ruft alle Georeplikationsverknüpfungen für den Redis-Cache namens "mycache1" ab.</span><span class="sxs-lookup"><span data-stu-id="15b8d-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="15b8d-119">Beispiel 2: Get using parameter set AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="15b8d-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="15b8d-120">Dieser Befehl ruft Georeplikationsverknüpfungen ab, bei denen der Redis-Cache namens "mycache1" primär ist.</span><span class="sxs-lookup"><span data-stu-id="15b8d-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="15b8d-121">Beispiel 3: Verwenden des Parameters "AllLinksForSecondaryCache"</span><span class="sxs-lookup"><span data-stu-id="15b8d-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="15b8d-122">Dieser Befehl ruft Georeplikationsverknüpfungen ab, bei denen der Redis-Cache namens "mycache2" sekundär ist.</span><span class="sxs-lookup"><span data-stu-id="15b8d-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="15b8d-123">Beispiel 4: Verwenden des Parametersatzs SingleLink</span><span class="sxs-lookup"><span data-stu-id="15b8d-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="15b8d-124">Dieser Befehl ruft eine einzelne Georeplikationsverknüpfung ab, wobei "Redis-Cache" mit dem Namen "mycache1" primär und der Redis-Cache mit dem Namen "mycache2" sekundär ist.</span><span class="sxs-lookup"><span data-stu-id="15b8d-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="15b8d-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15b8d-125">PARAMETERS</span></span>

### <span data-ttu-id="15b8d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b8d-126">-DefaultProfile</span></span>
<span data-ttu-id="15b8d-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15b8d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15b8d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="15b8d-128">-Name</span></span>
<span data-ttu-id="15b8d-129">Name des Redis-Caches.</span><span class="sxs-lookup"><span data-stu-id="15b8d-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="15b8d-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="15b8d-130">-PrimaryServerName</span></span>
<span data-ttu-id="15b8d-131">Name des primären Redis-Caches im Link.</span><span class="sxs-lookup"><span data-stu-id="15b8d-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="15b8d-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="15b8d-132">-SecondaryServerName</span></span>
<span data-ttu-id="15b8d-133">Name des sekundären Redis-Caches im Link.</span><span class="sxs-lookup"><span data-stu-id="15b8d-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="15b8d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b8d-134">CommonParameters</span></span>
<span data-ttu-id="15b8d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15b8d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b8d-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b8d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b8d-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="15b8d-137">INPUTS</span></span>

### <span data-ttu-id="15b8d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="15b8d-138">System.String</span></span>

## <span data-ttu-id="15b8d-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="15b8d-139">OUTPUTS</span></span>

### <span data-ttu-id="15b8d-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="15b8d-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="15b8d-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="15b8d-141">NOTES</span></span>

## <span data-ttu-id="15b8d-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="15b8d-142">RELATED LINKS</span></span>

[<span data-ttu-id="15b8d-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="15b8d-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="15b8d-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="15b8d-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="15b8d-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="15b8d-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="15b8d-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="15b8d-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="15b8d-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="15b8d-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="15b8d-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="15b8d-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)