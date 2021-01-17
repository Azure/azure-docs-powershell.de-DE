---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 68bcbcf0aa99ee4ee1a40c038e3eb5255deb690a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361541"
---
# <span data-ttu-id="d292d-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d292d-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="d292d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d292d-102">SYNOPSIS</span></span>
<span data-ttu-id="d292d-103">Fügt einem Lastenausgleich eine Front-End-IP-Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="d292d-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="d292d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d292d-104">SYNTAX</span></span>

### <span data-ttu-id="d292d-105">SetByResourceSubnet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d292d-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d292d-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="d292d-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d292d-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d292d-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d292d-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d292d-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d292d-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d292d-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d292d-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d292d-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d292d-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d292d-111">DESCRIPTION</span></span>
<span data-ttu-id="d292d-112">Das **Cmdlet "Add-AzLoadBalancerFrontendIpConfig"** fügt einem Azure Load Balancer eine Front-End-IP-Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="d292d-112">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="d292d-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d292d-113">EXAMPLES</span></span>

### <span data-ttu-id="d292d-114">Beispiel 1 Hinzufügen einer Front-End-IP-Konfiguration mit einer dynamischen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="d292d-114">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="d292d-115">Der erste Befehl ruft das virtuelle Azure-Netzwerk namens MyVnet ab und übergibt das Ergebnis über die Pipeline an das **Cmdlet "Get-AzVirtualNetworkSubnetConfig",** um das Subnetz namens "MySubnet" zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d292d-115">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="d292d-116">Der Befehl speichert dann das Ergebnis in der Variablen namens $Subnet.</span><span class="sxs-lookup"><span data-stu-id="d292d-116">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="d292d-117">Der zweite Befehl ruft den Lastenausgleich namens "MyLB" ab und übergibt das Ergebnis an das **Add-AzLoadBalancerFrontendIpConfig-Cmdlet,** das dem Lastenausgleich eine Front-End-IP-Konfiguration mit einer dynamischen privaten IP-Adresse aus dem Subnetz hinzufügt, das in der Variablen namens $MySubnet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d292d-117">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="d292d-118">Beispiel 2 Hinzufügen einer Front-End-IP-Konfiguration mit einer statischen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="d292d-118">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="d292d-119">Der erste Befehl ruft das virtuelle Azure-Netzwerk namens MyVnet ab und übergibt das Ergebnis über die Pipeline an das **Cmdlet "Get-AzVirtualNetworkSubnetConfig",** um das Subnetz namens "MySubnet" zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d292d-119">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="d292d-120">Der Befehl speichert dann das Ergebnis in der Variablen namens $Subnet.</span><span class="sxs-lookup"><span data-stu-id="d292d-120">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="d292d-121">Der zweite Befehl ruft den Lastenausgleich namens "MyLB" ab und übergibt das Ergebnis an das **Add-AzLoadBalancerFrontendIpConfig-Cmdlet,** das dem Lastenausgleich eine Front-End-IP-Konfiguration mit einer statischen privaten IP-Adresse aus dem Subnetz hinzufügt, das in der Variablen namens $Subnet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d292d-121">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="d292d-122">Beispiel 3 Hinzufügen einer Front-End-IP-Konfiguration mit einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="d292d-122">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\> $PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="d292d-123">Der erste Befehl ruft die öffentliche Azure-IP-Adresse "MyPub" ab und speichert das Ergebnis in der Variablen namens $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="d292d-123">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="d292d-124">Der zweite Befehl ruft den Lastenausgleich mit dem Namen "MyLB" ab und übergibt das Ergebnis an das **Add-AzLoadBalancerFrontendIpConfig-Cmdlet,** das dem Lastenausgleich eine Front-End-IP-Konfiguration mit der öffentlichen IP-Adresse hinzufügt, die in der Variablen namens $PublicIp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d292d-124">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

### <span data-ttu-id="d292d-125">Beispiel 4 Hinzufügen einer Front-End-IP-Konfiguration mit einem öffentlichen IP-Präfix</span><span class="sxs-lookup"><span data-stu-id="d292d-125">Example 4 Add a front-end IP configuration with a public IP prefix</span></span>
```
PS C:\> $PublicIpPrefix = Get-AzPublicIpPrefix -ResourceGroupName "myRG" -Name "MyPubPrefix"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddressPrefix $PublicIpPrefix | Set-AzLoadBalancer
```

