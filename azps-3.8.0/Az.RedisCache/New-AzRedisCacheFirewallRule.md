---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996035"
---
# <span data-ttu-id="41220-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="41220-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="41220-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41220-102">SYNOPSIS</span></span>
<span data-ttu-id="41220-103">Erstellen Sie eine Firewallregel in einem Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="41220-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="41220-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41220-104">SYNTAX</span></span>

### <span data-ttu-id="41220-105">NormalParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="41220-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41220-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="41220-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41220-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41220-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41220-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41220-108">DESCRIPTION</span></span>
<span data-ttu-id="41220-109">Erstellen Sie eine Firewallregel in einem Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="41220-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="41220-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41220-110">EXAMPLES</span></span>

### <span data-ttu-id="41220-111">Beispiel 1: Erstellen einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="41220-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="41220-112">Dieser Befehl erstellt eine Firewallregel mit dem Namen "ruleone" auf dem Namen "myCache".</span><span class="sxs-lookup"><span data-stu-id="41220-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="41220-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="41220-113">PARAMETERS</span></span>

### <span data-ttu-id="41220-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41220-114">-DefaultProfile</span></span>
<span data-ttu-id="41220-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="41220-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41220-116">-IP</span><span class="sxs-lookup"><span data-stu-id="41220-116">-EndIP</span></span>
<span data-ttu-id="41220-117">IP-Adresse wird beendet.</span><span class="sxs-lookup"><span data-stu-id="41220-117">Ending IP address.</span></span>

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

### <span data-ttu-id="41220-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="41220-118">-InputObject</span></span>
<span data-ttu-id="41220-119">Objekt vom Typ RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="41220-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="41220-120">-Name</span><span class="sxs-lookup"><span data-stu-id="41220-120">-Name</span></span>
<span data-ttu-id="41220-121">Name des Zwischenspeichers mit dem Namenzeichen</span><span class="sxs-lookup"><span data-stu-id="41220-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="41220-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41220-122">-ResourceGroupName</span></span>
<span data-ttu-id="41220-123">Name der Ressourcengruppe, in der der Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="41220-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="41220-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="41220-124">-ResourceId</span></span>
<span data-ttu-id="41220-125">Arm-ID des a/a-Caches.</span><span class="sxs-lookup"><span data-stu-id="41220-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="41220-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="41220-126">-RuleName</span></span>
<span data-ttu-id="41220-127">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="41220-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="41220-128">-IP</span><span class="sxs-lookup"><span data-stu-id="41220-128">-StartIP</span></span>
<span data-ttu-id="41220-129">IP-Adresse wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="41220-129">Starting IP address.</span></span>

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

### <span data-ttu-id="41220-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="41220-130">-Confirm</span></span>
<span data-ttu-id="41220-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41220-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41220-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41220-132">-WhatIf</span></span>
<span data-ttu-id="41220-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41220-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41220-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41220-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41220-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41220-135">CommonParameters</span></span>
<span data-ttu-id="41220-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41220-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41220-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41220-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41220-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41220-138">INPUTS</span></span>

### <span data-ttu-id="41220-139">System. String</span><span class="sxs-lookup"><span data-stu-id="41220-139">System.String</span></span>

### <span data-ttu-id="41220-140">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="41220-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="41220-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41220-141">OUTPUTS</span></span>

### <span data-ttu-id="41220-142">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="41220-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="41220-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="41220-143">NOTES</span></span>

## <span data-ttu-id="41220-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41220-144">RELATED LINKS</span></span>

[<span data-ttu-id="41220-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="41220-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="41220-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="41220-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="41220-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="41220-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="41220-148">Neu – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="41220-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="41220-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="41220-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="41220-150">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="41220-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)