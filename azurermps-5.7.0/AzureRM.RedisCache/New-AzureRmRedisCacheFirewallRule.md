---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: c89589d966c03614255751bf13769689ff875332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662722"
---
# <span data-ttu-id="1338c-101">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1338c-101">New-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="1338c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1338c-102">SYNOPSIS</span></span>
<span data-ttu-id="1338c-103">Erstellen Sie eine Firewallregel in einem Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="1338c-103">Create a firewall rule on a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1338c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1338c-104">SYNTAX</span></span>

### <span data-ttu-id="1338c-105">NormalParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1338c-105">NormalParameterSet (Default)</span></span>
```
New-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 -StartIP <String> -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1338c-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="1338c-106">RedisCacheAttributesObject</span></span>
```
New-AzureRmRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1338c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1338c-107">ResourceIdParameterSet</span></span>
```
New-AzureRmRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1338c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1338c-108">DESCRIPTION</span></span>
<span data-ttu-id="1338c-109">Erstellen Sie eine Firewallregel in einem Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="1338c-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="1338c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1338c-110">EXAMPLES</span></span>

### <span data-ttu-id="1338c-111">Beispiel 1: Erstellen einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="1338c-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="1338c-112">Dieser Befehl erstellt eine Firewallregel mit dem Namen "ruleone" auf dem Namen "myCache".</span><span class="sxs-lookup"><span data-stu-id="1338c-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="1338c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1338c-113">PARAMETERS</span></span>

### <span data-ttu-id="1338c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1338c-114">-DefaultProfile</span></span>
<span data-ttu-id="1338c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1338c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1338c-116">-IP</span><span class="sxs-lookup"><span data-stu-id="1338c-116">-EndIP</span></span>
<span data-ttu-id="1338c-117">IP-Adresse wird beendet.</span><span class="sxs-lookup"><span data-stu-id="1338c-117">Ending IP address.</span></span>

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

### <span data-ttu-id="1338c-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1338c-118">-InputObject</span></span>
<span data-ttu-id="1338c-119">Objekt vom Typ RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="1338c-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1338c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1338c-120">-Name</span></span>
<span data-ttu-id="1338c-121">Name des Zwischenspeichers mit dem Namenzeichen</span><span class="sxs-lookup"><span data-stu-id="1338c-121">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1338c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1338c-122">-ResourceGroupName</span></span>
<span data-ttu-id="1338c-123">Name der Ressourcengruppe, in der der Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1338c-123">Name of resource group in which cache exists.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1338c-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1338c-124">-ResourceId</span></span>
<span data-ttu-id="1338c-125">Arm-ID des a/a-Caches.</span><span class="sxs-lookup"><span data-stu-id="1338c-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1338c-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="1338c-126">-RuleName</span></span>
<span data-ttu-id="1338c-127">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="1338c-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="1338c-128">-IP</span><span class="sxs-lookup"><span data-stu-id="1338c-128">-StartIP</span></span>
<span data-ttu-id="1338c-129">IP-Adresse wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="1338c-129">Starting IP address.</span></span>

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

### <span data-ttu-id="1338c-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1338c-130">-Confirm</span></span>
<span data-ttu-id="1338c-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1338c-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1338c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1338c-132">-WhatIf</span></span>
<span data-ttu-id="1338c-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1338c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1338c-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1338c-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1338c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1338c-135">CommonParameters</span></span>
<span data-ttu-id="1338c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1338c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1338c-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1338c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1338c-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1338c-138">INPUTS</span></span>

### <span data-ttu-id="1338c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1338c-139">System.String</span></span>

## <span data-ttu-id="1338c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1338c-140">OUTPUTS</span></span>

### <span data-ttu-id="1338c-141">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1338c-141">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="1338c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="1338c-142">NOTES</span></span>

## <span data-ttu-id="1338c-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1338c-143">RELATED LINKS</span></span>

[<span data-ttu-id="1338c-144">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1338c-144">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="1338c-145">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1338c-145">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="1338c-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1338c-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="1338c-147">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1338c-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="1338c-148">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1338c-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="1338c-149">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1338c-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
