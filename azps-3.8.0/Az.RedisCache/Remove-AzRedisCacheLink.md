---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 38c72a19e73d87272fb91fb6472a41496658e7d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846927"
---
# <span data-ttu-id="2f4fe-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2f4fe-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="2f4fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f4fe-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4fe-103">Entfernen einer Geo-Replikationsverknüpfung zwischen zwei 2-a-Caches</span><span class="sxs-lookup"><span data-stu-id="2f4fe-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="2f4fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f4fe-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f4fe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f4fe-105">DESCRIPTION</span></span>
<span data-ttu-id="2f4fe-106">Entfernen einer Geo-Replikationsverknüpfung zwischen zwei 2-a-Caches</span><span class="sxs-lookup"><span data-stu-id="2f4fe-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="2f4fe-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f4fe-107">EXAMPLES</span></span>

### <span data-ttu-id="2f4fe-108">Beispiel 1: Entfernen einer Geo-Replikationsverknüpfung</span><span class="sxs-lookup"><span data-stu-id="2f4fe-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="2f4fe-109">Dieser Befehl entfernt eine Geo-Replication-Links, wobei der mycache1-Cache mit dem Namen "Primär" und der "mycache2.</span><span class="sxs-lookup"><span data-stu-id="2f4fe-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="2f4fe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f4fe-110">PARAMETERS</span></span>

### <span data-ttu-id="2f4fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4fe-111">-DefaultProfile</span></span>
<span data-ttu-id="2f4fe-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f4fe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f4fe-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f4fe-113">-PassThru</span></span>
<span data-ttu-id="2f4fe-114">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="2f4fe-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2f4fe-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="2f4fe-115">-PrimaryServerName</span></span>
<span data-ttu-id="2f4fe-116">Name des primären, in Verbindung stehenden "nicht-Cache".</span><span class="sxs-lookup"><span data-stu-id="2f4fe-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="2f4fe-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="2f4fe-117">-SecondaryServerName</span></span>
<span data-ttu-id="2f4fe-118">Der Name des sekundären "a/a-Cache" in Link.</span><span class="sxs-lookup"><span data-stu-id="2f4fe-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="2f4fe-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2f4fe-119">-Confirm</span></span>
<span data-ttu-id="2f4fe-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f4fe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f4fe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f4fe-121">-WhatIf</span></span>
<span data-ttu-id="2f4fe-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f4fe-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f4fe-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f4fe-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f4fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4fe-124">CommonParameters</span></span>
<span data-ttu-id="2f4fe-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f4fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4fe-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f4fe-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4fe-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f4fe-127">INPUTS</span></span>

### <span data-ttu-id="2f4fe-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2f4fe-128">System.String</span></span>

## <span data-ttu-id="2f4fe-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f4fe-129">OUTPUTS</span></span>

### <span data-ttu-id="2f4fe-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f4fe-130">System.Boolean</span></span>

## <span data-ttu-id="2f4fe-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f4fe-131">NOTES</span></span>

## <span data-ttu-id="2f4fe-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f4fe-132">RELATED LINKS</span></span>

[<span data-ttu-id="2f4fe-133">Neu – AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2f4fe-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="2f4fe-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2f4fe-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="2f4fe-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2f4fe-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="2f4fe-136">Neu – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2f4fe-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="2f4fe-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2f4fe-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="2f4fe-138">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2f4fe-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)