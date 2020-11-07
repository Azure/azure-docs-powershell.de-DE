---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 9692f44ce5d0a819d0176e0b295571ca260a2a71
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843639"
---
# <span data-ttu-id="571f8-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="571f8-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="571f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="571f8-102">SYNOPSIS</span></span>
<span data-ttu-id="571f8-103">Legt den Zielstatus für eine Front-End-IP-Konfiguration in einem Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="571f8-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="571f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="571f8-104">SYNTAX</span></span>

### <span data-ttu-id="571f8-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="571f8-105">SetByResourceSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="571f8-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="571f8-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="571f8-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="571f8-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="571f8-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="571f8-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="571f8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="571f8-109">DESCRIPTION</span></span>
<span data-ttu-id="571f8-110">Das Cmdlet " **Set-AzLoadBalancerFrontendIpConfig** " legt den Zielstatus für eine Front-End-IP-Konfiguration in einem Azure Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="571f8-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="571f8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="571f8-111">EXAMPLES</span></span>

### <span data-ttu-id="571f8-112">Beispiel 1: Ändern der Front-End-IP-Konfiguration eines Load Balancer</span><span class="sxs-lookup"><span data-stu-id="571f8-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="571f8-113">Der erste Befehl ruft das virtuelle Subnetz mit dem Namen Subnet ab und speichert es dann in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="571f8-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="571f8-114">Der zweite Befehl ruft das zugeordnete Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="571f8-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="571f8-115">Der dritte Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzLoadBalancerFrontendIpConfig zu übergeben, wodurch eine Front-End-IP-Konfiguration mit dem Namen "neu Frontend für $SLB" erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="571f8-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="571f8-116">Der vierte Befehl übergibt das Load Balancer in $SLB an **AzLoadBalancerFrontendIpConfig** , wodurch die Front-End-IP-Konfiguration gespeichert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="571f8-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="571f8-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="571f8-117">PARAMETERS</span></span>

### <span data-ttu-id="571f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="571f8-118">-DefaultProfile</span></span>
<span data-ttu-id="571f8-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="571f8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="571f8-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="571f8-120">-LoadBalancer</span></span>
<span data-ttu-id="571f8-121">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="571f8-121">Specifies a load balancer.</span></span>
<span data-ttu-id="571f8-122">Mit diesem Cmdlet wird der Zielstatus für eine Front-End-Konfiguration für das Load Balancer festgelegt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="571f8-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="571f8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="571f8-123">-Name</span></span>
<span data-ttu-id="571f8-124">Gibt den Namen der Front-End-IP-Konfiguration an, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="571f8-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="571f8-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="571f8-125">-PrivateIpAddress</span></span>
<span data-ttu-id="571f8-126">Gibt die private IP-Adresse des Load Balancer an, der der festzulegenden Front-End-IP-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="571f8-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="571f8-127">Geben Sie diesen Parameter nur an, wenn Sie auch den *Subnet* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="571f8-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="571f8-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="571f8-128">-PublicIpAddress</span></span>
<span data-ttu-id="571f8-129">Gibt das **PublicIpAddress** -Objekt an, das der festzulegenden Front-End-IP-Konfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="571f8-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="571f8-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="571f8-130">-PublicIpAddressId</span></span>
<span data-ttu-id="571f8-131">Gibt die ID des **PublicIpAddress** -Objekts an, das der Front-End-IP-Konfiguration zugeordnet ist, die dieses Cmdlet festlegt.</span><span class="sxs-lookup"><span data-stu-id="571f8-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="571f8-132">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="571f8-132">-Subnet</span></span>
<span data-ttu-id="571f8-133">Gibt das **Subnet** -Objekt an, das die von diesem Cmdlet festgelegte Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="571f8-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="571f8-134">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="571f8-134">-SubnetId</span></span>
<span data-ttu-id="571f8-135">Gibt die ID des Subnets an, das die von diesem Cmdlet festgelegte Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="571f8-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="571f8-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="571f8-136">-Zone</span></span>
<span data-ttu-id="571f8-137">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="571f8-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="571f8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="571f8-138">CommonParameters</span></span>
<span data-ttu-id="571f8-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="571f8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="571f8-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="571f8-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="571f8-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="571f8-141">INPUTS</span></span>

### <span data-ttu-id="571f8-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="571f8-142">PSLoadBalancer</span></span>
<span data-ttu-id="571f8-143">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="571f8-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="571f8-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="571f8-144">OUTPUTS</span></span>

### <span data-ttu-id="571f8-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="571f8-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="571f8-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="571f8-146">NOTES</span></span>

## <span data-ttu-id="571f8-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="571f8-147">RELATED LINKS</span></span>

[<span data-ttu-id="571f8-148">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="571f8-148">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="571f8-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="571f8-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="571f8-150">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="571f8-150">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="571f8-151">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="571f8-151">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="571f8-152">Neu – AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="571f8-152">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="571f8-153">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="571f8-153">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


