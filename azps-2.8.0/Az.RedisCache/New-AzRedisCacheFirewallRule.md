---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: dc52668a7d0f17d9cdbf9221a174228be1fa0f5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825160"
---
# <span data-ttu-id="c3c25-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c3c25-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="c3c25-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3c25-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c25-103">Erstellen Sie eine Firewallregel in einem Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="c3c25-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="c3c25-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3c25-104">SYNTAX</span></span>

### <span data-ttu-id="c3c25-105">NormalParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3c25-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3c25-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="c3c25-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3c25-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3c25-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3c25-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3c25-108">DESCRIPTION</span></span>
<span data-ttu-id="c3c25-109">Erstellen Sie eine Firewallregel in einem Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="c3c25-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="c3c25-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3c25-110">EXAMPLES</span></span>

### <span data-ttu-id="c3c25-111">Beispiel 1: Erstellen einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="c3c25-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="c3c25-112">Dieser Befehl erstellt eine Firewallregel mit dem Namen "ruleone" auf dem Namen "myCache".</span><span class="sxs-lookup"><span data-stu-id="c3c25-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="c3c25-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3c25-113">PARAMETERS</span></span>

### <span data-ttu-id="c3c25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c25-114">-DefaultProfile</span></span>
<span data-ttu-id="c3c25-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3c25-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3c25-116">-IP</span><span class="sxs-lookup"><span data-stu-id="c3c25-116">-EndIP</span></span>
<span data-ttu-id="c3c25-117">IP-Adresse wird beendet.</span><span class="sxs-lookup"><span data-stu-id="c3c25-117">Ending IP address.</span></span>

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

### <span data-ttu-id="c3c25-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3c25-118">-InputObject</span></span>
<span data-ttu-id="c3c25-119">Objekt vom Typ RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="c3c25-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="c3c25-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c3c25-120">-Name</span></span>
<span data-ttu-id="c3c25-121">Name des Zwischenspeichers mit dem Namenzeichen</span><span class="sxs-lookup"><span data-stu-id="c3c25-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="c3c25-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3c25-122">-ResourceGroupName</span></span>
<span data-ttu-id="c3c25-123">Name der Ressourcengruppe, in der der Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c3c25-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="c3c25-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c3c25-124">-ResourceId</span></span>
<span data-ttu-id="c3c25-125">Arm-ID des a/a-Caches.</span><span class="sxs-lookup"><span data-stu-id="c3c25-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="c3c25-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="c3c25-126">-RuleName</span></span>
<span data-ttu-id="c3c25-127">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="c3c25-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="c3c25-128">-IP</span><span class="sxs-lookup"><span data-stu-id="c3c25-128">-StartIP</span></span>
<span data-ttu-id="c3c25-129">IP-Adresse wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="c3c25-129">Starting IP address.</span></span>

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

### <span data-ttu-id="c3c25-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3c25-130">-Confirm</span></span>
<span data-ttu-id="c3c25-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3c25-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3c25-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3c25-132">-WhatIf</span></span>
<span data-ttu-id="c3c25-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3c25-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3c25-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3c25-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3c25-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c25-135">CommonParameters</span></span>
<span data-ttu-id="c3c25-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3c25-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c25-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3c25-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c25-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3c25-138">INPUTS</span></span>

### <span data-ttu-id="c3c25-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c3c25-139">System.String</span></span>

### <span data-ttu-id="c3c25-140">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="c3c25-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="c3c25-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3c25-141">OUTPUTS</span></span>

### <span data-ttu-id="c3c25-142">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c3c25-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="c3c25-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3c25-143">NOTES</span></span>

## <span data-ttu-id="c3c25-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3c25-144">RELATED LINKS</span></span>

[<span data-ttu-id="c3c25-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c3c25-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="c3c25-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c3c25-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="c3c25-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c3c25-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="c3c25-148">Neu – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c3c25-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="c3c25-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c3c25-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="c3c25-150">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c3c25-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)