---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 1bf6394621435293be1d00d4a9e9f435c160e668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824212"
---
# <span data-ttu-id="bd7fa-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bd7fa-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="bd7fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd7fa-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7fa-103">Besorgen Sie sich die Firewall-Regeln für den Cache für den "a</span><span class="sxs-lookup"><span data-stu-id="bd7fa-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="bd7fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd7fa-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd7fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd7fa-105">DESCRIPTION</span></span>
<span data-ttu-id="bd7fa-106">Wenn " **RuleName** "-Parameter angegeben wird, erhält das Cmdlet " **Get-AzRedisCacheFirewallRule** " Details zur angegebenen Firewallregel im Azure-Cache für den "".</span><span class="sxs-lookup"><span data-stu-id="bd7fa-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="bd7fa-107">Wenn nur **Name** angegeben wird, werden für diesen Vorgang alle Firewallregeln abgerufen, die für diesen freistellen-Cache verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="bd7fa-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="bd7fa-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd7fa-108">EXAMPLES</span></span>

### <span data-ttu-id="bd7fa-109">Beispiel 1: Abrufen einer einzelnen Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="bd7fa-109">Example 1: Get a single firewall rule</span></span>
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

<span data-ttu-id="bd7fa-110">Dieser Befehl ruft die Firewallregel mit dem Namen "ruleone" aus dem a/a-Cache mit dem Namen myCache ab</span><span class="sxs-lookup"><span data-stu-id="bd7fa-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="bd7fa-111">Beispiel 2: Abrufen aller Firewallregeln</span><span class="sxs-lookup"><span data-stu-id="bd7fa-111">Example 2: Get all firewall rules</span></span>
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

<span data-ttu-id="bd7fa-112">Dieser Befehl ruft alle Firewallregeln aus dem a/a-Cache mit dem Namen myCache ab.</span><span class="sxs-lookup"><span data-stu-id="bd7fa-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="bd7fa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd7fa-113">PARAMETERS</span></span>

### <span data-ttu-id="bd7fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7fa-114">-DefaultProfile</span></span>
<span data-ttu-id="bd7fa-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bd7fa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd7fa-116">-Name</span><span class="sxs-lookup"><span data-stu-id="bd7fa-116">-Name</span></span>
<span data-ttu-id="bd7fa-117">Name des Zwischenspeichers mit dem Namenzeichen</span><span class="sxs-lookup"><span data-stu-id="bd7fa-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="bd7fa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd7fa-118">-ResourceGroupName</span></span>
<span data-ttu-id="bd7fa-119">Name der Ressourcengruppe, in der der Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bd7fa-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="bd7fa-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="bd7fa-120">-RuleName</span></span>
<span data-ttu-id="bd7fa-121">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="bd7fa-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="bd7fa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7fa-122">CommonParameters</span></span>
<span data-ttu-id="bd7fa-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd7fa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7fa-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd7fa-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7fa-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd7fa-125">INPUTS</span></span>

### <span data-ttu-id="bd7fa-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bd7fa-126">System.String</span></span>

## <span data-ttu-id="bd7fa-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd7fa-127">OUTPUTS</span></span>

### <span data-ttu-id="bd7fa-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bd7fa-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="bd7fa-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd7fa-129">NOTES</span></span>

## <span data-ttu-id="bd7fa-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd7fa-130">RELATED LINKS</span></span>

[<span data-ttu-id="bd7fa-131">Neu – AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bd7fa-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="bd7fa-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bd7fa-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="bd7fa-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bd7fa-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="bd7fa-134">Neu – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bd7fa-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="bd7fa-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bd7fa-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="bd7fa-136">Satz-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bd7fa-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)