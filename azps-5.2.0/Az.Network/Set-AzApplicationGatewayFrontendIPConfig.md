---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: b72b072307ee4d8ae304888e2d1b3db4a36be3aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292102"
---
# <span data-ttu-id="66011-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="66011-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="66011-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66011-102">SYNOPSIS</span></span>
<span data-ttu-id="66011-103">Ändert eine Front-End-IP-Adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="66011-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="66011-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66011-104">SYNTAX</span></span>

### <span data-ttu-id="66011-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="66011-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66011-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="66011-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66011-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66011-107">DESCRIPTION</span></span>
<span data-ttu-id="66011-108">Das **Cmdlet Set-AzApplicationGatewayFrontendIPConfig** aktualisiert eine Front-End-IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="66011-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="66011-109">Ein Anwendungsgateway unterstützt zwei Typen von Front-End-IP-Adressen:</span><span class="sxs-lookup"><span data-stu-id="66011-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="66011-110">Öffentliche IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="66011-110">Public IP addresses</span></span>
- <span data-ttu-id="66011-111">Private IP-Adressen, für die in der Konfiguration der interne Lastenausgleich (Internal Load Balancing, ILB) verwendet wird. Ein Anwendungsgateway kann mindestens eine öffentliche und eine private IP-Adresse haben.</span><span class="sxs-lookup"><span data-stu-id="66011-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="66011-112">Eine öffentliche und eine private IP-Adresse sollten separat als Front-End-IP-Adressen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="66011-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="66011-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66011-113">EXAMPLES</span></span>

### <span data-ttu-id="66011-114">Beispiel 1: Festlegen einer öffentlichen IP als Front-End-IP eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="66011-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="66011-115">Der erste Befehl erstellt ein öffentliches IP-Adressobjekt und speichert es in der $PublicIp Variable.</span><span class="sxs-lookup"><span data-stu-id="66011-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="66011-116">Der zweite Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="66011-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="66011-117">Mit dem dritten Befehl wird die Front-End-IP-Konfiguration namens "FrontEndIp01" für das Gateway in $AppGw unter Verwendung der in der Datei gespeicherten $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="66011-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="66011-118">Beispiel 2: Festlegen einer statischen privaten IP als Front-End-IP eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="66011-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="66011-119">Der erste Befehl ruft ein virtuelles Netzwerk namens VNet01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $VNet Variable.</span><span class="sxs-lookup"><span data-stu-id="66011-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="66011-120">Der zweite Befehl ruft eine Subnetzkonfiguration namens Subnetz01 mit $VNet des ersten Befehls ab und speichert ihn in der $Subnet Variable.</span><span class="sxs-lookup"><span data-stu-id="66011-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="66011-121">Der dritte Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="66011-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="66011-122">Der vierte Befehl fügt eine Front-End-IP-Konfiguration namens FrontendIP02 mit $Subnet des zweiten Befehls und der privaten IP-Adresse 10.0.1.1 hinzu.</span><span class="sxs-lookup"><span data-stu-id="66011-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="66011-123">Beispiel 3: Festlegen einer dynamischen privaten IP als Front-End-IP eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="66011-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="66011-124">Der erste Befehl ruft ein virtuelles Netzwerk namens VNet01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $VNet Variable.</span><span class="sxs-lookup"><span data-stu-id="66011-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="66011-125">Der zweite Befehl ruft eine Subnetzkonfiguration namens Subnetz01 mit $VNet des ersten Befehls ab und speichert ihn in der $Subnet Variable.</span><span class="sxs-lookup"><span data-stu-id="66011-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="66011-126">Der dritte Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="66011-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="66011-127">Der vierte Befehl fügt eine Front-End-IP-Konfiguration namens FrontendIP02 mit $Subnet des zweiten Befehls hinzu.</span><span class="sxs-lookup"><span data-stu-id="66011-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="66011-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66011-128">PARAMETERS</span></span>

### <span data-ttu-id="66011-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66011-129">-ApplicationGateway</span></span>
<span data-ttu-id="66011-130">Gibt ein Anwendungsgatewayobjekt an, in dem die Front-End-IP-Konfiguration geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="66011-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66011-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66011-131">-DefaultProfile</span></span>
<span data-ttu-id="66011-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66011-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66011-133">-Name</span><span class="sxs-lookup"><span data-stu-id="66011-133">-Name</span></span>
<span data-ttu-id="66011-134">Gibt den Namen der Front-End-IP-Konfiguration an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="66011-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="66011-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="66011-135">-PrivateIPAddress</span></span>
<span data-ttu-id="66011-136">Gibt die private IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="66011-136">Specifies the private IP address.</span></span>
<span data-ttu-id="66011-137">Falls angegeben, wird diese IP statisch aus dem Subnetz zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="66011-137">If specified, this IP is statically allocated from the subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66011-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="66011-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="66011-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="66011-139">PrivateLinkConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66011-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="66011-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="66011-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="66011-141">PrivateLinkConfigurationId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66011-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="66011-142">-PublicIPAddress</span></span>
<span data-ttu-id="66011-143">Gibt die öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="66011-143">Specifies the public IP address.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66011-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="66011-144">-PublicIPAddressId</span></span>
<span data-ttu-id="66011-145">Gibt die ID der öffentlichen IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="66011-145">Specifies the ID of the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66011-146">-Subnet</span><span class="sxs-lookup"><span data-stu-id="66011-146">-Subnet</span></span>
<span data-ttu-id="66011-147">Gibt das subnetz an, das vom Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66011-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="66011-148">Geben Sie diesen Parameter an, wenn das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="66011-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="66011-149">Wenn die *Adresse "PrivateIPAddress"* angegeben ist, sollte sie zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="66011-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="66011-150">Wenn *"PrivateIPAddress"* nicht angegeben wird, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungsgateways aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="66011-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66011-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="66011-151">-SubnetId</span></span>
<span data-ttu-id="66011-152">Gibt die Subnetz-ID an.</span><span class="sxs-lookup"><span data-stu-id="66011-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="66011-153">Geben Sie diesen Parameter an, wenn das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="66011-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="66011-154">Wenn der *Parameter "PrivateIPAddress"* angegeben wird, sollte er zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="66011-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="66011-155">Wenn *"PrivateIPAddress"* nicht angegeben wird, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungsgateways aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="66011-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66011-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66011-156">CommonParameters</span></span>
<span data-ttu-id="66011-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66011-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66011-158">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66011-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66011-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66011-159">INPUTS</span></span>

### <span data-ttu-id="66011-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66011-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="66011-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66011-161">OUTPUTS</span></span>

### <span data-ttu-id="66011-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66011-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="66011-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="66011-163">NOTES</span></span>

## <span data-ttu-id="66011-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="66011-164">RELATED LINKS</span></span>

[<span data-ttu-id="66011-165">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="66011-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="66011-166">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="66011-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="66011-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="66011-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="66011-168">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="66011-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="66011-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="66011-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


