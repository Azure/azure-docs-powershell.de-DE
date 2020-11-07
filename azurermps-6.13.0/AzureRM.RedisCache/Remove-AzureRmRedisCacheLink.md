---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
ms.openlocfilehash: e4c45095dba8ec72e00fa26eee2d8a3fb6f029fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664330"
---
# <span data-ttu-id="dca76-101">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="dca76-101">Remove-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="dca76-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dca76-102">SYNOPSIS</span></span>
<span data-ttu-id="dca76-103">Entfernen einer Geo-Replikationsverknüpfung zwischen zwei 2-a-Caches</span><span class="sxs-lookup"><span data-stu-id="dca76-103">Remove a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dca76-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dca76-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dca76-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dca76-105">DESCRIPTION</span></span>
<span data-ttu-id="dca76-106">Entfernen einer Geo-Replikationsverknüpfung zwischen zwei 2-a-Caches</span><span class="sxs-lookup"><span data-stu-id="dca76-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="dca76-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dca76-107">EXAMPLES</span></span>

### <span data-ttu-id="dca76-108">Beispiel 1: Entfernen einer Geo-Replikationsverknüpfung</span><span class="sxs-lookup"><span data-stu-id="dca76-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="dca76-109">Dieser Befehl entfernt eine Geo-Replication-Links, wobei der mycache1-Cache mit dem Namen "Primär" und der "mycache2.</span><span class="sxs-lookup"><span data-stu-id="dca76-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="dca76-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dca76-110">PARAMETERS</span></span>

### <span data-ttu-id="dca76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca76-111">-DefaultProfile</span></span>
<span data-ttu-id="dca76-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dca76-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dca76-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dca76-113">-PassThru</span></span>
<span data-ttu-id="dca76-114">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="dca76-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca76-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="dca76-115">-PrimaryServerName</span></span>
<span data-ttu-id="dca76-116">Name des primären, in Verbindung stehenden "nicht-Cache".</span><span class="sxs-lookup"><span data-stu-id="dca76-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="dca76-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="dca76-117">-SecondaryServerName</span></span>
<span data-ttu-id="dca76-118">Der Name des sekundären "a/a-Cache" in Link.</span><span class="sxs-lookup"><span data-stu-id="dca76-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="dca76-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dca76-119">-Confirm</span></span>
<span data-ttu-id="dca76-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dca76-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dca76-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dca76-121">-WhatIf</span></span>
<span data-ttu-id="dca76-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dca76-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dca76-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dca76-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dca76-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca76-124">CommonParameters</span></span>
<span data-ttu-id="dca76-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dca76-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca76-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dca76-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca76-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dca76-127">INPUTS</span></span>

### <span data-ttu-id="dca76-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dca76-128">System.String</span></span>

## <span data-ttu-id="dca76-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dca76-129">OUTPUTS</span></span>

### <span data-ttu-id="dca76-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dca76-130">System.Boolean</span></span>

## <span data-ttu-id="dca76-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="dca76-131">NOTES</span></span>

## <span data-ttu-id="dca76-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dca76-132">RELATED LINKS</span></span>

[<span data-ttu-id="dca76-133">Neu – AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="dca76-133">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="dca76-134">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="dca76-134">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="dca76-135">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dca76-135">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="dca76-136">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dca76-136">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="dca76-137">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dca76-137">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="dca76-138">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dca76-138">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
