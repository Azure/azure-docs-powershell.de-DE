---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/reset-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: df306f6bf97d47d87a78d0cefecff6c4d89020aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482782"
---
# <span data-ttu-id="465b4-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="465b4-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="465b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="465b4-102">SYNOPSIS</span></span>
<span data-ttu-id="465b4-103">Startet Knoten eines Caches neu.</span><span class="sxs-lookup"><span data-stu-id="465b4-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="465b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="465b4-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="465b4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="465b4-105">DESCRIPTION</span></span>
<span data-ttu-id="465b4-106">Mit dem Cmdlet **Reset-AzureRmRedisCache** werden die Knoten einer Azure-a-Cache-Instanz neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="465b4-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="465b4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="465b4-107">EXAMPLES</span></span>

### <span data-ttu-id="465b4-108">Beispiel 1: beide Knoten neu starten</span><span class="sxs-lookup"><span data-stu-id="465b4-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="465b4-109">Dieser Befehl startet beide Knoten für den Cache mit dem Namen "RedisCache06" neu.</span><span class="sxs-lookup"><span data-stu-id="465b4-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="465b4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="465b4-110">PARAMETERS</span></span>

### <span data-ttu-id="465b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="465b4-111">-DefaultProfile</span></span>
<span data-ttu-id="465b4-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="465b4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="465b4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="465b4-113">-Force</span></span>
<span data-ttu-id="465b4-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="465b4-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="465b4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="465b4-115">-Name</span></span>
<span data-ttu-id="465b4-116">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="465b4-116">Specifies the name of a cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="465b4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="465b4-117">-PassThru</span></span>
<span data-ttu-id="465b4-118">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der angibt, ob der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="465b4-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="465b4-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="465b4-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="465b4-120">-Reboottype</span><span class="sxs-lookup"><span data-stu-id="465b4-120">-RebootType</span></span>
<span data-ttu-id="465b4-121">Gibt an, welche Knoten oder Knoten neu gestartet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="465b4-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="465b4-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="465b4-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="465b4-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="465b4-123">PrimaryNode</span></span> 
- <span data-ttu-id="465b4-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="465b4-124">SecondaryNode</span></span> 
- <span data-ttu-id="465b4-125">Allnodes</span><span class="sxs-lookup"><span data-stu-id="465b4-125">AllNodes</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="465b4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="465b4-126">-ResourceGroupName</span></span>
<span data-ttu-id="465b4-127">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="465b4-127">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="465b4-128">-Scherbe</span><span class="sxs-lookup"><span data-stu-id="465b4-128">-ShardId</span></span>
<span data-ttu-id="465b4-129">Gibt die ID des Shard an, den dieses Cmdlet für einen Premium-Cache neu startet, wobei die Clusterfunktion aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="465b4-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="465b4-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="465b4-130">-Confirm</span></span>
<span data-ttu-id="465b4-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="465b4-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="465b4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="465b4-132">-WhatIf</span></span>
<span data-ttu-id="465b4-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="465b4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="465b4-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="465b4-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="465b4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="465b4-135">CommonParameters</span></span>
<span data-ttu-id="465b4-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="465b4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="465b4-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="465b4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="465b4-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="465b4-138">INPUTS</span></span>

### <span data-ttu-id="465b4-139">Keine</span><span class="sxs-lookup"><span data-stu-id="465b4-139">None</span></span>
<span data-ttu-id="465b4-140">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="465b4-140">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="465b4-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="465b4-141">OUTPUTS</span></span>

### <span data-ttu-id="465b4-142">Keine</span><span class="sxs-lookup"><span data-stu-id="465b4-142">None</span></span>

## <span data-ttu-id="465b4-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="465b4-143">NOTES</span></span>
* <span data-ttu-id="465b4-144">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="465b4-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="465b4-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="465b4-145">RELATED LINKS</span></span>

[<span data-ttu-id="465b4-146">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="465b4-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="465b4-147">Importieren-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="465b4-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="465b4-148">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="465b4-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="465b4-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="465b4-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="465b4-150">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="465b4-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


