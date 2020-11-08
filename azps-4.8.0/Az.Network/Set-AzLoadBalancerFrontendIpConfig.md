---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b9f7767554efe6a91ea0989e4d37eec7c4832708
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009043"
---
# <span data-ttu-id="46c20-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46c20-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="46c20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46c20-102">SYNOPSIS</span></span>
<span data-ttu-id="46c20-103">Aktualisiert eine Front-End-IP-Konfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="46c20-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="46c20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46c20-104">SYNTAX</span></span>

### <span data-ttu-id="46c20-105">SetByResourceSubnet (Standard)</span><span class="sxs-lookup"><span data-stu-id="46c20-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46c20-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="46c20-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46c20-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="46c20-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46c20-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="46c20-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46c20-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46c20-109">DESCRIPTION</span></span>
<span data-ttu-id="46c20-110">Das Cmdlet " **Satz-AzLoadBalancerFrontendIpConfig** " aktualisiert eine Front-End-IP-Konfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="46c20-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="46c20-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46c20-111">EXAMPLES</span></span>

### <span data-ttu-id="46c20-112">Beispiel 1: Ändern der Front-End-IP-Konfiguration eines Load Balancer</span><span class="sxs-lookup"><span data-stu-id="46c20-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="46c20-113">Der erste Befehl ruft das virtuelle Subnetz mit dem Namen Subnet ab und speichert es dann in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="46c20-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="46c20-114">Der zweite Befehl ruft das zugeordnete Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="46c20-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="46c20-115">Der dritte Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzLoadBalancerFrontendIpConfig zu übergeben, wodurch eine Front-End-IP-Konfiguration mit dem Namen "neu Frontend für $SLB" erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="46c20-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="46c20-116">Der vierte Befehl übergibt das Load Balancer in $SLB an **AzLoadBalancerFrontendIpConfig** , wodurch die Front-End-IP-Konfiguration gespeichert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="46c20-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="46c20-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="46c20-117">PARAMETERS</span></span>

### <span data-ttu-id="46c20-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c20-118">-DefaultProfile</span></span>
<span data-ttu-id="46c20-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46c20-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46c20-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46c20-120">-LoadBalancer</span></span>
<span data-ttu-id="46c20-121">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="46c20-121">Specifies a load balancer.</span></span>
<span data-ttu-id="46c20-122">Dieses Cmdlet aktualisiert eine Front-End-Konfiguration für das Load Balancer, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="46c20-122">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="46c20-123">-Name</span><span class="sxs-lookup"><span data-stu-id="46c20-123">-Name</span></span>
<span data-ttu-id="46c20-124">Gibt den Namen der Front-End-IP-Konfiguration an, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="46c20-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="46c20-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="46c20-125">-PrivateIpAddress</span></span>
<span data-ttu-id="46c20-126">Gibt die private IP-Adresse des Load Balancer an, der der festzulegenden Front-End-IP-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="46c20-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="46c20-127">Geben Sie diesen Parameter nur an, wenn Sie auch den *Subnet* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="46c20-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="46c20-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="46c20-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="46c20-129">Die private IP-Adressenversion der IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="46c20-129">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="46c20-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="46c20-130">-PublicIpAddress</span></span>
<span data-ttu-id="46c20-131">Gibt das **PublicIpAddress** -Objekt an, das der festzulegenden Front-End-IP-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="46c20-131">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="46c20-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="46c20-132">-PublicIpAddressId</span></span>
<span data-ttu-id="46c20-133">Gibt die ID des **PublicIpAddress** -Objekts an, das der Front-End-IP-Konfiguration zugeordnet ist, die dieses Cmdlet festlegt.</span><span class="sxs-lookup"><span data-stu-id="46c20-133">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="46c20-134">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="46c20-134">-Subnet</span></span>
<span data-ttu-id="46c20-135">Gibt das **Subnet** -Objekt an, das die von diesem Cmdlet festgelegte Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="46c20-135">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="46c20-136">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="46c20-136">-SubnetId</span></span>
<span data-ttu-id="46c20-137">Gibt die ID des Subnets an, das die von diesem Cmdlet festgelegte Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="46c20-137">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="46c20-138">-Zone</span><span class="sxs-lookup"><span data-stu-id="46c20-138">-Zone</span></span>
<span data-ttu-id="46c20-139">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="46c20-139">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="46c20-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46c20-140">-Confirm</span></span>
<span data-ttu-id="46c20-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46c20-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46c20-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46c20-142">-WhatIf</span></span>
<span data-ttu-id="46c20-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46c20-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46c20-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46c20-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46c20-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c20-145">CommonParameters</span></span>
<span data-ttu-id="46c20-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46c20-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c20-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46c20-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c20-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46c20-148">INPUTS</span></span>

### <span data-ttu-id="46c20-149">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46c20-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="46c20-150">System. String</span><span class="sxs-lookup"><span data-stu-id="46c20-150">System.String</span></span>

### <span data-ttu-id="46c20-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="46c20-151">System.String[]</span></span>

### <span data-ttu-id="46c20-152">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="46c20-152">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="46c20-153">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="46c20-153">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="46c20-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46c20-154">OUTPUTS</span></span>

### <span data-ttu-id="46c20-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46c20-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="46c20-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="46c20-156">NOTES</span></span>

## <span data-ttu-id="46c20-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46c20-157">RELATED LINKS</span></span>

[<span data-ttu-id="46c20-158">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46c20-158">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="46c20-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46c20-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="46c20-160">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46c20-160">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="46c20-161">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46c20-161">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="46c20-162">Neu – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46c20-162">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="46c20-163">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46c20-163">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


