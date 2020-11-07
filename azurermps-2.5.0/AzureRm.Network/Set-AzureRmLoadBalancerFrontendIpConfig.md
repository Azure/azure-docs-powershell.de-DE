---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 8de9d162ceba8dc436d5244f75011b79a949ddeb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850331"
---
# <span data-ttu-id="a5a82-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5a82-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="a5a82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5a82-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a82-103">Legt den Zielstatus für eine Front-End-IP-Konfiguration in einem Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="a5a82-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5a82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5a82-104">SYNTAX</span></span>

### <span data-ttu-id="a5a82-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="a5a82-105">SetByResourceSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5a82-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="a5a82-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5a82-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5a82-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5a82-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5a82-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5a82-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5a82-109">DESCRIPTION</span></span>
<span data-ttu-id="a5a82-110">Das Cmdlet " **Set-AzureRmLoadBalancerFrontendIpConfig** " legt den Zielstatus für eine Front-End-IP-Konfiguration in einem Azure Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="a5a82-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="a5a82-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5a82-111">EXAMPLES</span></span>

### <span data-ttu-id="a5a82-112">Beispiel 1: Ändern der Front-End-IP-Konfiguration eines Load Balancer</span><span class="sxs-lookup"><span data-stu-id="a5a82-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="a5a82-113">Der erste Befehl ruft das virtuelle Subnetz mit dem Namen Subnet ab und speichert es dann in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5a82-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="a5a82-114">Der zweite Befehl ruft das zugeordnete Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5a82-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="a5a82-115">Der dritte Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzureRmLoadBalancerFrontendIpConfig zu übergeben, wodurch eine Front-End-IP-Konfiguration mit dem Namen "neu Frontend für $SLB" erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a5a82-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="a5a82-116">Der vierte Befehl übergibt das Load Balancer in $SLB an **AzureRmLoadBalancerFrontendIpConfig** , wodurch die Front-End-IP-Konfiguration gespeichert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a5a82-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="a5a82-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5a82-117">PARAMETERS</span></span>

### <span data-ttu-id="a5a82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a82-118">-DefaultProfile</span></span>
<span data-ttu-id="a5a82-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5a82-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5a82-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5a82-120">-LoadBalancer</span></span>
<span data-ttu-id="a5a82-121">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="a5a82-121">Specifies a load balancer.</span></span>
<span data-ttu-id="a5a82-122">Mit diesem Cmdlet wird der Zielstatus für eine Front-End-Konfiguration für das Load Balancer festgelegt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a5a82-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a5a82-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a5a82-123">-Name</span></span>
<span data-ttu-id="a5a82-124">Gibt den Namen der Front-End-IP-Konfiguration an, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5a82-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="a5a82-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5a82-125">-PrivateIpAddress</span></span>
<span data-ttu-id="a5a82-126">Gibt die private IP-Adresse des Load Balancer an, der der festzulegenden Front-End-IP-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a5a82-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="a5a82-127">Geben Sie diesen Parameter nur an, wenn Sie auch den *Subnet* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="a5a82-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="a5a82-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5a82-128">-PublicIpAddress</span></span>
<span data-ttu-id="a5a82-129">Gibt das **PublicIpAddress** -Objekt an, das der festzulegenden Front-End-IP-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a5a82-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="a5a82-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="a5a82-130">-PublicIpAddressId</span></span>
<span data-ttu-id="a5a82-131">Gibt die ID des **PublicIpAddress** -Objekts an, das der Front-End-IP-Konfiguration zugeordnet ist, die dieses Cmdlet festlegt.</span><span class="sxs-lookup"><span data-stu-id="a5a82-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="a5a82-132">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="a5a82-132">-Subnet</span></span>
<span data-ttu-id="a5a82-133">Gibt das **Subnet** -Objekt an, das die von diesem Cmdlet festgelegte Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="a5a82-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="a5a82-134">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="a5a82-134">-SubnetId</span></span>
<span data-ttu-id="a5a82-135">Gibt die ID des Subnets an, das die von diesem Cmdlet festgelegte Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="a5a82-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="a5a82-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="a5a82-136">-Zone</span></span>
<span data-ttu-id="a5a82-137">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="a5a82-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="a5a82-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a82-138">CommonParameters</span></span>
<span data-ttu-id="a5a82-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a82-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a82-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a82-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a82-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5a82-141">INPUTS</span></span>

### <span data-ttu-id="a5a82-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5a82-142">PSLoadBalancer</span></span>
<span data-ttu-id="a5a82-143">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5a82-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a5a82-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5a82-144">OUTPUTS</span></span>

### <span data-ttu-id="a5a82-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5a82-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a5a82-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5a82-146">NOTES</span></span>

## <span data-ttu-id="a5a82-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5a82-147">RELATED LINKS</span></span>

[<span data-ttu-id="a5a82-148">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5a82-148">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a5a82-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5a82-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a5a82-150">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5a82-150">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a5a82-151">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a5a82-151">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="a5a82-152">Neu – AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5a82-152">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a5a82-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5a82-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


