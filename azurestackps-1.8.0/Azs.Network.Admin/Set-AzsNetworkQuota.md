---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d20f84d91c110ae1f4e55508b33f758fc0d5583
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827907"
---
# <span data-ttu-id="ffad6-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="ffad6-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="ffad6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ffad6-102">SYNOPSIS</span></span>
<span data-ttu-id="ffad6-103">Erstellen oder Aktualisieren eines Kontingents</span><span class="sxs-lookup"><span data-stu-id="ffad6-103">Create or update a quota.</span></span>

## <span data-ttu-id="ffad6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffad6-104">SYNTAX</span></span>

### <span data-ttu-id="ffad6-105">Kontingente (Standard)</span><span class="sxs-lookup"><span data-stu-id="ffad6-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffad6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffad6-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffad6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ffad6-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffad6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ffad6-108">DESCRIPTION</span></span>
<span data-ttu-id="ffad6-109">Erstellen oder Aktualisieren eines Kontingents</span><span class="sxs-lookup"><span data-stu-id="ffad6-109">Create or update a quota.</span></span>

## <span data-ttu-id="ffad6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ffad6-110">EXAMPLES</span></span>

### <span data-ttu-id="ffad6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ffad6-111">EXAMPLE 1</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="ffad6-112">Aktualisieren eines Netzwerk Kontingents nach Namen</span><span class="sxs-lookup"><span data-stu-id="ffad6-112">Update a network quota by name.</span></span>

### <span data-ttu-id="ffad6-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ffad6-113">EXAMPLE 2</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="ffad6-114">Aktualisieren eines Netzwerk Kontingents nach Namen</span><span class="sxs-lookup"><span data-stu-id="ffad6-114">Update a network quota by name.</span></span>

## <span data-ttu-id="ffad6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffad6-115">PARAMETERS</span></span>

### <span data-ttu-id="ffad6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ffad6-116">-Name</span></span>
<span data-ttu-id="ffad6-117">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ffad6-117">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffad6-118">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ffad6-118">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="ffad6-119">Die maximal zulässige Anzahl von NICs pro Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ffad6-119">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffad6-120">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ffad6-120">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="ffad6-121">Die maximal zulässige öffentliche IP-Adresse pro Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ffad6-121">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffad6-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ffad6-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="ffad6-123">Die maximale Anzahl der pro Abonnement zulässigen virtuellen Netzwerk-Gateway-Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="ffad6-123">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffad6-124">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ffad6-124">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="ffad6-125">Die maximal-Anzahl der pro Abonnement zulässigen virtuellen Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="ffad6-125">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffad6-126">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ffad6-126">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="ffad6-127">Die maximale Anzahl von virtuellen Netzwerkgateways, die pro Abonnement zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ffad6-127">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffad6-128">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ffad6-128">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="ffad6-129">Die maximal zulässige Anzahl von Sicherheitsgruppen pro Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ffad6-129">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffad6-130">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ffad6-130">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="ffad6-131">Die maximal zulässige Anzahl von Lasten ausgleichseinheiten pro Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ffad6-131">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffad6-132">-Standort</span><span class="sxs-lookup"><span data-stu-id="ffad6-132">-Location</span></span>
<span data-ttu-id="ffad6-133">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ffad6-133">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffad6-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ffad6-134">-ResourceId</span></span>
<span data-ttu-id="ffad6-135">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ffad6-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffad6-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ffad6-136">-InputObject</span></span>
<span data-ttu-id="ffad6-137">Von Get-AzsNetworkQuota zurückgegebenes Posbbily-geändertes Netzwerk Kontingent</span><span class="sxs-lookup"><span data-stu-id="ffad6-137">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

```yaml
Type: Quota
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffad6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffad6-138">-WhatIf</span></span>
<span data-ttu-id="ffad6-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ffad6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffad6-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ffad6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffad6-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ffad6-141">-Confirm</span></span>
<span data-ttu-id="ffad6-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ffad6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffad6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffad6-143">CommonParameters</span></span>
<span data-ttu-id="ffad6-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffad6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffad6-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffad6-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffad6-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ffad6-146">INPUTS</span></span>

## <span data-ttu-id="ffad6-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ffad6-147">OUTPUTS</span></span>

### <span data-ttu-id="ffad6-148">Microsoft. AzureStack. Management. Network. admin. Models. Quota</span><span class="sxs-lookup"><span data-stu-id="ffad6-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="ffad6-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="ffad6-149">NOTES</span></span>

## <span data-ttu-id="ffad6-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ffad6-150">RELATED LINKS</span></span>
