---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 7596dff276a4913dd1c322ad023ebfb32b8e1aac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300676"
---
# <span data-ttu-id="7d47b-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d47b-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="7d47b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d47b-102">SYNOPSIS</span></span>
<span data-ttu-id="7d47b-103">Fügt eine Front-End-IP-Konfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="7d47b-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="7d47b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d47b-104">SYNTAX</span></span>

### <span data-ttu-id="7d47b-105">SetByResourceSubnet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d47b-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d47b-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="7d47b-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d47b-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7d47b-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d47b-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7d47b-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d47b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d47b-109">DESCRIPTION</span></span>
<span data-ttu-id="7d47b-110">Mit dem Cmdlet **Add-AzLoadBalancerFrontendIpConfig** wird eine Front-End-IP-Konfiguration zu einem Azure Load Balancer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7d47b-110">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="7d47b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d47b-111">EXAMPLES</span></span>

### <span data-ttu-id="7d47b-112">Beispiel 1: Hinzufügen einer Front-End-IP-Konfiguration mit einer dynamischen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="7d47b-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="7d47b-113">Der erste Befehl ruft das Azure Virtual Network mit dem Namen MyVnet ab und übergibt das Ergebnis mithilfe der Pipeline an das Cmdlet **Get-AzVirtualNetworkSubnetConfig** , um das Subnetz mit dem Namen mysubnet abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7d47b-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="7d47b-114">Der Befehl speichert dann das Ergebnis in der Variablen mit dem Namen $Subnet.</span><span class="sxs-lookup"><span data-stu-id="7d47b-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="7d47b-115">Der zweite Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLB ab und übergibt das Ergebnis an das **Add-AzLoadBalancerFrontendIpConfig-** Cmdlet, das dem Load Balancer eine Front-End-IP-Konfiguration mit einer dynamischen privaten IP-Adresse aus dem Subnetz hinzufügt, das in der Variablen mit dem Namen $MySubnet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7d47b-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="7d47b-116">Beispiel 2 Hinzufügen einer Front-End-IP-Konfiguration mit einer statischen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="7d47b-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="7d47b-117">Der erste Befehl ruft das Azure Virtual Network mit dem Namen MyVnet ab und übergibt das Ergebnis mithilfe der Pipeline an das Cmdlet **Get-AzVirtualNetworkSubnetConfig** , um das Subnetz mit dem Namen mysubnet abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7d47b-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="7d47b-118">Der Befehl speichert dann das Ergebnis in der Variablen mit dem Namen $Subnet.</span><span class="sxs-lookup"><span data-stu-id="7d47b-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="7d47b-119">Der zweite Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLB ab und übergibt das Ergebnis an das **Add-AzLoadBalancerFrontendIpConfig-** Cmdlet, das dem Load Balancer eine Front-End-IP-Konfiguration mit einer statischen privaten IP-Adresse aus dem Subnetz hinzufügt, das in der Variablen mit dem Namen $Subnet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7d47b-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="7d47b-120">Beispiel 3 Hinzufügen einer Front-End-IP-Konfiguration mit einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="7d47b-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="7d47b-121">Der erste Befehl ruft die Azure Public IP-Adresse mit dem Namen mypub ab und speichert das Ergebnis in der Variablen mit dem Namen $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="7d47b-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="7d47b-122">Der zweite Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLB ab und übergibt das Ergebnis an das **Add-AzLoadBalancerFrontendIpConfig-** Cmdlet, das dem Lastenausgleichsmodul eine Front-End-IP-Konfiguration hinzufügt, wobei die öffentliche IP-Adresse in der Variablen mit dem Namen $PublicIp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7d47b-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="7d47b-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d47b-123">PARAMETERS</span></span>

### <span data-ttu-id="7d47b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d47b-124">-DefaultProfile</span></span>
<span data-ttu-id="7d47b-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d47b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d47b-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7d47b-126">-LoadBalancer</span></span>
<span data-ttu-id="7d47b-127">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7d47b-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="7d47b-128">Dieses Cmdlet fügt dem Load Balancer eine Front-End-IP-Konfiguration hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7d47b-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="7d47b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="7d47b-129">-Name</span></span>
<span data-ttu-id="7d47b-130">Gibt den Namen der Front-End-IP-Konfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d47b-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="7d47b-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7d47b-131">-PrivateIpAddress</span></span>
<span data-ttu-id="7d47b-132">Gibt die private IP-Adresse an, die einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d47b-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7d47b-133">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7d47b-133">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="7d47b-134">Die private IP-Adressenversion der IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7d47b-134">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="7d47b-135">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7d47b-135">-PublicIpAddress</span></span>
<span data-ttu-id="7d47b-136">Gibt die öffentliche IP-Adresse an, die einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d47b-136">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7d47b-137">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7d47b-137">-PublicIpAddressId</span></span>
<span data-ttu-id="7d47b-138">Gibt die ID der öffentlichen IP-Adresse an, in der eine Front-End-IP-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d47b-138">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7d47b-139">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="7d47b-139">-Subnet</span></span>
<span data-ttu-id="7d47b-140">Gibt das Subnet-Objekt an, in dem eine Front-End-IP-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d47b-140">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7d47b-141">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="7d47b-141">-SubnetId</span></span>
<span data-ttu-id="7d47b-142">Gibt die ID des Subnets an, in dem eine Front-End-IP-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d47b-142">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7d47b-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="7d47b-143">-Zone</span></span>
<span data-ttu-id="7d47b-144">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="7d47b-144">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="7d47b-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7d47b-145">-Confirm</span></span>
<span data-ttu-id="7d47b-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d47b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d47b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d47b-147">-WhatIf</span></span>
<span data-ttu-id="7d47b-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d47b-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d47b-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d47b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d47b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d47b-150">CommonParameters</span></span>
<span data-ttu-id="7d47b-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d47b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d47b-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d47b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d47b-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d47b-153">INPUTS</span></span>

### <span data-ttu-id="7d47b-154">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7d47b-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="7d47b-155">System. String</span><span class="sxs-lookup"><span data-stu-id="7d47b-155">System.String</span></span>

### <span data-ttu-id="7d47b-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="7d47b-156">System.String[]</span></span>

### <span data-ttu-id="7d47b-157">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="7d47b-157">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="7d47b-158">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7d47b-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7d47b-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d47b-159">OUTPUTS</span></span>

### <span data-ttu-id="7d47b-160">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7d47b-160">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7d47b-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d47b-161">NOTES</span></span>

## <span data-ttu-id="7d47b-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d47b-162">RELATED LINKS</span></span>

[<span data-ttu-id="7d47b-163">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d47b-163">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7d47b-164">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7d47b-164">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="7d47b-165">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7d47b-165">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7d47b-166">Neu – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d47b-166">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7d47b-167">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d47b-167">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7d47b-168">Satz-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d47b-168">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


