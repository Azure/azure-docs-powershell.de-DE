---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: c19be1f524519a55a5a95a575e97cfd250952570
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169212"
---
# <span data-ttu-id="5cb0a-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5cb0a-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="5cb0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cb0a-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb0a-103">Entfernen Sie eine Firewallregel aus einem Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="5cb0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5cb0a-104">SYNTAX</span></span>

### <span data-ttu-id="5cb0a-105">NormalParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5cb0a-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cb0a-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="5cb0a-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cb0a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5cb0a-107">DESCRIPTION</span></span>
<span data-ttu-id="5cb0a-108">Entfernen Sie eine Firewallregel aus einem Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="5cb0a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5cb0a-109">EXAMPLES</span></span>

### <span data-ttu-id="5cb0a-110">Beispiel 1: Entfernen einer einzelnen Firewallregel</span><span class="sxs-lookup"><span data-stu-id="5cb0a-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="5cb0a-111">Mit diesem Befehl wird eine Firewallregel namens "ruleone" aus dem Redis Cache namens "mycache" entfernt.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="5cb0a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cb0a-112">PARAMETERS</span></span>

### <span data-ttu-id="5cb0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb0a-113">-DefaultProfile</span></span>
<span data-ttu-id="5cb0a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cb0a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cb0a-115">-InputObject</span></span>
<span data-ttu-id="5cb0a-116">Objekt vom Typ PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5cb0a-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb0a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5cb0a-117">-Name</span></span>
<span data-ttu-id="5cb0a-118">Name des Redis-Caches.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-118">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb0a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cb0a-119">-PassThru</span></span>
<span data-ttu-id="5cb0a-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5cb0a-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5cb0a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb0a-121">-ResourceGroupName</span></span>
<span data-ttu-id="5cb0a-122">Name der Ressourcengruppe, in der der Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-122">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb0a-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="5cb0a-123">-RuleName</span></span>
<span data-ttu-id="5cb0a-124">Name der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-124">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb0a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cb0a-125">-Confirm</span></span>
<span data-ttu-id="5cb0a-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cb0a-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5cb0a-127">-WhatIf</span></span>
<span data-ttu-id="5cb0a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cb0a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cb0a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb0a-130">CommonParameters</span></span>
<span data-ttu-id="5cb0a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb0a-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cb0a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb0a-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5cb0a-133">INPUTS</span></span>

### <span data-ttu-id="5cb0a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5cb0a-134">System.String</span></span>

### <span data-ttu-id="5cb0a-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5cb0a-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="5cb0a-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5cb0a-136">OUTPUTS</span></span>

### <span data-ttu-id="5cb0a-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5cb0a-137">System.Boolean</span></span>

## <span data-ttu-id="5cb0a-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5cb0a-138">NOTES</span></span>

## <span data-ttu-id="5cb0a-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5cb0a-139">RELATED LINKS</span></span>

[<span data-ttu-id="5cb0a-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5cb0a-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="5cb0a-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5cb0a-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="5cb0a-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5cb0a-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="5cb0a-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5cb0a-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="5cb0a-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5cb0a-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="5cb0a-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5cb0a-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)