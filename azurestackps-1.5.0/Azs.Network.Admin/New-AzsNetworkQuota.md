---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc762c4b7d932f682f77e2df6586c773e0f22e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475302"
---
# <span data-ttu-id="27868-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="27868-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="27868-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="27868-102">SYNOPSIS</span></span>
<span data-ttu-id="27868-103">Erstellen oder Aktualisieren eines Kontingents</span><span class="sxs-lookup"><span data-stu-id="27868-103">Create or update a quota.</span></span>

## <span data-ttu-id="27868-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="27868-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27868-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27868-105">DESCRIPTION</span></span>
<span data-ttu-id="27868-106">Erstellen oder Aktualisieren eines Kontingents</span><span class="sxs-lookup"><span data-stu-id="27868-106">Create or update a quota.</span></span>

## <span data-ttu-id="27868-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27868-107">EXAMPLES</span></span>

### <span data-ttu-id="27868-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="27868-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="27868-109">Erstellen Sie ein neues Netzwerk Kontingent mit allen Standardwerten.</span><span class="sxs-lookup"><span data-stu-id="27868-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="27868-110">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="27868-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="27868-111">Erstellen Sie ein neues Netzwerk Kontingent mit nicht Standardwerten für Kontingent.</span><span class="sxs-lookup"><span data-stu-id="27868-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="27868-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="27868-112">PARAMETERS</span></span>

### <span data-ttu-id="27868-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="27868-113">-Location</span></span>
<span data-ttu-id="27868-114">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="27868-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27868-115">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27868-115">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="27868-116">Die maximal zulässige Anzahl von Lasten ausgleichseinheiten pro Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27868-116">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27868-117">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27868-117">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="27868-118">Die maximal zulässige Anzahl von NICs pro Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27868-118">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27868-119">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27868-119">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="27868-120">Die maximal zulässige öffentliche IP-Adresse pro Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27868-120">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27868-121">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27868-121">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="27868-122">Die maximal zulässige Anzahl von Sicherheitsgruppen pro Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27868-122">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27868-123">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27868-123">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="27868-124">Die maximale Anzahl der pro Abonnement zulässigen virtuellen Netzwerk-Gateway-Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="27868-124">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27868-125">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27868-125">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="27868-126">Die maximale Anzahl von virtuellen Netzwerkgateways, die pro Abonnement zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="27868-126">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27868-127">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27868-127">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="27868-128">Die maximal-Anzahl der pro Abonnement zulässigen virtuellen Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="27868-128">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27868-129">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="27868-129">-MigrationPhase</span></span>
<span data-ttu-id="27868-130">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="27868-130">Deprecated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: Prepare
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27868-131">-Name</span><span class="sxs-lookup"><span data-stu-id="27868-131">-Name</span></span>
<span data-ttu-id="27868-132">Der Name der Netzwerk Kontingent Ressource.</span><span class="sxs-lookup"><span data-stu-id="27868-132">Name of the network quota resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27868-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="27868-133">-Confirm</span></span>
<span data-ttu-id="27868-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27868-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27868-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27868-135">-WhatIf</span></span>
<span data-ttu-id="27868-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27868-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27868-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27868-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27868-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27868-138">CommonParameters</span></span>
<span data-ttu-id="27868-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27868-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27868-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27868-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27868-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="27868-141">INPUTS</span></span>

## <span data-ttu-id="27868-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27868-142">OUTPUTS</span></span>

### <span data-ttu-id="27868-143">Microsoft. AzureStack. Management. Network. admin. Models. Quota</span><span class="sxs-lookup"><span data-stu-id="27868-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="27868-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="27868-144">NOTES</span></span>

## <span data-ttu-id="27868-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="27868-145">RELATED LINKS</span></span>

