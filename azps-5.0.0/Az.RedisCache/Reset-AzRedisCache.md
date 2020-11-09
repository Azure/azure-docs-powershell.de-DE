---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: c2373bb4ef093a35abc12b14f55f4c977fc54d64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302638"
---
# <span data-ttu-id="3a1ae-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a1ae-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="3a1ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="3a1ae-103">Startet Knoten eines Caches neu.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="3a1ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a1ae-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a1ae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a1ae-105">DESCRIPTION</span></span>
<span data-ttu-id="3a1ae-106">Mit dem Cmdlet **Reset-AzRedisCache** werden die Knoten einer Azure-a-Cache-Instanz neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="3a1ae-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a1ae-107">EXAMPLES</span></span>

### <span data-ttu-id="3a1ae-108">Beispiel 1: beide Knoten neu starten</span><span class="sxs-lookup"><span data-stu-id="3a1ae-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="3a1ae-109">Dieser Befehl startet beide Knoten für den Cache mit dem Namen "RedisCache06" neu.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="3a1ae-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a1ae-110">PARAMETERS</span></span>

### <span data-ttu-id="3a1ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a1ae-111">-DefaultProfile</span></span>
<span data-ttu-id="3a1ae-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a1ae-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3a1ae-113">-Force</span></span>
<span data-ttu-id="3a1ae-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a1ae-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3a1ae-115">-Name</span></span>
<span data-ttu-id="3a1ae-116">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="3a1ae-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a1ae-117">-PassThru</span></span>
<span data-ttu-id="3a1ae-118">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der angibt, ob der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="3a1ae-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a1ae-120">-Reboottype</span><span class="sxs-lookup"><span data-stu-id="3a1ae-120">-RebootType</span></span>
<span data-ttu-id="3a1ae-121">Gibt an, welche Knoten oder Knoten neu gestartet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="3a1ae-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3a1ae-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3a1ae-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="3a1ae-123">PrimaryNode</span></span> 
- <span data-ttu-id="3a1ae-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="3a1ae-124">SecondaryNode</span></span> 
- <span data-ttu-id="3a1ae-125">Allnodes</span><span class="sxs-lookup"><span data-stu-id="3a1ae-125">AllNodes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a1ae-126">-ResourceGroupName</span></span>
<span data-ttu-id="3a1ae-127">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-127">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ae-128">-Scherbe</span><span class="sxs-lookup"><span data-stu-id="3a1ae-128">-ShardId</span></span>
<span data-ttu-id="3a1ae-129">Gibt die ID des Shard an, den dieses Cmdlet für einen Premium-Cache neu startet, wobei die Clusterfunktion aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ae-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a1ae-130">-Confirm</span></span>
<span data-ttu-id="3a1ae-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a1ae-132">-WhatIf</span></span>
<span data-ttu-id="3a1ae-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a1ae-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a1ae-135">CommonParameters</span></span>
<span data-ttu-id="3a1ae-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a1ae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a1ae-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a1ae-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a1ae-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a1ae-138">INPUTS</span></span>

### <span data-ttu-id="3a1ae-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3a1ae-139">System.String</span></span>

### <span data-ttu-id="3a1ae-140">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3a1ae-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3a1ae-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a1ae-141">OUTPUTS</span></span>

### <span data-ttu-id="3a1ae-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a1ae-142">System.Boolean</span></span>

## <span data-ttu-id="3a1ae-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a1ae-143">NOTES</span></span>
* <span data-ttu-id="3a1ae-144">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="3a1ae-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="3a1ae-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a1ae-145">RELATED LINKS</span></span>

[<span data-ttu-id="3a1ae-146">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a1ae-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="3a1ae-147">Importieren-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a1ae-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="3a1ae-148">Neu – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a1ae-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="3a1ae-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a1ae-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="3a1ae-150">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a1ae-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


