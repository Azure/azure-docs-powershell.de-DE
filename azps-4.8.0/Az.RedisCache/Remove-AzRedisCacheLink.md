---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 38c72a19e73d87272fb91fb6472a41496658e7d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166162"
---
# <span data-ttu-id="3b561-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3b561-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="3b561-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b561-102">SYNOPSIS</span></span>
<span data-ttu-id="3b561-103">Entfernen einer Geo-Replikationsverknüpfung zwischen zwei 2-a-Caches</span><span class="sxs-lookup"><span data-stu-id="3b561-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="3b561-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b561-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b561-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b561-105">DESCRIPTION</span></span>
<span data-ttu-id="3b561-106">Entfernen einer Geo-Replikationsverknüpfung zwischen zwei 2-a-Caches</span><span class="sxs-lookup"><span data-stu-id="3b561-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="3b561-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b561-107">EXAMPLES</span></span>

### <span data-ttu-id="3b561-108">Beispiel 1: Entfernen einer Geo-Replikationsverknüpfung</span><span class="sxs-lookup"><span data-stu-id="3b561-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="3b561-109">Dieser Befehl entfernt eine Geo-Replication-Links, wobei der mycache1-Cache mit dem Namen "Primär" und der "mycache2.</span><span class="sxs-lookup"><span data-stu-id="3b561-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="3b561-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b561-110">PARAMETERS</span></span>

### <span data-ttu-id="3b561-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b561-111">-DefaultProfile</span></span>
<span data-ttu-id="3b561-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b561-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b561-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b561-113">-PassThru</span></span>
<span data-ttu-id="3b561-114">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="3b561-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3b561-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="3b561-115">-PrimaryServerName</span></span>
<span data-ttu-id="3b561-116">Name des primären, in Verbindung stehenden "nicht-Cache".</span><span class="sxs-lookup"><span data-stu-id="3b561-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="3b561-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="3b561-117">-SecondaryServerName</span></span>
<span data-ttu-id="3b561-118">Der Name des sekundären "a/a-Cache" in Link.</span><span class="sxs-lookup"><span data-stu-id="3b561-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="3b561-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b561-119">-Confirm</span></span>
<span data-ttu-id="3b561-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b561-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b561-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b561-121">-WhatIf</span></span>
<span data-ttu-id="3b561-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b561-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b561-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b561-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b561-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b561-124">CommonParameters</span></span>
<span data-ttu-id="3b561-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b561-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b561-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b561-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b561-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b561-127">INPUTS</span></span>

### <span data-ttu-id="3b561-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3b561-128">System.String</span></span>

## <span data-ttu-id="3b561-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b561-129">OUTPUTS</span></span>

### <span data-ttu-id="3b561-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b561-130">System.Boolean</span></span>

## <span data-ttu-id="3b561-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b561-131">NOTES</span></span>

## <span data-ttu-id="3b561-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b561-132">RELATED LINKS</span></span>

[<span data-ttu-id="3b561-133">Neu – AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3b561-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="3b561-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3b561-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="3b561-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3b561-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="3b561-136">Neu – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3b561-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="3b561-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3b561-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="3b561-138">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3b561-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)