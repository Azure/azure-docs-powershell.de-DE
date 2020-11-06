---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: a45407fc7f25e2c7bee5c591ab3110b0620a2c0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495738"
---
# <span data-ttu-id="136d6-101">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="136d6-101">Get-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="136d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="136d6-102">SYNOPSIS</span></span>
<span data-ttu-id="136d6-103">Link "Geo-Replikation" für den "Mehrweg"-Cache</span><span class="sxs-lookup"><span data-stu-id="136d6-103">Get geo replication link for Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="136d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="136d6-104">SYNTAX</span></span>

### <span data-ttu-id="136d6-105">AllLinksForCache (Standard)</span><span class="sxs-lookup"><span data-stu-id="136d6-105">AllLinksForCache (Default)</span></span>
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="136d6-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="136d6-106">AllLinksForPrimaryCache</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="136d6-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="136d6-107">SingleLink</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="136d6-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="136d6-108">AllLinksForSecondaryCache</span></span>
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="136d6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="136d6-109">DESCRIPTION</span></span>
<span data-ttu-id="136d6-110">Es gibt vier verschiedene Möglichkeiten zum Abrufen von Details zur Geo-Replikationsverknüpfung.</span><span class="sxs-lookup"><span data-stu-id="136d6-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="136d6-111">Geben Sie entweder den Parameternamen oder PrimaryServerName und/oder SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="136d6-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="136d6-112">Name angegeben ist, wird der gesamte Link, in dem der Cache vorhanden ist, zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="136d6-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="136d6-113">Wenn nur PrimaryServerName angegeben ist, werden alle Verknüpfungen zurückgegeben, wobei der Cache primär ist.</span><span class="sxs-lookup"><span data-stu-id="136d6-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="136d6-114">Wenn nur SecondaryServerName angegeben ist, werden alle Links, bei denen der Cache sekundär ist, zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="136d6-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="136d6-115">Wenn PrimaryServerName und SecondaryServerName beide angegeben sind, wird ein bestimmter Link mit der korrekten Rolle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="136d6-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="136d6-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="136d6-116">EXAMPLES</span></span>

### <span data-ttu-id="136d6-117">Beispiel 1: Abrufen mit dem Parametersatz AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="136d6-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="136d6-118">Dieser Befehl ruft alle Links für die Geo-Replikation für den "mycache1.</span><span class="sxs-lookup"><span data-stu-id="136d6-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="136d6-119">Beispiel 2: Abrufen der Verwendung von Parametersatz AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="136d6-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="136d6-120">Dieser Befehl ruft georeplikations-links ab, wobei der Name des mycache1-Caches primär ist.</span><span class="sxs-lookup"><span data-stu-id="136d6-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="136d6-121">Beispiel 3: Abrufen mit dem Parametersatz AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="136d6-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="136d6-122">Dieser Befehl ruft georeplikations-links ab, wobei der mycache2-Cache mit dem Namen "Sekundär" ist.</span><span class="sxs-lookup"><span data-stu-id="136d6-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="136d6-123">Beispiel 4: Abrufen der Verwendung von Parametersatz SingleLink</span><span class="sxs-lookup"><span data-stu-id="136d6-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="136d6-124">Dieser Befehl ruft eine einzelne georeplikations-links ab, wobei der mycache1-Cache mit dem Namen "Primär" und der "mycache2" mit dem Namen "4/4" sekundäre</span><span class="sxs-lookup"><span data-stu-id="136d6-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="136d6-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="136d6-125">PARAMETERS</span></span>

### <span data-ttu-id="136d6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="136d6-126">-DefaultProfile</span></span>
<span data-ttu-id="136d6-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="136d6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="136d6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="136d6-128">-Name</span></span>
<span data-ttu-id="136d6-129">Name des Zwischenspeichers mit dem Namenzeichen</span><span class="sxs-lookup"><span data-stu-id="136d6-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="136d6-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="136d6-130">-PrimaryServerName</span></span>
<span data-ttu-id="136d6-131">Name des primären, in Verbindung stehenden "nicht-Cache".</span><span class="sxs-lookup"><span data-stu-id="136d6-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="136d6-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="136d6-132">-SecondaryServerName</span></span>
<span data-ttu-id="136d6-133">Der Name des sekundären "a/a-Cache" in Link.</span><span class="sxs-lookup"><span data-stu-id="136d6-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="136d6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="136d6-134">CommonParameters</span></span>
<span data-ttu-id="136d6-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="136d6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="136d6-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="136d6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="136d6-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="136d6-137">INPUTS</span></span>

### <span data-ttu-id="136d6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="136d6-138">System.String</span></span>

## <span data-ttu-id="136d6-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="136d6-139">OUTPUTS</span></span>

### <span data-ttu-id="136d6-140">Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="136d6-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="136d6-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="136d6-141">NOTES</span></span>

## <span data-ttu-id="136d6-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="136d6-142">RELATED LINKS</span></span>

[<span data-ttu-id="136d6-143">Neu – AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="136d6-143">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="136d6-144">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="136d6-144">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="136d6-145">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="136d6-145">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="136d6-146">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="136d6-146">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="136d6-147">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="136d6-147">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="136d6-148">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="136d6-148">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
