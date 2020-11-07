---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: f54527b167fa15ea4c4e878b81d86a00079e28a0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850808"
---
# <span data-ttu-id="a9bdd-101">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a9bdd-101">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="a9bdd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="a9bdd-103">Fügt eine Front-End-IP-Konfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-103">Adds a front-end IP configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9bdd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9bdd-104">SYNTAX</span></span>

### <span data-ttu-id="a9bdd-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="a9bdd-105">SetByResourceSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9bdd-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="a9bdd-106">SetByResourceIdSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9bdd-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a9bdd-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9bdd-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a9bdd-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9bdd-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9bdd-109">DESCRIPTION</span></span>
<span data-ttu-id="a9bdd-110">Mit dem Cmdlet **Add-AzureRmLoadBalancerFrontendIpConifg** wird eine Front-End-IP-Konfiguration zu einem Azure Load Balancer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-110">The **Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="a9bdd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9bdd-111">EXAMPLES</span></span>

### <span data-ttu-id="a9bdd-112">Beispiel 1: Hinzufügen einer Front-End-IP-Konfiguration mit einer dynamischen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="a9bdd-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

<span data-ttu-id="a9bdd-113">Der erste Befehl ruft das Azure Virtual Network mit dem Namen MyVnet ab und übergibt das Ergebnis mithilfe der Pipeline an das Cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** , um das Subnetz mit dem Namen mysubnet abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="a9bdd-114">Der Befehl speichert dann das Ergebnis in der Variablen mit dem Namen $Subnet.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="a9bdd-115">Der zweite Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLB ab und übergibt das Ergebnis an das **Add-AzureRmLoadBalancerFrontendIpConfig-** Cmdlet, das dem Load Balancer eine Front-End-IP-Konfiguration mit einer dynamischen privaten IP-Adresse aus dem Subnetz hinzufügt, das in der Variablen mit dem Namen $MySubnet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="a9bdd-116">Beispiel 2 Hinzufügen einer Front-End-IP-Konfiguration mit einer statischen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="a9bdd-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="a9bdd-117">Der erste Befehl ruft das Azure Virtual Network mit dem Namen MyVnet ab und übergibt das Ergebnis mithilfe der Pipeline an das Cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** , um das Subnetz mit dem Namen mysubnet abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="a9bdd-118">Der Befehl speichert dann das Ergebnis in der Variablen mit dem Namen $Subnet.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="a9bdd-119">Der zweite Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLB ab und übergibt das Ergebnis an das **Add-AzureRmLoadBalancerFrontendIpConfig-** Cmdlet, das dem Load Balancer eine Front-End-IP-Konfiguration mit einer statischen privaten IP-Adresse aus dem Subnetz hinzufügt, das in der Variablen mit dem Namen $Subnet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="a9bdd-120">Beispiel 3 Hinzufügen einer Front-End-IP-Konfiguration mit einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="a9bdd-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

<span data-ttu-id="a9bdd-121">Der erste Befehl ruft die Azure Public IP-Adresse mit dem Namen mypub ab und speichert das Ergebnis in der Variablen mit dem Namen $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="a9bdd-122">Der zweite Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLB ab und übergibt das Ergebnis an das **Add-AzureRmLoadBalancerFrontendIpConfig-** Cmdlet, das dem Lastenausgleichsmodul eine Front-End-IP-Konfiguration hinzufügt, wobei die öffentliche IP-Adresse in der Variablen mit dem Namen $PublicIp gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="a9bdd-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9bdd-123">PARAMETERS</span></span>

### <span data-ttu-id="a9bdd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9bdd-124">-DefaultProfile</span></span>
<span data-ttu-id="a9bdd-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bdd-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9bdd-126">-LoadBalancer</span></span>
<span data-ttu-id="a9bdd-127">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="a9bdd-128">Dieses Cmdlet fügt dem Load Balancer eine Front-End-IP-Konfiguration hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9bdd-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a9bdd-129">-Name</span></span>
<span data-ttu-id="a9bdd-130">Gibt den Namen der Front-End-IP-Konfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-130">Specifies the name of the front-end IP configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bdd-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a9bdd-131">-PrivateIpAddress</span></span>
<span data-ttu-id="a9bdd-132">Gibt die private IP-Adresse an, die einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bdd-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a9bdd-133">-PublicIpAddress</span></span>
<span data-ttu-id="a9bdd-134">Gibt die öffentliche IP-Adresse an, die einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bdd-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="a9bdd-135">-PublicIpAddressId</span></span>
<span data-ttu-id="a9bdd-136">Gibt an die ID der öffentlichen IP-Adresse, in der eine Front-End-IP-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bdd-137">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="a9bdd-137">-Subnet</span></span>
<span data-ttu-id="a9bdd-138">Gibt das Subnet-Objekt an, in dem eine Front-End-IP-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bdd-139">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="a9bdd-139">-SubnetId</span></span>
<span data-ttu-id="a9bdd-140">Gibt die ID des Subnets an, in dem eine Front-End-IP-Konfiguration hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bdd-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="a9bdd-141">-Zone</span></span>
<span data-ttu-id="a9bdd-142">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9bdd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9bdd-143">CommonParameters</span></span>
<span data-ttu-id="a9bdd-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9bdd-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9bdd-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9bdd-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9bdd-146">INPUTS</span></span>

### <span data-ttu-id="a9bdd-147">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9bdd-147">PSLoadBalancer</span></span>
<span data-ttu-id="a9bdd-148">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9bdd-148">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a9bdd-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9bdd-149">OUTPUTS</span></span>

### <span data-ttu-id="a9bdd-150">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9bdd-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a9bdd-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9bdd-151">NOTES</span></span>

## <span data-ttu-id="a9bdd-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9bdd-152">RELATED LINKS</span></span>

[<span data-ttu-id="a9bdd-153">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a9bdd-153">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a9bdd-154">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a9bdd-154">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="a9bdd-155">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a9bdd-155">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a9bdd-156">Neu – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a9bdd-156">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a9bdd-157">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a9bdd-157">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a9bdd-158">Satz-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a9bdd-158">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


