---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 2dba7d00ea308225736de6714c90c74b0ce30837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660917"
---
# <span data-ttu-id="5199c-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5199c-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="5199c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5199c-102">SYNOPSIS</span></span>
<span data-ttu-id="5199c-103">Fügt eine Front-End-IP-Konfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="5199c-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="5199c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5199c-104">SYNTAX</span></span>

### <span data-ttu-id="5199c-105">SetByResourceSubnet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5199c-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5199c-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="5199c-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5199c-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5199c-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5199c-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5199c-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5199c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5199c-109">DESCRIPTION</span></span>
<span data-ttu-id="5199c-110">Mit dem Cmdlet **Add-AzLoadBalancerFrontendIpConifg** wird eine Front-End-IP-Konfiguration zu einem Azure Load Balancer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5199c-110">The **Add-AzLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="5199c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5199c-111">EXAMPLES</span></span>

### <span data-ttu-id="5199c-112">Beispiel 1: Hinzufügen einer Front-End-IP-Konfiguration mit einer dynamischen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5199c-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="5199c-113">Der erste Befehl ruft das Azure Virtual Network mit dem Namen MyVnet ab und übergibt das Ergebnis mithilfe der Pipeline an das Cmdlet **Get-AzVirtualNetworkSubnetConfig** , um das Subnetz mit dem Namen mysubnet abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5199c-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="5199c-114">Der Befehl speichert dann das Ergebnis in der Variablen mit dem Namen $Subnet.</span><span class="sxs-lookup"><span data-stu-id="5199c-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="5199c-115">Der zweite Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLB ab und übergibt das Ergebnis an das **Add-AzLoadBalancerFrontendIpConfig-** Cmdlet, das dem Load Balancer eine Front-End-IP-Konfiguration mit einer dynamischen privaten IP-Adresse aus dem Subnetz hinzufügt, das in der Variablen mit dem Namen $MySubnet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5199c-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="5199c-116">Beispiel 2 Hinzufügen einer Front-End-IP-Konfiguration mit einer statischen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5199c-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="5199c-117">Der erste Befehl ruft das Azure Virtual Network mit dem Namen MyVnet ab und übergibt das Ergebnis mithilfe der Pipeline an das Cmdlet **Get-AzVirtualNetworkSubnetConfig** , um das Subnetz mit dem Namen mysubnet abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5199c-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="5199c-118">Der Befehl speichert dann das Ergebnis in der Variablen mit dem Namen $Subnet.</span><span class="sxs-lookup"><span data-stu-id="5199c-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="5199c-119">Der zweite Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLB ab und übergibt das Ergebnis an das **Add-AzLoadBalancerFrontendIpConfig-** Cmdlet, das dem Load Balancer eine Front-End-IP-Konfiguration mit einer statischen privaten IP-Adresse aus dem Subnetz hinzufügt, das in der Variablen mit dem Namen $Subnet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5199c-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="5199c-120">Beispiel 3 Hinzufügen einer Front-End-IP-Konfiguration mit einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5199c-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="5199c-121">Der erste Befehl ruft die Azure Public IP-Adresse mit dem Namen mypub ab und speichert das Ergebnis in der Variablen mit dem Namen $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="5199c-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="5199c-122">Der zweite Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLB ab und übergibt das Ergebnis an das **Add-AzLoadBalancerFrontendIpConfig-** Cmdlet, das dem Lastenausgleichsmodul eine Front-End-IP-Konfiguration hinzufügt, wobei die öffentliche IP-Adresse in der Variablen mit dem Namen $PublicIp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5199c-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="5199c-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="5199c-123">PARAMETERS</span></span>

### <span data-ttu-id="5199c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5199c-124">-DefaultProfile</span></span>
<span data-ttu-id="5199c-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5199c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5199c-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5199c-126">-LoadBalancer</span></span>
<span data-ttu-id="5199c-127">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5199c-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="5199c-128">Dieses Cmdlet fügt dem Load Balancer eine Front-End-IP-Konfiguration hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5199c-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="5199c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="5199c-129">-Name</span></span>
<span data-ttu-id="5199c-130">Gibt den Namen der Front-End-IP-Konfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5199c-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="5199c-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="5199c-131">-PrivateIpAddress</span></span>
<span data-ttu-id="5199c-132">Gibt die private IP-Adresse an, die einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5199c-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="5199c-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5199c-133">-PublicIpAddress</span></span>
<span data-ttu-id="5199c-134">Gibt die öffentliche IP-Adresse an, die einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5199c-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="5199c-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="5199c-135">-PublicIpAddressId</span></span>
<span data-ttu-id="5199c-136">Gibt an die ID der öffentlichen IP-Adresse, in der eine Front-End-IP-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5199c-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="5199c-137">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="5199c-137">-Subnet</span></span>
<span data-ttu-id="5199c-138">Gibt das Subnet-Objekt an, in dem eine Front-End-IP-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5199c-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="5199c-139">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="5199c-139">-SubnetId</span></span>
<span data-ttu-id="5199c-140">Gibt die ID des Subnets an, in dem eine Front-End-IP-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5199c-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="5199c-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="5199c-141">-Zone</span></span>
<span data-ttu-id="5199c-142">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="5199c-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="5199c-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5199c-143">-Confirm</span></span>
<span data-ttu-id="5199c-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5199c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5199c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5199c-145">-WhatIf</span></span>
<span data-ttu-id="5199c-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5199c-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5199c-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5199c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5199c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5199c-148">CommonParameters</span></span>
<span data-ttu-id="5199c-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5199c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5199c-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5199c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5199c-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5199c-151">INPUTS</span></span>

### <span data-ttu-id="5199c-152">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5199c-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="5199c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="5199c-153">System.String</span></span>

### <span data-ttu-id="5199c-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="5199c-154">System.String[]</span></span>

### <span data-ttu-id="5199c-155">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5199c-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="5199c-156">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5199c-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="5199c-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5199c-157">OUTPUTS</span></span>

### <span data-ttu-id="5199c-158">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5199c-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5199c-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="5199c-159">NOTES</span></span>

## <span data-ttu-id="5199c-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5199c-160">RELATED LINKS</span></span>

[<span data-ttu-id="5199c-161">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5199c-161">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5199c-162">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5199c-162">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="5199c-163">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5199c-163">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5199c-164">Neu – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5199c-164">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5199c-165">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5199c-165">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5199c-166">Satz-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5199c-166">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