<span data-ttu-id="d292d-126">Der erste Befehl ruft das öffentliche Azure-IP-Präfix "MyPubPrefix" ab und speichert das Ergebnis in der Variablen namens $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="d292d-126">The first command gets the Azure public IP prefix named MyPubPrefix and stores the result in the variable named $PublicIpPrefix.</span></span>
<span data-ttu-id="d292d-127">Der zweite Befehl ruft den Lastenausgleich namens "MyLB" ab und übergibt das Ergebnis an das **Add-AzLoadBalancerFrontendIpConfig-Cmdlet,** das dem Lastenausgleich eine Front-End-IP-Konfiguration mit dem öffentlichen IP-Präfix hinzufügt, das in der Variablen namens $PublicIpPrefix gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d292d-127">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP prefix stored in the variable named $PublicIpPrefix.</span></span>

## <span data-ttu-id="d292d-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d292d-128">PARAMETERS</span></span>

### <span data-ttu-id="d292d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d292d-129">-DefaultProfile</span></span>
<span data-ttu-id="d292d-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d292d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d292d-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d292d-131">-LoadBalancer</span></span>
<span data-ttu-id="d292d-132">Gibt ein **LoadBalancer-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="d292d-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="d292d-133">Dieses Cmdlet fügt dem von diesem Parameter angegebenen Lastenausgleich eine Front-End-IP-Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="d292d-133">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="d292d-134">-Name</span><span class="sxs-lookup"><span data-stu-id="d292d-134">-Name</span></span>
<span data-ttu-id="d292d-135">Gibt den Namen der hinzuzufügenden Front-End-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="d292d-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="d292d-136">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d292d-136">-PrivateIpAddress</span></span>
<span data-ttu-id="d292d-137">Gibt die private IP-Adresse an, die einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d292d-137">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="d292d-138">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="d292d-138">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="d292d-139">Die private IP-Adressversion der IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d292d-139">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="d292d-140">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d292d-140">-PublicIpAddress</span></span>
<span data-ttu-id="d292d-141">Gibt die öffentliche IP-Adresse an, die einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d292d-141">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="d292d-142">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d292d-142">-PublicIpAddressId</span></span>
<span data-ttu-id="d292d-143">Gibt die ID der öffentlichen IP-Adresse an, in der eine Front-End-IP-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d292d-143">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="d292d-144">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d292d-144">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="d292d-145">Gibt das Präfixobjekt für öffentliche IP-Adressen an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d292d-145">Specifies the public ip address prefix object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="d292d-146">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="d292d-146">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="d292d-147">Gibt die ID des Präfixobjekts für öffentliche IP-Adressen an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d292d-147">Specifies the ID of the public ip address prefix object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="d292d-148">-Subnet</span><span class="sxs-lookup"><span data-stu-id="d292d-148">-Subnet</span></span>
<span data-ttu-id="d292d-149">Gibt das Subnetzobjekt an, in dem eine Front-End-IP-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d292d-149">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="d292d-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d292d-150">-SubnetId</span></span>
<span data-ttu-id="d292d-151">Gibt die ID des Subnetzes an, in dem eine Front-End-IP-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d292d-151">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="d292d-152">-Zone</span><span class="sxs-lookup"><span data-stu-id="d292d-152">-Zone</span></span>
<span data-ttu-id="d292d-153">Eine Liste der Verfügbarkeitszonen, in der die für die Ressource zugeordnete IP aufgeführt wird, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="d292d-153">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="d292d-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d292d-154">-Confirm</span></span>
<span data-ttu-id="d292d-155">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d292d-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d292d-156">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d292d-156">-WhatIf</span></span>
<span data-ttu-id="d292d-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d292d-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d292d-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d292d-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d292d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d292d-159">CommonParameters</span></span>
<span data-ttu-id="d292d-160">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d292d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d292d-161">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d292d-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d292d-162">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d292d-162">INPUTS</span></span>

### <span data-ttu-id="d292d-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d292d-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="d292d-164">System.String</span><span class="sxs-lookup"><span data-stu-id="d292d-164">System.String</span></span>

### <span data-ttu-id="d292d-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d292d-165">System.String[]</span></span>

### <span data-ttu-id="d292d-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="d292d-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="d292d-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d292d-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="d292d-168">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d292d-168">OUTPUTS</span></span>

### <span data-ttu-id="d292d-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d292d-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d292d-170">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d292d-170">NOTES</span></span>

## <span data-ttu-id="d292d-171">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d292d-171">RELATED LINKS</span></span>

[<span data-ttu-id="d292d-172">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d292d-172">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d292d-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d292d-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="d292d-174">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d292d-174">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d292d-175">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d292d-175">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d292d-176">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d292d-176">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d292d-177">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d292d-177">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


