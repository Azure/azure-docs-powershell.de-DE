---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: dff5f565e27f89360465ede3eb8fbe2c3d5620a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481006"
---
# <span data-ttu-id="83137-101">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="83137-101">Get-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="83137-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83137-102">SYNOPSIS</span></span>
<span data-ttu-id="83137-103">Link "Geo-Replikation" für den "Mehrweg"-Cache</span><span class="sxs-lookup"><span data-stu-id="83137-103">Get geo replication link for Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83137-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83137-104">SYNTAX</span></span>

### <span data-ttu-id="83137-105">AllLinksForCache (Standard)</span><span class="sxs-lookup"><span data-stu-id="83137-105">AllLinksForCache (Default)</span></span>
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83137-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="83137-106">AllLinksForPrimaryCache</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83137-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="83137-107">SingleLink</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83137-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="83137-108">AllLinksForSecondaryCache</span></span>
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83137-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83137-109">DESCRIPTION</span></span>
<span data-ttu-id="83137-110">Es gibt vier verschiedene Möglichkeiten zum Abrufen von Details zur Geo-Replikationsverknüpfung.</span><span class="sxs-lookup"><span data-stu-id="83137-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="83137-111">Geben Sie entweder den Parameternamen oder PrimaryServerName und/oder SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="83137-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="83137-112">Name angegeben ist, wird der gesamte Link, in dem der Cache vorhanden ist, zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83137-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="83137-113">Wenn nur PrimaryServerName angegeben ist, werden alle Verknüpfungen zurückgegeben, wobei der Cache primär ist.</span><span class="sxs-lookup"><span data-stu-id="83137-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="83137-114">Wenn nur SecondaryServerName angegeben ist, werden alle Links, bei denen der Cache sekundär ist, zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83137-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="83137-115">Wenn PrimaryServerName und SecondaryServerName beide angegeben sind, wird ein bestimmter Link mit der korrekten Rolle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83137-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="83137-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83137-116">EXAMPLES</span></span>

### <span data-ttu-id="83137-117">Beispiel 1: Abrufen mit dem Parametersatz AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="83137-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="83137-118">Dieser Befehl ruft alle Links für die Geo-Replikation für den "mycache1.</span><span class="sxs-lookup"><span data-stu-id="83137-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="83137-119">Beispiel 2: Abrufen der Verwendung von Parametersatz AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="83137-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="83137-120">Dieser Befehl ruft georeplikations-links ab, wobei der Name des mycache1-Caches primär ist.</span><span class="sxs-lookup"><span data-stu-id="83137-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="83137-121">Beispiel 3: Abrufen mit dem Parametersatz AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="83137-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="83137-122">Dieser Befehl ruft georeplikations-links ab, wobei der mycache2-Cache mit dem Namen "Sekundär" ist.</span><span class="sxs-lookup"><span data-stu-id="83137-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="83137-123">Beispiel 4: Abrufen der Verwendung von Parametersatz SingleLink</span><span class="sxs-lookup"><span data-stu-id="83137-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="83137-124">Dieser Befehl ruft eine einzelne georeplikations-links ab, wobei der mycache1-Cache mit dem Namen "Primär" und der "mycache2" mit dem Namen "4/4" sekundäre</span><span class="sxs-lookup"><span data-stu-id="83137-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="83137-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="83137-125">PARAMETERS</span></span>

### <span data-ttu-id="83137-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83137-126">-DefaultProfile</span></span>
<span data-ttu-id="83137-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83137-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83137-128">-Name</span><span class="sxs-lookup"><span data-stu-id="83137-128">-Name</span></span>
<span data-ttu-id="83137-129">Name des Zwischenspeichers mit dem Namenzeichen</span><span class="sxs-lookup"><span data-stu-id="83137-129">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83137-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="83137-130">-PrimaryServerName</span></span>
<span data-ttu-id="83137-131">Name des primären, in Verbindung stehenden "nicht-Cache".</span><span class="sxs-lookup"><span data-stu-id="83137-131">Name of primary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83137-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="83137-132">-SecondaryServerName</span></span>
<span data-ttu-id="83137-133">Der Name des sekundären "a/a-Cache" in Link.</span><span class="sxs-lookup"><span data-stu-id="83137-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83137-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83137-134">CommonParameters</span></span>
<span data-ttu-id="83137-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83137-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83137-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83137-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83137-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83137-137">INPUTS</span></span>

### <span data-ttu-id="83137-138">System. String</span><span class="sxs-lookup"><span data-stu-id="83137-138">System.String</span></span>
<span data-ttu-id="83137-139">Sie können die Eingabe an dieses Cmdlet nach Name, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="83137-139">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="83137-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83137-140">OUTPUTS</span></span>

### <span data-ttu-id="83137-141">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer, Microsoft. Azure. Commands. RedisCache, Version = 4.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="83137-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="83137-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="83137-142">NOTES</span></span>

## <span data-ttu-id="83137-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83137-143">RELATED LINKS</span></span>

[<span data-ttu-id="83137-144">Neu – AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="83137-144">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="83137-145">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="83137-145">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="83137-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="83137-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="83137-147">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="83137-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="83137-148">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="83137-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="83137-149">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="83137-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
