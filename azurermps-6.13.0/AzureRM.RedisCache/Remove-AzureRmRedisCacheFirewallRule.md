---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 25c3d0c72539ecd74e25ed455b4afcf4211c0718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663644"
---
# <span data-ttu-id="9ba55-101">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9ba55-101">Remove-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="9ba55-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ba55-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba55-103">Entfernen einer Firewall-Regel aus einem Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="9ba55-103">Remove a firewall rule from a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ba55-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ba55-104">SYNTAX</span></span>

### <span data-ttu-id="9ba55-105">NormalParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ba55-105">NormalParameterSet (Default)</span></span>
```
Remove-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ba55-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="9ba55-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzureRmRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ba55-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ba55-107">DESCRIPTION</span></span>
<span data-ttu-id="9ba55-108">Entfernen einer Firewall-Regel aus einem Zwischenspeicher mit einem Zwischenspeicher.</span><span class="sxs-lookup"><span data-stu-id="9ba55-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="9ba55-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ba55-109">EXAMPLES</span></span>

### <span data-ttu-id="9ba55-110">Beispiel 1: Entfernen einer einzelnen Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="9ba55-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="9ba55-111">Mit diesem Befehl wird eine Firewallregel mit dem Namen "ruleone" aus dem a/a-Cache "myCache" entfernt.</span><span class="sxs-lookup"><span data-stu-id="9ba55-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="9ba55-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ba55-112">PARAMETERS</span></span>

### <span data-ttu-id="9ba55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba55-113">-DefaultProfile</span></span>
<span data-ttu-id="9ba55-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ba55-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ba55-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9ba55-115">-InputObject</span></span>
<span data-ttu-id="9ba55-116">Objekt vom Typ PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9ba55-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="9ba55-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9ba55-117">-Name</span></span>
<span data-ttu-id="9ba55-118">Name des Zwischenspeichers mit dem Namenzeichen</span><span class="sxs-lookup"><span data-stu-id="9ba55-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="9ba55-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ba55-119">-PassThru</span></span>
<span data-ttu-id="9ba55-120">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="9ba55-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9ba55-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba55-121">-ResourceGroupName</span></span>
<span data-ttu-id="9ba55-122">Name der Ressourcengruppe, in der der Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9ba55-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="9ba55-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="9ba55-123">-RuleName</span></span>
<span data-ttu-id="9ba55-124">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="9ba55-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="9ba55-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ba55-125">-Confirm</span></span>
<span data-ttu-id="9ba55-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ba55-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ba55-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ba55-127">-WhatIf</span></span>
<span data-ttu-id="9ba55-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ba55-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ba55-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ba55-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ba55-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba55-130">CommonParameters</span></span>
<span data-ttu-id="9ba55-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ba55-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba55-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ba55-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba55-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ba55-133">INPUTS</span></span>

### <span data-ttu-id="9ba55-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9ba55-134">System.String</span></span>

### <span data-ttu-id="9ba55-135">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9ba55-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>
<span data-ttu-id="9ba55-136">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9ba55-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9ba55-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ba55-137">OUTPUTS</span></span>

### <span data-ttu-id="9ba55-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ba55-138">System.Boolean</span></span>

## <span data-ttu-id="9ba55-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ba55-139">NOTES</span></span>

## <span data-ttu-id="9ba55-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ba55-140">RELATED LINKS</span></span>

[<span data-ttu-id="9ba55-141">Neu – AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9ba55-141">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="9ba55-142">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9ba55-142">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="9ba55-143">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9ba55-143">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="9ba55-144">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9ba55-144">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="9ba55-145">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9ba55-145">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="9ba55-146">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="9ba55-146">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
