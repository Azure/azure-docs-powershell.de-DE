---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a16b625c4624753943659ba796b169ef338888f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146564"
---
# <span data-ttu-id="b0a4e-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b0a4e-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="b0a4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0a4e-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a4e-103">Aktualisiert eine Front-End-IP-Konfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="b0a4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0a4e-104">SYNTAX</span></span>

### <span data-ttu-id="b0a4e-105">SetByResourceSubnet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0a4e-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a4e-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="b0a4e-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a4e-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0a4e-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0a4e-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0a4e-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0a4e-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b0a4e-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0a4e-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b0a4e-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0a4e-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0a4e-111">DESCRIPTION</span></span>
<span data-ttu-id="b0a4e-112">Das **Cmdlet Set-AzLoadBalancerFrontendIpConfig** aktualisiert eine Front-End-IP-Konfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-112">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="b0a4e-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b0a4e-113">EXAMPLES</span></span>

### <span data-ttu-id="b0a4e-114">Beispiel 1: Ändern der Front-End-IP-Konfiguration eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="b0a4e-114">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="b0a4e-115">Der erste Befehl ruft das virtuelle Subnetz namens Subnetz ab und speichert es dann in $Subnet Variable.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-115">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="b0a4e-116">Der zweite Befehl ruft den zugeordneten Lastenausgleich namens "MyLoadBalancer" ab und speichert ihn dann in der $slb Variable.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-116">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="b0a4e-117">Der dritte Befehl verwendet den Pipelineoperator, um den Lastenausgleich in $slb an Add-AzLoadBalancerFrontendIpConfig zu übergeben, wodurch eine Front-End-IP-Konfiguration namens "NewFrontend" für $slb.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-117">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="b0a4e-118">Der vierte Befehl übergibt den Lastenausgleich in $slb an **Set-AzLoadBalancerFrontendIpConfig,** wodurch die Front-End-IP-Konfiguration gespeichert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-118">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig**, which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="b0a4e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0a4e-119">PARAMETERS</span></span>

### <span data-ttu-id="b0a4e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a4e-120">-DefaultProfile</span></span>
<span data-ttu-id="b0a4e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0a4e-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b0a4e-122">-LoadBalancer</span></span>
<span data-ttu-id="b0a4e-123">Gibt einen Lastenausgleich an.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-123">Specifies a load balancer.</span></span>
<span data-ttu-id="b0a4e-124">Dieses Cmdlet aktualisiert eine Front-End-Konfiguration für den Lastenausgleich, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-124">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b0a4e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b0a4e-125">-Name</span></span>
<span data-ttu-id="b0a4e-126">Gibt den Namen der front-end-IP-Konfiguration an, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-126">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="b0a4e-127">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0a4e-127">-PrivateIpAddress</span></span>
<span data-ttu-id="b0a4e-128">Gibt die private IP-Adresse des Lastenausgleichs an, der der fest zu setzenden Front-End-IP-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-128">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="b0a4e-129">Geben Sie diesen Parameter nur an, wenn Sie auch den Parameter *"Subnet"* angeben.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-129">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="b0a4e-130">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="b0a4e-130">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="b0a4e-131">Die private IP-Adressversion der IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-131">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="b0a4e-132">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0a4e-132">-PublicIpAddress</span></span>
<span data-ttu-id="b0a4e-133">Gibt das **PublicIpAddress-Objekt** an, das der front-end-IP-Konfiguration zugeordnet ist, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-133">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="b0a4e-134">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b0a4e-134">-PublicIpAddressId</span></span>
<span data-ttu-id="b0a4e-135">Gibt die ID des **PublicIpAddress-Objekts** an, das der Front-End-IP-Konfiguration zugeordnet ist, die von diesem Cmdlet festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-135">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="b0a4e-136">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b0a4e-136">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="b0a4e-137">Gibt das **PublicIpAddressPrefix-Objekt** an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-137">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b0a4e-138">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="b0a4e-138">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="b0a4e-139">Gibt die ID des **PublicIpAddressPrefix-Objekts** an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-139">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b0a4e-140">-Subnet</span><span class="sxs-lookup"><span data-stu-id="b0a4e-140">-Subnet</span></span>
<span data-ttu-id="b0a4e-141">Gibt das **Subnetzobjekt** an, das die Front-End-IP-Konfiguration enthält, die von diesem Cmdlet festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-141">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="b0a4e-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b0a4e-142">-SubnetId</span></span>
<span data-ttu-id="b0a4e-143">Gibt die ID des Subnetzes an, das die Front-End-IP-Konfiguration enthält, die von diesem Cmdlet festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-143">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="b0a4e-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="b0a4e-144">-Zone</span></span>
<span data-ttu-id="b0a4e-145">Eine Liste der Verfügbarkeitszonen, in der die für die Ressource zugeordnete IP aufgeführt wird, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="b0a4e-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0a4e-146">-Confirm</span></span>
<span data-ttu-id="b0a4e-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0a4e-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b0a4e-148">-WhatIf</span></span>
<span data-ttu-id="b0a4e-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0a4e-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0a4e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a4e-151">CommonParameters</span></span>
<span data-ttu-id="b0a4e-152">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0a4e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a4e-153">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0a4e-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a4e-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b0a4e-154">INPUTS</span></span>

### <span data-ttu-id="b0a4e-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b0a4e-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b0a4e-156">System.String</span><span class="sxs-lookup"><span data-stu-id="b0a4e-156">System.String</span></span>

### <span data-ttu-id="b0a4e-157">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b0a4e-157">System.String[]</span></span>

### <span data-ttu-id="b0a4e-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b0a4e-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="b0a4e-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0a4e-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="b0a4e-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b0a4e-160">OUTPUTS</span></span>

### <span data-ttu-id="b0a4e-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b0a4e-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b0a4e-162">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b0a4e-162">NOTES</span></span>

## <span data-ttu-id="b0a4e-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b0a4e-163">RELATED LINKS</span></span>

[<span data-ttu-id="b0a4e-164">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b0a4e-164">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b0a4e-165">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b0a4e-165">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b0a4e-166">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b0a4e-166">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b0a4e-167">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b0a4e-167">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="b0a4e-168">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b0a4e-168">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b0a4e-169">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b0a4e-169">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


