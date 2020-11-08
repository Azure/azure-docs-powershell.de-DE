---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/set-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: c2cc0e7a22d7e581eece9004950b54bc0151fad3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007075"
---
# <span data-ttu-id="f629b-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="f629b-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="f629b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f629b-102">SYNOPSIS</span></span>
<span data-ttu-id="f629b-103">Erstellen oder Aktualisieren eines Kontingents</span><span class="sxs-lookup"><span data-stu-id="f629b-103">Create or update a quota.</span></span>

## <span data-ttu-id="f629b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f629b-104">SYNTAX</span></span>

### <span data-ttu-id="f629b-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f629b-105">UpdateExpanded (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f629b-106">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f629b-106">Update</span></span>
```
Set-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f629b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f629b-107">DESCRIPTION</span></span>
<span data-ttu-id="f629b-108">Erstellen oder Aktualisieren eines Kontingents</span><span class="sxs-lookup"><span data-stu-id="f629b-108">Create or update a quota.</span></span>

## <span data-ttu-id="f629b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f629b-109">EXAMPLES</span></span>

### <span data-ttu-id="f629b-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f629b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="f629b-111">Aktualisieren eines Netzwerk Kontingents nach Namen</span><span class="sxs-lookup"><span data-stu-id="f629b-111">Update a network quota by name.</span></span>

### <span data-ttu-id="f629b-112">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f629b-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="f629b-113">Aktualisieren eines Netzwerk Kontingents nach Namen</span><span class="sxs-lookup"><span data-stu-id="f629b-113">Update a network quota by name.</span></span>

## <span data-ttu-id="f629b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f629b-114">PARAMETERS</span></span>

### <span data-ttu-id="f629b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f629b-115">-DefaultProfile</span></span>
<span data-ttu-id="f629b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f629b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f629b-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="f629b-117">-Location</span></span>
<span data-ttu-id="f629b-118">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f629b-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f629b-119">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f629b-119">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="f629b-120">Die maximale Anzahl von Last-Balancern, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-120">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f629b-121">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f629b-121">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="f629b-122">Die maximale Anzahl von NICs, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-122">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f629b-123">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f629b-123">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="f629b-124">Die maximale Anzahl von öffentlichen IP-Adressen, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-124">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f629b-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f629b-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="f629b-126">Die maximale Anzahl von Sicherheitsgruppen, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-126">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f629b-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f629b-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="f629b-128">Maximale Anzahl von virtuellen Netzwerk-Gateway-Verbindungen, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-128">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f629b-129">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f629b-129">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="f629b-130">Maximale Anzahl von virtuellen Netzwerkgateways, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-130">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f629b-131">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f629b-131">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="f629b-132">Die maximale Anzahl von virtuellen Netzwerken, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-132">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f629b-133">-Name</span><span class="sxs-lookup"><span data-stu-id="f629b-133">-Name</span></span>
<span data-ttu-id="f629b-134">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f629b-134">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f629b-135">-Kontingent</span><span class="sxs-lookup"><span data-stu-id="f629b-135">-Quota</span></span>
<span data-ttu-id="f629b-136">Netzwerk Kontingent Ressource</span><span class="sxs-lookup"><span data-stu-id="f629b-136">Network quota resource.</span></span>
<span data-ttu-id="f629b-137">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Kontingenteigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f629b-137">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f629b-138">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f629b-138">-SubscriptionId</span></span>
<span data-ttu-id="f629b-139">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f629b-139">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f629b-140">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f629b-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f629b-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="f629b-141">-Tag</span></span>
<span data-ttu-id="f629b-142">Liste der Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="f629b-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f629b-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f629b-143">-Confirm</span></span>
<span data-ttu-id="f629b-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f629b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f629b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f629b-145">-WhatIf</span></span>
<span data-ttu-id="f629b-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f629b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f629b-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f629b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f629b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f629b-148">CommonParameters</span></span>
<span data-ttu-id="f629b-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f629b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f629b-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f629b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f629b-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f629b-151">INPUTS</span></span>

### <span data-ttu-id="f629b-152">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="f629b-152">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

## <span data-ttu-id="f629b-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f629b-153">OUTPUTS</span></span>

### <span data-ttu-id="f629b-154">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="f629b-154">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="f629b-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="f629b-155">NOTES</span></span>

<span data-ttu-id="f629b-156">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f629b-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f629b-157">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f629b-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f629b-158">Kontingent <IQuota> : Netzwerk Kontingent Ressource.</span><span class="sxs-lookup"><span data-stu-id="f629b-158">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="f629b-159">`[Tag <IResourceTags>]`: Liste von Schlüsselwert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="f629b-159">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="f629b-160">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f629b-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximale Anzahl von Last-Balancern, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="f629b-162">`[MaxNicsPerSubscription <Int64?>]`: Maximale Anzahl von NICs, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-162">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="f629b-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximale Anzahl von öffentlichen IP-Adressen, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="f629b-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximale Anzahl von Sicherheitsgruppen, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="f629b-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximale Anzahl von virtuellen Netzwerk-Gateway-Verbindungen, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="f629b-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximale Anzahl von virtuellen Netzwerkgateways, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="f629b-167">`[MaxVnetsPerSubscription <Int64?>]`: Maximale Anzahl von virtuellen Netzwerken, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f629b-167">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="f629b-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f629b-168">RELATED LINKS</span></span>

