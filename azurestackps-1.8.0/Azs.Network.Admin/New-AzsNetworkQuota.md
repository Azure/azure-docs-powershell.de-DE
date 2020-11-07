---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: acda4a136b98a8a83190704a3635bd97ae97a7b2
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827776"
---
# <span data-ttu-id="542d6-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="542d6-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="542d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="542d6-102">SYNOPSIS</span></span>
<span data-ttu-id="542d6-103">Erstellen oder Aktualisieren eines Kontingents</span><span class="sxs-lookup"><span data-stu-id="542d6-103">Create or update a quota.</span></span>

## <span data-ttu-id="542d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="542d6-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="542d6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="542d6-105">DESCRIPTION</span></span>
<span data-ttu-id="542d6-106">Erstellen oder Aktualisieren eines Kontingents</span><span class="sxs-lookup"><span data-stu-id="542d6-106">Create or update a quota.</span></span>

## <span data-ttu-id="542d6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="542d6-107">EXAMPLES</span></span>

### <span data-ttu-id="542d6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="542d6-108">EXAMPLE 1</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="542d6-109">Erstellen Sie ein neues Netzwerk Kontingent mit allen Standardwerten.</span><span class="sxs-lookup"><span data-stu-id="542d6-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="542d6-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="542d6-110">EXAMPLE 2</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="542d6-111">Erstellen Sie ein neues Netzwerk Kontingent mit nicht Standardwerten für Kontingent.</span><span class="sxs-lookup"><span data-stu-id="542d6-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="542d6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="542d6-112">PARAMETERS</span></span>

### <span data-ttu-id="542d6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="542d6-113">-Name</span></span>
<span data-ttu-id="542d6-114">Der Name der Netzwerk Kontingent Ressource.</span><span class="sxs-lookup"><span data-stu-id="542d6-114">Name of the network quota resource.</span></span>

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

### <span data-ttu-id="542d6-115">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="542d6-115">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="542d6-116">Die maximal zulässige Anzahl von NICs pro Abonnement.</span><span class="sxs-lookup"><span data-stu-id="542d6-116">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="542d6-117">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="542d6-117">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="542d6-118">Die maximal zulässige öffentliche IP-Adresse pro Abonnement.</span><span class="sxs-lookup"><span data-stu-id="542d6-118">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="542d6-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="542d6-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="542d6-120">Die maximale Anzahl der pro Abonnement zulässigen virtuellen Netzwerk-Gateway-Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="542d6-120">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="542d6-121">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="542d6-121">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="542d6-122">Die maximal-Anzahl der pro Abonnement zulässigen virtuellen Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="542d6-122">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="542d6-123">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="542d6-123">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="542d6-124">Die maximale Anzahl von virtuellen Netzwerkgateways, die pro Abonnement zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="542d6-124">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="542d6-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="542d6-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="542d6-126">Die maximal zulässige Anzahl von Sicherheitsgruppen pro Abonnement.</span><span class="sxs-lookup"><span data-stu-id="542d6-126">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="542d6-127">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="542d6-127">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="542d6-128">Die maximal zulässige Anzahl von Lasten ausgleichseinheiten pro Abonnement.</span><span class="sxs-lookup"><span data-stu-id="542d6-128">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="542d6-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="542d6-129">-Location</span></span>
<span data-ttu-id="542d6-130">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="542d6-130">Location of the resource.</span></span>

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

### <span data-ttu-id="542d6-131">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="542d6-131">-MigrationPhase</span></span>
<span data-ttu-id="542d6-132">Migrationsstatus wie "keine", "vorbereiten", "Commit" und "Abbrechen".</span><span class="sxs-lookup"><span data-stu-id="542d6-132">State of migration such as None, Prepare, Commit, and Abort.</span></span>

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

### <span data-ttu-id="542d6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="542d6-133">-WhatIf</span></span>
<span data-ttu-id="542d6-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="542d6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="542d6-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="542d6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="542d6-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="542d6-136">-Confirm</span></span>
<span data-ttu-id="542d6-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="542d6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="542d6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542d6-138">CommonParameters</span></span>
<span data-ttu-id="542d6-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="542d6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542d6-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="542d6-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542d6-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="542d6-141">INPUTS</span></span>

## <span data-ttu-id="542d6-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="542d6-142">OUTPUTS</span></span>

### <span data-ttu-id="542d6-143">Microsoft. AzureStack. Management. Network. admin. Models. Quota</span><span class="sxs-lookup"><span data-stu-id="542d6-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="542d6-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="542d6-144">NOTES</span></span>

## <span data-ttu-id="542d6-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="542d6-145">RELATED LINKS</span></span>
