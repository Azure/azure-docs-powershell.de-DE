---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: e24ea6e0b5bf88b17a6209f2ea69634200a10a62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825128"
---
# <span data-ttu-id="85105-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="85105-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="85105-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85105-102">SYNOPSIS</span></span>
<span data-ttu-id="85105-103">Entfernen einer Firewall-Regel aus einem Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="85105-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="85105-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85105-104">SYNTAX</span></span>

### <span data-ttu-id="85105-105">NormalParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="85105-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85105-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="85105-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85105-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85105-107">DESCRIPTION</span></span>
<span data-ttu-id="85105-108">Entfernen einer Firewall-Regel aus einem Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="85105-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="85105-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85105-109">EXAMPLES</span></span>

### <span data-ttu-id="85105-110">Beispiel 1: Entfernen einer einzelnen Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="85105-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="85105-111">Mit diesem Befehl wird eine Firewallregel mit dem Namen "ruleone" aus dem a/a-Cache "myCache" entfernt.</span><span class="sxs-lookup"><span data-stu-id="85105-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="85105-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="85105-112">PARAMETERS</span></span>

### <span data-ttu-id="85105-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85105-113">-DefaultProfile</span></span>
<span data-ttu-id="85105-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85105-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85105-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="85105-115">-InputObject</span></span>
<span data-ttu-id="85105-116">Objekt vom Typ PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="85105-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="85105-117">-Name</span><span class="sxs-lookup"><span data-stu-id="85105-117">-Name</span></span>
<span data-ttu-id="85105-118">Name des Zwischenspeichers mit dem Namenzeichen</span><span class="sxs-lookup"><span data-stu-id="85105-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="85105-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85105-119">-PassThru</span></span>
<span data-ttu-id="85105-120">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="85105-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="85105-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85105-121">-ResourceGroupName</span></span>
<span data-ttu-id="85105-122">Name der Ressourcengruppe, in der der Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="85105-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="85105-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="85105-123">-RuleName</span></span>
<span data-ttu-id="85105-124">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="85105-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="85105-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="85105-125">-Confirm</span></span>
<span data-ttu-id="85105-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85105-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85105-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85105-127">-WhatIf</span></span>
<span data-ttu-id="85105-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85105-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85105-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85105-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85105-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85105-130">CommonParameters</span></span>
<span data-ttu-id="85105-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85105-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85105-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85105-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85105-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85105-133">INPUTS</span></span>

### <span data-ttu-id="85105-134">System. String</span><span class="sxs-lookup"><span data-stu-id="85105-134">System.String</span></span>

### <span data-ttu-id="85105-135">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="85105-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="85105-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85105-136">OUTPUTS</span></span>

### <span data-ttu-id="85105-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85105-137">System.Boolean</span></span>

## <span data-ttu-id="85105-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="85105-138">NOTES</span></span>

## <span data-ttu-id="85105-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85105-139">RELATED LINKS</span></span>

[<span data-ttu-id="85105-140">Neu – AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="85105-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="85105-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="85105-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="85105-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="85105-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="85105-143">Neu – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="85105-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="85105-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="85105-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="85105-145">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="85105-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)