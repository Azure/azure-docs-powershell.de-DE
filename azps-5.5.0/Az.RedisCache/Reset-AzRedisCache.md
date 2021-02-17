---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: c2373bb4ef093a35abc12b14f55f4c977fc54d64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153796"
---
# <span data-ttu-id="a466c-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a466c-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="a466c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a466c-102">SYNOPSIS</span></span>
<span data-ttu-id="a466c-103">Startet die Knoten eines Caches neu.</span><span class="sxs-lookup"><span data-stu-id="a466c-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="a466c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a466c-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a466c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a466c-105">DESCRIPTION</span></span>
<span data-ttu-id="a466c-106">Das **Cmdlet "Reset-AzRedisCache"** startet die Knoten einer Azure Redis-Cache-Instanz neu.</span><span class="sxs-lookup"><span data-stu-id="a466c-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="a466c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a466c-107">EXAMPLES</span></span>

### <span data-ttu-id="a466c-108">Beispiel 1: Neustarten beider Knoten</span><span class="sxs-lookup"><span data-stu-id="a466c-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="a466c-109">Mit diesem Befehl werden beide Knoten für den Cache mit dem Namen "RedisCache06" neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="a466c-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="a466c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a466c-110">PARAMETERS</span></span>

### <span data-ttu-id="a466c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a466c-111">-DefaultProfile</span></span>
<span data-ttu-id="a466c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a466c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a466c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a466c-113">-Force</span></span>
<span data-ttu-id="a466c-114">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="a466c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a466c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a466c-115">-Name</span></span>
<span data-ttu-id="a466c-116">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="a466c-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a466c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a466c-117">-PassThru</span></span>
<span data-ttu-id="a466c-118">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der angibt, ob der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a466c-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="a466c-119">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a466c-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a466c-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="a466c-120">-RebootType</span></span>
<span data-ttu-id="a466c-121">Gibt an, welcher Knoten oder Knoten neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a466c-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="a466c-122">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="a466c-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a466c-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="a466c-123">PrimaryNode</span></span> 
- <span data-ttu-id="a466c-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="a466c-124">SecondaryNode</span></span> 
- <span data-ttu-id="a466c-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="a466c-125">AllNodes</span></span>

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

### <span data-ttu-id="a466c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a466c-126">-ResourceGroupName</span></span>
<span data-ttu-id="a466c-127">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="a466c-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="a466c-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="a466c-128">-ShardId</span></span>
<span data-ttu-id="a466c-129">Gibt die ID des Shards an, den dieses Cmdlet für einen Premiumcache mit aktivierter Clustering neu startet.</span><span class="sxs-lookup"><span data-stu-id="a466c-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="a466c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a466c-130">-Confirm</span></span>
<span data-ttu-id="a466c-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a466c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a466c-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a466c-132">-WhatIf</span></span>
<span data-ttu-id="a466c-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a466c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a466c-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a466c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a466c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a466c-135">CommonParameters</span></span>
<span data-ttu-id="a466c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a466c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a466c-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a466c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a466c-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a466c-138">INPUTS</span></span>

### <span data-ttu-id="a466c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a466c-139">System.String</span></span>

### <span data-ttu-id="a466c-140">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a466c-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a466c-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a466c-141">OUTPUTS</span></span>

### <span data-ttu-id="a466c-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a466c-142">System.Boolean</span></span>

## <span data-ttu-id="a466c-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a466c-143">NOTES</span></span>
* <span data-ttu-id="a466c-144">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="a466c-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a466c-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a466c-145">RELATED LINKS</span></span>

[<span data-ttu-id="a466c-146">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a466c-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="a466c-147">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a466c-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="a466c-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a466c-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="a466c-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a466c-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="a466c-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a466c-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


