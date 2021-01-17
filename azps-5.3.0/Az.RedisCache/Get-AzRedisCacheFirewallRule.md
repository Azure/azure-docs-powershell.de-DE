---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 8e28951f826c5a049f345bb3182bda10e7de82fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378270"
---
# <span data-ttu-id="7580f-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7580f-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="7580f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7580f-102">SYNOPSIS</span></span>
<span data-ttu-id="7580f-103">Richten Sie Firewallregeln für den Redis Cache ein.</span><span class="sxs-lookup"><span data-stu-id="7580f-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="7580f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7580f-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7580f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7580f-105">DESCRIPTION</span></span>
<span data-ttu-id="7580f-106">Wenn **der Parameter "RuleName"** angegeben ist, ruft das **Cmdlet "Get-AzRedisCacheFirewallRule"** Details zur angegebenen Firewallregel im Azure Redis Cache ab.</span><span class="sxs-lookup"><span data-stu-id="7580f-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="7580f-107">Wenn nur **"Name"** angegeben wird, sind durch diesen Vorgang alle Firewallregeln für diesen Redis Cache verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7580f-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="7580f-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7580f-108">EXAMPLES</span></span>

### <span data-ttu-id="7580f-109">Beispiel 1: Erhalten einer einzelnen Firewallregel</span><span class="sxs-lookup"><span data-stu-id="7580f-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="7580f-110">Dieser Befehl ruft die Firewallregel namens "ruleone" aus dem Redis Cache namens "mycache" ab.</span><span class="sxs-lookup"><span data-stu-id="7580f-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="7580f-111">Beispiel 2: Alle Firewallregeln erhalten</span><span class="sxs-lookup"><span data-stu-id="7580f-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruletwo
        RuleName          : ruletwo
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.33
        EndIP             : 10.0.0.64
```

<span data-ttu-id="7580f-112">Dieser Befehl ruft alle Firewallregeln aus dem Redis Cache namens mycache ab.</span><span class="sxs-lookup"><span data-stu-id="7580f-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="7580f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7580f-113">PARAMETERS</span></span>

### <span data-ttu-id="7580f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7580f-114">-DefaultProfile</span></span>
<span data-ttu-id="7580f-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7580f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7580f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7580f-116">-Name</span></span>
<span data-ttu-id="7580f-117">Name des Redis-Caches.</span><span class="sxs-lookup"><span data-stu-id="7580f-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="7580f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7580f-118">-ResourceGroupName</span></span>
<span data-ttu-id="7580f-119">Name der Ressourcengruppe, in der der Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7580f-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="7580f-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="7580f-120">-RuleName</span></span>
<span data-ttu-id="7580f-121">Name der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="7580f-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="7580f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7580f-122">CommonParameters</span></span>
<span data-ttu-id="7580f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7580f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7580f-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7580f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7580f-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7580f-125">INPUTS</span></span>

### <span data-ttu-id="7580f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7580f-126">System.String</span></span>

## <span data-ttu-id="7580f-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7580f-127">OUTPUTS</span></span>

### <span data-ttu-id="7580f-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7580f-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="7580f-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7580f-129">NOTES</span></span>

## <span data-ttu-id="7580f-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7580f-130">RELATED LINKS</span></span>

[<span data-ttu-id="7580f-131">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7580f-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="7580f-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7580f-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="7580f-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7580f-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="7580f-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7580f-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="7580f-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7580f-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="7580f-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7580f-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)