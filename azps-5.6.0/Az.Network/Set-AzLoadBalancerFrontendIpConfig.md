---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: ef9121f0962cc5ba06aa9c040d4647a1365fdf80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924571"
---
# <span data-ttu-id="7da58-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7da58-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="7da58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7da58-102">SYNOPSIS</span></span>
<span data-ttu-id="7da58-103">Aktualisiert eine Front-End-IP-Konfiguration für einen Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="7da58-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="7da58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7da58-104">SYNTAX</span></span>

### <span data-ttu-id="7da58-105">SetByResourceSubnet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7da58-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7da58-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="7da58-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7da58-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7da58-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7da58-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7da58-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7da58-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7da58-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7da58-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7da58-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7da58-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7da58-111">DESCRIPTION</span></span>
<span data-ttu-id="7da58-112">Das **Cmdlet Set-AzLoadBalancerFrontendIpConfig** aktualisiert eine Front-End-IP-Konfiguration für einen Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="7da58-112">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="7da58-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7da58-113">EXAMPLES</span></span>

### <span data-ttu-id="7da58-114">Beispiel 1: Ändern der Front-End-IP-Konfiguration eines Load Balancers</span><span class="sxs-lookup"><span data-stu-id="7da58-114">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="7da58-115">Der erste Befehl ruft das virtuelle Subnetz namens Subnetz ab und speichert es dann in der $Subnet Variable.</span><span class="sxs-lookup"><span data-stu-id="7da58-115">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="7da58-116">Der zweite Befehl ruft den zugeordneten Lastenausgleich mit dem Namen MyLoadBalancer ab und speichert ihn dann in $slb Variablen.</span><span class="sxs-lookup"><span data-stu-id="7da58-116">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="7da58-117">Der dritte Befehl verwendet den Pipelineoperator, um den Load Balancer in $slb an Add-AzLoadBalancerFrontendIpConfig zu übergeben, wodurch eine Front-End-IP-Konfiguration mit dem Namen NewFrontend für $slb.</span><span class="sxs-lookup"><span data-stu-id="7da58-117">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="7da58-118">Der vierte Befehl übergibt den Load Balancer in $slb an **Set-AzLoadBalancerFrontendIpConfig**, mit dem die Front-End-IP-Konfiguration gespeichert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7da58-118">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig**, which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="7da58-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7da58-119">PARAMETERS</span></span>

### <span data-ttu-id="7da58-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da58-120">-DefaultProfile</span></span>
<span data-ttu-id="7da58-121">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7da58-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7da58-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7da58-122">-LoadBalancer</span></span>
<span data-ttu-id="7da58-123">Gibt einen Lastenausgleich an.</span><span class="sxs-lookup"><span data-stu-id="7da58-123">Specifies a load balancer.</span></span>
<span data-ttu-id="7da58-124">Dieses Cmdlet aktualisiert eine Front-End-Konfiguration für den Load Balancer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7da58-124">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7da58-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7da58-125">-Name</span></span>
<span data-ttu-id="7da58-126">Gibt den Namen der festgelegten Front-End-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="7da58-126">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="7da58-127">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7da58-127">-PrivateIpAddress</span></span>
<span data-ttu-id="7da58-128">Gibt die private IP-Adresse des Load Balancers an, der der front-end-IP-Konfiguration zugeordnet ist, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7da58-128">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="7da58-129">Geben Sie diesen Parameter nur an, wenn Sie auch den *Parameter Subnetz* angeben.</span><span class="sxs-lookup"><span data-stu-id="7da58-129">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da58-130">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7da58-130">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="7da58-131">Die private IP-Adressversion der IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7da58-131">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da58-132">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7da58-132">-PublicIpAddress</span></span>
<span data-ttu-id="7da58-133">Gibt das **PublicIpAddress-Objekt** an, das der front-end-IP-Konfiguration zugeordnet ist, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7da58-133">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da58-134">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7da58-134">-PublicIpAddressId</span></span>
<span data-ttu-id="7da58-135">Gibt die ID des **PublicIpAddress-Objekts** an, das der front-end-IP-Konfiguration zugeordnet ist, die von diesem Cmdlet festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7da58-135">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da58-136">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7da58-136">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="7da58-137">Gibt das **PublicIpAddressPrefix-Objekt** an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7da58-137">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da58-138">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="7da58-138">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="7da58-139">Gibt die ID des **PublicIpAddressPrefix-Objekts** an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7da58-139">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da58-140">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="7da58-140">-Subnet</span></span>
<span data-ttu-id="7da58-141">Gibt das **Subnetzobjekt** an, das die von diesem Cmdlet festgelegte Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="7da58-141">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da58-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7da58-142">-SubnetId</span></span>
<span data-ttu-id="7da58-143">Gibt die ID des Subnetzes an, das die front-end-IP-Konfiguration enthält, die von diesem Cmdlet festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7da58-143">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da58-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="7da58-144">-Zone</span></span>
<span data-ttu-id="7da58-145">Eine Liste der Verfügbarkeitszonen, in der die für die Ressource zugewiesene IP bezeichnet wird, muss von stammen.</span><span class="sxs-lookup"><span data-stu-id="7da58-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da58-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7da58-146">-Confirm</span></span>
<span data-ttu-id="7da58-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7da58-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7da58-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7da58-148">-WhatIf</span></span>
<span data-ttu-id="7da58-149">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7da58-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7da58-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7da58-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7da58-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da58-151">CommonParameters</span></span>
<span data-ttu-id="7da58-152">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da58-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da58-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7da58-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da58-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7da58-154">INPUTS</span></span>

### <span data-ttu-id="7da58-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7da58-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="7da58-156">System.String</span><span class="sxs-lookup"><span data-stu-id="7da58-156">System.String</span></span>

### <span data-ttu-id="7da58-157">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7da58-157">System.String[]</span></span>

### <span data-ttu-id="7da58-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="7da58-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="7da58-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7da58-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7da58-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7da58-160">OUTPUTS</span></span>

### <span data-ttu-id="7da58-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7da58-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7da58-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7da58-162">NOTES</span></span>

## <span data-ttu-id="7da58-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7da58-163">RELATED LINKS</span></span>

[<span data-ttu-id="7da58-164">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7da58-164">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7da58-165">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7da58-165">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7da58-166">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7da58-166">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7da58-167">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7da58-167">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="7da58-168">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7da58-168">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7da58-169">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7da58-169">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


