---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 8e28951f826c5a049f345bb3182bda10e7de82fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003707"
---
# <span data-ttu-id="c867a-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c867a-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="c867a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c867a-102">SYNOPSIS</span></span>
<span data-ttu-id="c867a-103">Besorgen Sie sich die Firewall-Regeln für den Cache für den "a</span><span class="sxs-lookup"><span data-stu-id="c867a-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="c867a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c867a-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c867a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c867a-105">DESCRIPTION</span></span>
<span data-ttu-id="c867a-106">Wenn " **RuleName** "-Parameter angegeben wird, erhält das Cmdlet " **Get-AzRedisCacheFirewallRule** " Details zur angegebenen Firewallregel im Azure-Cache für den "".</span><span class="sxs-lookup"><span data-stu-id="c867a-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="c867a-107">Wenn nur **Name** angegeben wird, werden für diesen Vorgang alle Firewallregeln abgerufen, die für diesen freistellen-Cache verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c867a-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="c867a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c867a-108">EXAMPLES</span></span>

### <span data-ttu-id="c867a-109">Beispiel 1: Abrufen einer einzelnen Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="c867a-109">Example 1: Get a single firewall rule</span></span>
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

<span data-ttu-id="c867a-110">Dieser Befehl ruft die Firewallregel mit dem Namen "ruleone" aus dem a/a-Cache mit dem Namen myCache ab</span><span class="sxs-lookup"><span data-stu-id="c867a-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="c867a-111">Beispiel 2: Abrufen aller Firewallregeln</span><span class="sxs-lookup"><span data-stu-id="c867a-111">Example 2: Get all firewall rules</span></span>
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

<span data-ttu-id="c867a-112">Dieser Befehl ruft alle Firewallregeln aus dem a/a-Cache mit dem Namen myCache ab.</span><span class="sxs-lookup"><span data-stu-id="c867a-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="c867a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c867a-113">PARAMETERS</span></span>

### <span data-ttu-id="c867a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c867a-114">-DefaultProfile</span></span>
<span data-ttu-id="c867a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c867a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c867a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c867a-116">-Name</span></span>
<span data-ttu-id="c867a-117">Name des Zwischenspeichers mit dem Namenzeichen</span><span class="sxs-lookup"><span data-stu-id="c867a-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="c867a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c867a-118">-ResourceGroupName</span></span>
<span data-ttu-id="c867a-119">Name der Ressourcengruppe, in der der Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c867a-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="c867a-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="c867a-120">-RuleName</span></span>
<span data-ttu-id="c867a-121">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="c867a-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="c867a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c867a-122">CommonParameters</span></span>
<span data-ttu-id="c867a-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c867a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c867a-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c867a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c867a-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c867a-125">INPUTS</span></span>

### <span data-ttu-id="c867a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c867a-126">System.String</span></span>

## <span data-ttu-id="c867a-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c867a-127">OUTPUTS</span></span>

### <span data-ttu-id="c867a-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c867a-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="c867a-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="c867a-129">NOTES</span></span>

## <span data-ttu-id="c867a-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c867a-130">RELATED LINKS</span></span>

[<span data-ttu-id="c867a-131">Neu – AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c867a-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="c867a-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c867a-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="c867a-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c867a-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="c867a-134">Neu – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c867a-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="c867a-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c867a-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="c867a-136">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c867a-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)