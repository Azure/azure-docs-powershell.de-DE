---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/new-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: 554ebe0e6c4ef8a4b0d262071595c0dc6336f482
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842528"
---
# <span data-ttu-id="c74ae-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="c74ae-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="c74ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c74ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c74ae-103">Erstellen oder Aktualisieren eines Kontingents</span><span class="sxs-lookup"><span data-stu-id="c74ae-103">Create or update a quota.</span></span>

## <span data-ttu-id="c74ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c74ae-104">SYNTAX</span></span>

### <span data-ttu-id="c74ae-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c74ae-105">CreateExpanded (Default)</span></span>
```
New-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c74ae-106">Erstellen</span><span class="sxs-lookup"><span data-stu-id="c74ae-106">Create</span></span>
```
New-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c74ae-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c74ae-107">CreateViaIdentity</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> -Quota <IQuota> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c74ae-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c74ae-108">CreateViaIdentityExpanded</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-MaxLoadBalancersPerSubscription <Int64>]
 [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxSecurityGroupsPerSubscription <Int64>] [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c74ae-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c74ae-109">DESCRIPTION</span></span>
<span data-ttu-id="c74ae-110">Erstellen oder Aktualisieren eines Kontingents</span><span class="sxs-lookup"><span data-stu-id="c74ae-110">Create or update a quota.</span></span>

## <span data-ttu-id="c74ae-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c74ae-111">EXAMPLES</span></span>

### <span data-ttu-id="c74ae-112">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c74ae-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="c74ae-113">Erstellen Sie ein neues Netzwerk Kontingent mit allen Standardwerten.</span><span class="sxs-lookup"><span data-stu-id="c74ae-113">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="c74ae-114">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c74ae-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```
<span data-ttu-id="c74ae-115">Erstellen Sie ein neues Netzwerk Kontingent mit nicht Standardwerten für Kontingent.</span><span class="sxs-lookup"><span data-stu-id="c74ae-115">Create a new network quota with non default values for quota.</span></span>



## <span data-ttu-id="c74ae-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c74ae-116">PARAMETERS</span></span>

### <span data-ttu-id="c74ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c74ae-117">-DefaultProfile</span></span>
<span data-ttu-id="c74ae-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c74ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c74ae-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c74ae-119">-InputObject</span></span>
<span data-ttu-id="c74ae-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c74ae-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c74ae-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="c74ae-121">-Location</span></span>
<span data-ttu-id="c74ae-122">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c74ae-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c74ae-123">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="c74ae-123">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="c74ae-124">Die maximale Anzahl von Last-Balancern, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-124">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c74ae-125">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="c74ae-125">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="c74ae-126">Die maximale Anzahl von NICs, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-126">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c74ae-127">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="c74ae-127">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="c74ae-128">Die maximale Anzahl von öffentlichen IP-Adressen, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-128">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c74ae-129">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="c74ae-129">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="c74ae-130">Die maximale Anzahl von Sicherheitsgruppen, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-130">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c74ae-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="c74ae-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="c74ae-132">Maximale Anzahl von virtuellen Netzwerk-Gateway-Verbindungen, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-132">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c74ae-133">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="c74ae-133">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="c74ae-134">Maximale Anzahl von virtuellen Netzwerkgateways, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-134">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c74ae-135">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="c74ae-135">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="c74ae-136">Die maximale Anzahl von virtuellen Netzwerken, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-136">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c74ae-137">-Name</span><span class="sxs-lookup"><span data-stu-id="c74ae-137">-Name</span></span>
<span data-ttu-id="c74ae-138">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c74ae-138">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c74ae-139">-Kontingent</span><span class="sxs-lookup"><span data-stu-id="c74ae-139">-Quota</span></span>
<span data-ttu-id="c74ae-140">Netzwerk Kontingent Ressource</span><span class="sxs-lookup"><span data-stu-id="c74ae-140">Network quota resource.</span></span>
<span data-ttu-id="c74ae-141">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Kontingenteigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c74ae-141">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c74ae-142">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c74ae-142">-SubscriptionId</span></span>
<span data-ttu-id="c74ae-143">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c74ae-143">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c74ae-144">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c74ae-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c74ae-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="c74ae-145">-Tag</span></span>
<span data-ttu-id="c74ae-146">Liste der Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="c74ae-146">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c74ae-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c74ae-147">-Confirm</span></span>
<span data-ttu-id="c74ae-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c74ae-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c74ae-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c74ae-149">-WhatIf</span></span>
<span data-ttu-id="c74ae-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c74ae-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c74ae-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c74ae-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c74ae-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c74ae-152">CommonParameters</span></span>
<span data-ttu-id="c74ae-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c74ae-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c74ae-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c74ae-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c74ae-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c74ae-155">INPUTS</span></span>

### <span data-ttu-id="c74ae-156">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="c74ae-156">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

### <span data-ttu-id="c74ae-157">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c74ae-157">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="c74ae-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c74ae-158">OUTPUTS</span></span>

### <span data-ttu-id="c74ae-159">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="c74ae-159">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="c74ae-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="c74ae-160">NOTES</span></span>

<span data-ttu-id="c74ae-161">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c74ae-161">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c74ae-162">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c74ae-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c74ae-163">Inputobject <INetworkAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="c74ae-163">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c74ae-164">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="c74ae-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c74ae-165">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c74ae-165">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c74ae-166">`[ResourceName <String>]`: Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c74ae-166">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="c74ae-167">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c74ae-167">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c74ae-168">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c74ae-168">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="c74ae-169">Kontingent <IQuota> : Netzwerk Kontingent Ressource.</span><span class="sxs-lookup"><span data-stu-id="c74ae-169">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="c74ae-170">`[Tag <IResourceTags>]`: Liste von Schlüsselwert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="c74ae-170">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="c74ae-171">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c74ae-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximale Anzahl von Last-Balancern, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="c74ae-173">`[MaxNicsPerSubscription <Int64?>]`: Maximale Anzahl von NICs, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-173">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="c74ae-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximale Anzahl von öffentlichen IP-Adressen, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="c74ae-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximale Anzahl von Sicherheitsgruppen, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="c74ae-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximale Anzahl von virtuellen Netzwerk-Gateway-Verbindungen, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="c74ae-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximale Anzahl von virtuellen Netzwerkgateways, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="c74ae-178">`[MaxVnetsPerSubscription <Int64?>]`: Maximale Anzahl von virtuellen Netzwerken, die ein Mandanten Abonnement bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c74ae-178">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="c74ae-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c74ae-179">RELATED LINKS</span></span>

