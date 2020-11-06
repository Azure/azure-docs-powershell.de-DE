---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 231787f57061ff4e118510c3dc166915b39da436
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482801"
---
# <span data-ttu-id="23c9d-101">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="23c9d-101">Get-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="23c9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="23c9d-103">Besorgen Sie sich die Firewall-Regeln für den Cache für den "a</span><span class="sxs-lookup"><span data-stu-id="23c9d-103">Get firewall rules set on Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23c9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23c9d-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23c9d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23c9d-105">DESCRIPTION</span></span>
<span data-ttu-id="23c9d-106">Wenn " **RuleName** "-Parameter angegeben wird, erhält das Cmdlet " **Get-AzureRmRedisCacheFirewallRule** " Details zur angegebenen Firewallregel im Azure-Cache für den "".</span><span class="sxs-lookup"><span data-stu-id="23c9d-106">If **RuleName** parameter if provided, **Get-AzureRmRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="23c9d-107">Wenn nur **Name** angegeben wird, werden für diesen Vorgang alle Firewallregeln abgerufen, die für diesen freistellen-Cache verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="23c9d-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="23c9d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23c9d-108">EXAMPLES</span></span>

### <span data-ttu-id="23c9d-109">Beispiel 1: Abrufen einer einzelnen Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="23c9d-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="23c9d-110">Dieser Befehl ruft die Firewallregel mit dem Namen "ruleone" aus dem a/a-Cache mit dem Namen myCache ab</span><span class="sxs-lookup"><span data-stu-id="23c9d-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="23c9d-111">Beispiel 2: Abrufen aller Firewallregeln</span><span class="sxs-lookup"><span data-stu-id="23c9d-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache"

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

<span data-ttu-id="23c9d-112">Dieser Befehl ruft alle Firewallregeln aus dem a/a-Cache mit dem Namen myCache ab.</span><span class="sxs-lookup"><span data-stu-id="23c9d-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="23c9d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="23c9d-113">PARAMETERS</span></span>

### <span data-ttu-id="23c9d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23c9d-114">-DefaultProfile</span></span>
<span data-ttu-id="23c9d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23c9d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23c9d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="23c9d-116">-Name</span></span>
<span data-ttu-id="23c9d-117">Name des Zwischenspeichers mit dem Namenzeichen</span><span class="sxs-lookup"><span data-stu-id="23c9d-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="23c9d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23c9d-118">-ResourceGroupName</span></span>
<span data-ttu-id="23c9d-119">Name der Ressourcengruppe, in der der Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="23c9d-119">Name of resource group in which cache exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23c9d-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="23c9d-120">-RuleName</span></span>
<span data-ttu-id="23c9d-121">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="23c9d-121">Name of firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23c9d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23c9d-122">CommonParameters</span></span>
<span data-ttu-id="23c9d-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23c9d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23c9d-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23c9d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23c9d-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23c9d-125">INPUTS</span></span>

### <span data-ttu-id="23c9d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="23c9d-126">System.String</span></span>
<span data-ttu-id="23c9d-127">Sie können die Eingabe an dieses Cmdlet nach Name, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="23c9d-127">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="23c9d-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23c9d-128">OUTPUTS</span></span>

### <span data-ttu-id="23c9d-129">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule, Microsoft. Azure. Commands. RedisCache, Version = 4.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="23c9d-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="23c9d-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="23c9d-130">NOTES</span></span>

## <span data-ttu-id="23c9d-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23c9d-131">RELATED LINKS</span></span>

[<span data-ttu-id="23c9d-132">Neu – AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="23c9d-132">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="23c9d-133">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="23c9d-133">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="23c9d-134">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23c9d-134">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="23c9d-135">Neu – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23c9d-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="23c9d-136">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23c9d-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="23c9d-137">Satz-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23c9d-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
