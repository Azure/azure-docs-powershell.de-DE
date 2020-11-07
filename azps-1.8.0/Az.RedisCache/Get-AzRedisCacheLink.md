---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 8129634e940624fe09dad4a1199f96dbcf5162bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659764"
---
# <span data-ttu-id="97070-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="97070-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="97070-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97070-102">SYNOPSIS</span></span>
<span data-ttu-id="97070-103">Link "Geo-Replikation" für den "Mehrweg"-Cache</span><span class="sxs-lookup"><span data-stu-id="97070-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="97070-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97070-104">SYNTAX</span></span>

### <span data-ttu-id="97070-105">AllLinksForCache (Standard)</span><span class="sxs-lookup"><span data-stu-id="97070-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97070-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="97070-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97070-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="97070-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97070-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="97070-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97070-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97070-109">DESCRIPTION</span></span>
<span data-ttu-id="97070-110">Es gibt vier verschiedene Möglichkeiten zum Abrufen von Details zur Geo-Replikationsverknüpfung.</span><span class="sxs-lookup"><span data-stu-id="97070-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="97070-111">Geben Sie entweder den Parameternamen oder PrimaryServerName und/oder SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="97070-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="97070-112">Name angegeben ist, wird der gesamte Link, in dem der Cache vorhanden ist, zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97070-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="97070-113">Wenn nur PrimaryServerName angegeben ist, werden alle Verknüpfungen zurückgegeben, wobei der Cache primär ist.</span><span class="sxs-lookup"><span data-stu-id="97070-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="97070-114">Wenn nur SecondaryServerName angegeben ist, werden alle Links, bei denen der Cache sekundär ist, zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97070-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="97070-115">Wenn PrimaryServerName und SecondaryServerName beide angegeben sind, wird ein bestimmter Link mit der korrekten Rolle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97070-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="97070-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97070-116">EXAMPLES</span></span>

### <span data-ttu-id="97070-117">Beispiel 1: Abrufen mit dem Parametersatz AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="97070-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="97070-118">Dieser Befehl ruft alle Links für die Geo-Replikation für den "mycache1.</span><span class="sxs-lookup"><span data-stu-id="97070-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="97070-119">Beispiel 2: Abrufen der Verwendung von Parametersatz AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="97070-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="97070-120">Dieser Befehl ruft georeplikations-links ab, wobei der Name des mycache1-Caches primär ist.</span><span class="sxs-lookup"><span data-stu-id="97070-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="97070-121">Beispiel 3: Abrufen mit dem Parametersatz AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="97070-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="97070-122">Dieser Befehl ruft georeplikations-links ab, wobei der mycache2-Cache mit dem Namen "Sekundär" ist.</span><span class="sxs-lookup"><span data-stu-id="97070-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="97070-123">Beispiel 4: Abrufen der Verwendung von Parametersatz SingleLink</span><span class="sxs-lookup"><span data-stu-id="97070-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="97070-124">Dieser Befehl ruft eine einzelne georeplikations-links ab, wobei der mycache1-Cache mit dem Namen "Primär" und der "mycache2" mit dem Namen "4/4" sekundäre</span><span class="sxs-lookup"><span data-stu-id="97070-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="97070-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="97070-125">PARAMETERS</span></span>

### <span data-ttu-id="97070-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97070-126">-DefaultProfile</span></span>
<span data-ttu-id="97070-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97070-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97070-128">-Name</span><span class="sxs-lookup"><span data-stu-id="97070-128">-Name</span></span>
<span data-ttu-id="97070-129">Name des Zwischenspeichers mit dem Namenzeichen</span><span class="sxs-lookup"><span data-stu-id="97070-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="97070-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="97070-130">-PrimaryServerName</span></span>
<span data-ttu-id="97070-131">Name des primären, in Verbindung stehenden "nicht-Cache".</span><span class="sxs-lookup"><span data-stu-id="97070-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="97070-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="97070-132">-SecondaryServerName</span></span>
<span data-ttu-id="97070-133">Der Name des sekundären "a/a-Cache" in Link.</span><span class="sxs-lookup"><span data-stu-id="97070-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="97070-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97070-134">CommonParameters</span></span>
<span data-ttu-id="97070-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97070-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97070-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97070-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97070-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97070-137">INPUTS</span></span>

### <span data-ttu-id="97070-138">System. String</span><span class="sxs-lookup"><span data-stu-id="97070-138">System.String</span></span>

## <span data-ttu-id="97070-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97070-139">OUTPUTS</span></span>

### <span data-ttu-id="97070-140">Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="97070-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="97070-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="97070-141">NOTES</span></span>

## <span data-ttu-id="97070-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97070-142">RELATED LINKS</span></span>

[<span data-ttu-id="97070-143">Neu – AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="97070-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="97070-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="97070-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="97070-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="97070-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="97070-146">Neu – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="97070-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="97070-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="97070-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="97070-148">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="97070-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)