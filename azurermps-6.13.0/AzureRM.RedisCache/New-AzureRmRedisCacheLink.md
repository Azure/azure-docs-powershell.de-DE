---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
ms.openlocfilehash: f625c9180287166b01607c468c44b5e0623c11cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475957"
---
# <span data-ttu-id="7f7ae-101">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="7f7ae-101">New-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="7f7ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f7ae-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7ae-103">Erstellen Sie einen Link zur Geo-Replikation zwischen zwei zwischen Speicherungs-Caches.</span><span class="sxs-lookup"><span data-stu-id="7f7ae-103">Create a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f7ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f7ae-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f7ae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f7ae-105">DESCRIPTION</span></span>
<span data-ttu-id="7f7ae-106">Erstellen Sie einen Link zur Geo-Replikation zwischen zwei zwischen Speicherungs-Caches.</span><span class="sxs-lookup"><span data-stu-id="7f7ae-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="7f7ae-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f7ae-107">EXAMPLES</span></span>

### <span data-ttu-id="7f7ae-108">Beispiel 1: Erstellen einer Verknüpfung zwischen zwei Caches</span><span class="sxs-lookup"><span data-stu-id="7f7ae-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="7f7ae-109">Dieser Befehl erstellt einen Link zur Geo-Replikation zwischen mycache1 und mycache2.</span><span class="sxs-lookup"><span data-stu-id="7f7ae-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="7f7ae-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f7ae-110">PARAMETERS</span></span>

### <span data-ttu-id="7f7ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7ae-111">-DefaultProfile</span></span>
<span data-ttu-id="7f7ae-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f7ae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f7ae-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="7f7ae-113">-PrimaryServerName</span></span>
<span data-ttu-id="7f7ae-114">Name des primären, in Verbindung stehenden "nicht-Cache".</span><span class="sxs-lookup"><span data-stu-id="7f7ae-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="7f7ae-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="7f7ae-115">-SecondaryServerName</span></span>
<span data-ttu-id="7f7ae-116">Der Name des sekundären "a/a-Cache" in Link.</span><span class="sxs-lookup"><span data-stu-id="7f7ae-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="7f7ae-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7f7ae-117">-Confirm</span></span>
<span data-ttu-id="7f7ae-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f7ae-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f7ae-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f7ae-119">-WhatIf</span></span>
<span data-ttu-id="7f7ae-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f7ae-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f7ae-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f7ae-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f7ae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7ae-122">CommonParameters</span></span>
<span data-ttu-id="7f7ae-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f7ae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7ae-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f7ae-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7ae-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f7ae-125">INPUTS</span></span>

### <span data-ttu-id="7f7ae-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7f7ae-126">System.String</span></span>

## <span data-ttu-id="7f7ae-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f7ae-127">OUTPUTS</span></span>

### <span data-ttu-id="7f7ae-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="7f7ae-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="7f7ae-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f7ae-129">NOTES</span></span>

## <span data-ttu-id="7f7ae-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f7ae-130">RELATED LINKS</span></span>

[<span data-ttu-id="7f7ae-131">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="7f7ae-131">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="7f7ae-132">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="7f7ae-132">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="7f7ae-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7f7ae-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="7f7ae-134">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7f7ae-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="7f7ae-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7f7ae-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="7f7ae-136">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7f7ae-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
