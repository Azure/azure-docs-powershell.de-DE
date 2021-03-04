---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: 41a2172fffdbd83edc8ab72a4fe922d600362731
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928968"
---
# <span data-ttu-id="755e5-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="755e5-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="755e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="755e5-102">SYNOPSIS</span></span>
<span data-ttu-id="755e5-103">Erstellen Sie eine Georeplikationsverknüpfung zwischen zwei Redis Caches.</span><span class="sxs-lookup"><span data-stu-id="755e5-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="755e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="755e5-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="755e5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="755e5-105">DESCRIPTION</span></span>
<span data-ttu-id="755e5-106">Erstellen Sie eine Georeplikationsverknüpfung zwischen zwei Redis Caches.</span><span class="sxs-lookup"><span data-stu-id="755e5-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="755e5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="755e5-107">EXAMPLES</span></span>

### <span data-ttu-id="755e5-108">Beispiel 1: Erstellen einer Verknüpfung zwischen zwei Caches</span><span class="sxs-lookup"><span data-stu-id="755e5-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="755e5-109">Mit diesem Befehl wird eine Georeplikationsverknüpfung zwischen Redis Cache mycache1 und mycache2 erstellt.</span><span class="sxs-lookup"><span data-stu-id="755e5-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="755e5-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="755e5-110">PARAMETERS</span></span>

### <span data-ttu-id="755e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755e5-111">-DefaultProfile</span></span>
<span data-ttu-id="755e5-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="755e5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="755e5-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="755e5-113">-PrimaryServerName</span></span>
<span data-ttu-id="755e5-114">Name des primären Redis-Caches in Link.</span><span class="sxs-lookup"><span data-stu-id="755e5-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="755e5-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="755e5-115">-SecondaryServerName</span></span>
<span data-ttu-id="755e5-116">Name des sekundären Redis-Caches in Link.</span><span class="sxs-lookup"><span data-stu-id="755e5-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="755e5-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="755e5-117">-Confirm</span></span>
<span data-ttu-id="755e5-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="755e5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="755e5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="755e5-119">-WhatIf</span></span>
<span data-ttu-id="755e5-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="755e5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="755e5-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="755e5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="755e5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755e5-122">CommonParameters</span></span>
<span data-ttu-id="755e5-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="755e5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755e5-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="755e5-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755e5-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="755e5-125">INPUTS</span></span>

### <span data-ttu-id="755e5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="755e5-126">System.String</span></span>

## <span data-ttu-id="755e5-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="755e5-127">OUTPUTS</span></span>

### <span data-ttu-id="755e5-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="755e5-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="755e5-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="755e5-129">NOTES</span></span>

## <span data-ttu-id="755e5-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="755e5-130">RELATED LINKS</span></span>

[<span data-ttu-id="755e5-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="755e5-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="755e5-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="755e5-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="755e5-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="755e5-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="755e5-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="755e5-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="755e5-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="755e5-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="755e5-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="755e5-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)