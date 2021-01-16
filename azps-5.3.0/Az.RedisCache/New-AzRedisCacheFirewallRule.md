---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460863"
---
# <span data-ttu-id="90f00-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="90f00-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="90f00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90f00-102">SYNOPSIS</span></span>
<span data-ttu-id="90f00-103">Erstellen Sie eine Firewallregel in einem Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="90f00-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="90f00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90f00-104">SYNTAX</span></span>

### <span data-ttu-id="90f00-105">NormalParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="90f00-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f00-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="90f00-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f00-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90f00-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90f00-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90f00-108">DESCRIPTION</span></span>
<span data-ttu-id="90f00-109">Erstellen Sie eine Firewallregel in einem Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="90f00-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="90f00-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="90f00-110">EXAMPLES</span></span>

### <span data-ttu-id="90f00-111">Beispiel 1: Erstellen einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="90f00-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="90f00-112">Mit diesem Befehl wird eine Firewallregel namens "ruleone" im Redis Cache namens "mycache" erstellt.</span><span class="sxs-lookup"><span data-stu-id="90f00-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="90f00-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90f00-113">PARAMETERS</span></span>

### <span data-ttu-id="90f00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90f00-114">-DefaultProfile</span></span>
<span data-ttu-id="90f00-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90f00-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90f00-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="90f00-116">-EndIP</span></span>
<span data-ttu-id="90f00-117">Beenden der IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="90f00-117">Ending IP address.</span></span>

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

### <span data-ttu-id="90f00-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90f00-118">-InputObject</span></span>
<span data-ttu-id="90f00-119">Objekt vom Typ "RedisCacheAttributes"</span><span class="sxs-lookup"><span data-stu-id="90f00-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90f00-120">-Name</span><span class="sxs-lookup"><span data-stu-id="90f00-120">-Name</span></span>
<span data-ttu-id="90f00-121">Name des Redis-Caches.</span><span class="sxs-lookup"><span data-stu-id="90f00-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="90f00-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90f00-122">-ResourceGroupName</span></span>
<span data-ttu-id="90f00-123">Name der Ressourcengruppe, in der der Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="90f00-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="90f00-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90f00-124">-ResourceId</span></span>
<span data-ttu-id="90f00-125">ARM-ID von Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="90f00-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f00-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="90f00-126">-RuleName</span></span>
<span data-ttu-id="90f00-127">Name der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="90f00-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="90f00-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="90f00-128">-StartIP</span></span>
<span data-ttu-id="90f00-129">Start-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="90f00-129">Starting IP address.</span></span>

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

### <span data-ttu-id="90f00-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90f00-130">-Confirm</span></span>
<span data-ttu-id="90f00-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90f00-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90f00-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="90f00-132">-WhatIf</span></span>
<span data-ttu-id="90f00-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90f00-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90f00-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90f00-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90f00-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f00-135">CommonParameters</span></span>
<span data-ttu-id="90f00-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90f00-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f00-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90f00-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f00-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="90f00-138">INPUTS</span></span>

### <span data-ttu-id="90f00-139">System.String</span><span class="sxs-lookup"><span data-stu-id="90f00-139">System.String</span></span>

### <span data-ttu-id="90f00-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="90f00-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="90f00-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="90f00-141">OUTPUTS</span></span>

### <span data-ttu-id="90f00-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="90f00-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="90f00-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="90f00-143">NOTES</span></span>

## <span data-ttu-id="90f00-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="90f00-144">RELATED LINKS</span></span>

[<span data-ttu-id="90f00-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="90f00-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="90f00-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="90f00-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="90f00-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90f00-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="90f00-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90f00-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="90f00-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90f00-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="90f00-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90f00-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)