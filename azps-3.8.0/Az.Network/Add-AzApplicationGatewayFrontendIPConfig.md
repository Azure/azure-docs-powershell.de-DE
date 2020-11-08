---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 30238f9466e87ab732b1b2b6d30bba26bcd4c83a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004531"
---
# <span data-ttu-id="ec0d8-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ec0d8-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="ec0d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0d8-103">Fügt eine Front-End-IP-Konfiguration zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="ec0d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec0d8-104">SYNTAX</span></span>

### <span data-ttu-id="ec0d8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ec0d8-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec0d8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ec0d8-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec0d8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec0d8-107">DESCRIPTION</span></span>
<span data-ttu-id="ec0d8-108">Mit dem Cmdlet **Add-AzApplicationGatewayFrontendIPConfig** wird ein Front-End-IP-Konfiguration zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="ec0d8-109">Ein Anwendungsgateway unterstützt zwei Arten von Front-End-IP-Konfigurationen:</span><span class="sxs-lookup"><span data-stu-id="ec0d8-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="ec0d8-110">Öffentliche IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="ec0d8-110">Public IP addresses</span></span>
- <span data-ttu-id="ec0d8-111">Private IP-Adressen mithilfe von Internal Load-Balancing (ILB) ein Anwendungsgateway kann höchstens eine öffentliche IP-Adresse und eine private IP-Adresse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="ec0d8-112">Fügen Sie die öffentliche IP-Adresse und die private IP-Adresse als separate Front-End-IPS hinzu.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="ec0d8-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec0d8-113">EXAMPLES</span></span>

### <span data-ttu-id="ec0d8-114">Beispiel 1: Hinzufügen einer öffentlichen IP-Adresse als Front-End-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="ec0d8-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="ec0d8-115">Der erste Befehl erstellt ein öffentliches IP-Adressen Objekt und speichert es in der $PublicIp-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="ec0d8-116">Der zweite Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ec0d8-117">Der dritte Befehl fügt die Front-End-IP-Konfiguration mit dem Namen "FrontEndIp01" für das Gateway in $AppGw unter Verwendung der in $PublicIp gespeicherten Adresse hinzu.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="ec0d8-118">Beispiel 2: Hinzufügen einer statischen privaten IP als Front-End-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="ec0d8-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="ec0d8-119">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="ec0d8-120">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="ec0d8-121">Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ec0d8-122">Der vierte Befehl fügt eine Front-End-IP-Konfiguration mit dem Namen FrontendIP02 mit $Subnet aus dem zweiten Befehl und der privaten IP-Adresse 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="ec0d8-123">Beispiel 3: Hinzufügen einer dynamischen privaten IP als Front-End-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="ec0d8-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="ec0d8-124">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="ec0d8-125">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="ec0d8-126">Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ec0d8-127">Der vierte Befehl fügt eine Front-End-IP-Konfiguration mit dem Namen FrontendIP02 mithilfe von $Subnet aus dem zweiten Befehl hinzu.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="ec0d8-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec0d8-128">PARAMETERS</span></span>

### <span data-ttu-id="ec0d8-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec0d8-129">-ApplicationGateway</span></span>
<span data-ttu-id="ec0d8-130">Gibt das Anwendungsgateway an, dem dieses Cmdlet eine Front-End-IP-Konfiguration hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec0d8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec0d8-131">-DefaultProfile</span></span>
<span data-ttu-id="ec0d8-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec0d8-133">-Name</span><span class="sxs-lookup"><span data-stu-id="ec0d8-133">-Name</span></span>
<span data-ttu-id="ec0d8-134">Gibt den Namen der Front-End-IP-Konfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="ec0d8-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="ec0d8-135">-PrivateIPAddress</span></span>
<span data-ttu-id="ec0d8-136">Gibt die private IP-Adresse an, die als Front-End-IP für das Anwendungsgateway hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="ec0d8-137">Falls angegeben, wird diese IP-Adresse statisch vom Subnetz zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-137">If specified, this IP is statically allocated from the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec0d8-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="ec0d8-138">-PublicIPAddress</span></span>
<span data-ttu-id="ec0d8-139">Gibt die öffentliche IP-Adresse an, die von diesem Cmdlet als Front-End-IP-Adresse für das Anwendungsgateway hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-139">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec0d8-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="ec0d8-140">-PublicIPAddressId</span></span>
<span data-ttu-id="ec0d8-141">Gibt die ID der öffentlichen IP-Adresse an, die von diesem Cmdlet als Front-End-IP-Adresse für das Anwendungsgateway hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-141">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec0d8-142">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="ec0d8-142">-Subnet</span></span>
<span data-ttu-id="ec0d8-143">Gibt das Subnetz an, das dieses Cmdlet als Front-End-IP-Konfiguration hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-143">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="ec0d8-144">Wenn Sie diesen Parameter angeben, bedeutet dies, dass das Anwendungsgateway eine private IP-basierte Konfiguration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-144">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="ec0d8-145">Wenn der Parameter *PrivateIPAddress* angegeben wird, sollte er zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-145">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="ec0d8-146">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec0d8-147">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="ec0d8-147">-SubnetId</span></span>
<span data-ttu-id="ec0d8-148">Gibt die Subnetz-ID an, die dieses Cmdlet als Front-End-IP-Konfiguration hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-148">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="ec0d8-149">Das übergeben von Subnetz impliziert eine private IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-149">Passing subnet implies private IP.</span></span>
<span data-ttu-id="ec0d8-150">Wenn der Parameter *PrivateIPAddress* angegeben wird, sollte er zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-150">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="ec0d8-151">Andernfalls wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-151">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec0d8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0d8-152">CommonParameters</span></span>
<span data-ttu-id="ec0d8-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec0d8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec0d8-154">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec0d8-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0d8-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec0d8-155">INPUTS</span></span>

### <span data-ttu-id="ec0d8-156">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec0d8-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ec0d8-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec0d8-157">OUTPUTS</span></span>

### <span data-ttu-id="ec0d8-158">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec0d8-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ec0d8-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec0d8-159">NOTES</span></span>

## <span data-ttu-id="ec0d8-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec0d8-160">RELATED LINKS</span></span>

[<span data-ttu-id="ec0d8-161">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ec0d8-161">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ec0d8-162">Neu – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ec0d8-162">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ec0d8-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ec0d8-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ec0d8-164">Satz-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ec0d8-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


