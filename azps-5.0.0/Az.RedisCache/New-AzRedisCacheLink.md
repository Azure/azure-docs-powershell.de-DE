---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: d27f3ece14e18465fc534bff1a3451eaec2c40a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176765"
---
# <span data-ttu-id="60493-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="60493-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="60493-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60493-102">SYNOPSIS</span></span>
<span data-ttu-id="60493-103">Erstellen Sie einen Link zur Geo-Replikation zwischen zwei zwischen Speicherungs-Caches.</span><span class="sxs-lookup"><span data-stu-id="60493-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="60493-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60493-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60493-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60493-105">DESCRIPTION</span></span>
<span data-ttu-id="60493-106">Erstellen Sie einen Link zur Geo-Replikation zwischen zwei zwischen Speicherungs-Caches.</span><span class="sxs-lookup"><span data-stu-id="60493-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="60493-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60493-107">EXAMPLES</span></span>

### <span data-ttu-id="60493-108">Beispiel 1: Erstellen einer Verknüpfung zwischen zwei Caches</span><span class="sxs-lookup"><span data-stu-id="60493-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="60493-109">Dieser Befehl erstellt einen Link zur Geo-Replikation zwischen mycache1 und mycache2.</span><span class="sxs-lookup"><span data-stu-id="60493-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="60493-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="60493-110">PARAMETERS</span></span>

### <span data-ttu-id="60493-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60493-111">-DefaultProfile</span></span>
<span data-ttu-id="60493-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60493-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60493-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="60493-113">-PrimaryServerName</span></span>
<span data-ttu-id="60493-114">Name des primären, in Verbindung stehenden "nicht-Cache".</span><span class="sxs-lookup"><span data-stu-id="60493-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="60493-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="60493-115">-SecondaryServerName</span></span>
<span data-ttu-id="60493-116">Der Name des sekundären "a/a-Cache" in Link.</span><span class="sxs-lookup"><span data-stu-id="60493-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="60493-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="60493-117">-Confirm</span></span>
<span data-ttu-id="60493-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60493-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60493-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60493-119">-WhatIf</span></span>
<span data-ttu-id="60493-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60493-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60493-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60493-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60493-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60493-122">CommonParameters</span></span>
<span data-ttu-id="60493-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60493-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60493-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60493-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60493-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60493-125">INPUTS</span></span>

### <span data-ttu-id="60493-126">System. String</span><span class="sxs-lookup"><span data-stu-id="60493-126">System.String</span></span>

## <span data-ttu-id="60493-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60493-127">OUTPUTS</span></span>

### <span data-ttu-id="60493-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="60493-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="60493-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="60493-129">NOTES</span></span>

## <span data-ttu-id="60493-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60493-130">RELATED LINKS</span></span>

[<span data-ttu-id="60493-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="60493-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="60493-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="60493-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="60493-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="60493-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="60493-134">Neu – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="60493-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="60493-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="60493-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="60493-136">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="60493-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)