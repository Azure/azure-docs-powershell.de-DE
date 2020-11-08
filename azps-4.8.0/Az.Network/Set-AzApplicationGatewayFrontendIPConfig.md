---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: b72b072307ee4d8ae304888e2d1b3db4a36be3aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173182"
---
# <span data-ttu-id="4fe97-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4fe97-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="4fe97-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4fe97-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe97-103">Ändert die Konfiguration einer Front-End-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="4fe97-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="4fe97-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fe97-104">SYNTAX</span></span>

### <span data-ttu-id="4fe97-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4fe97-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fe97-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4fe97-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fe97-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4fe97-107">DESCRIPTION</span></span>
<span data-ttu-id="4fe97-108">Das Cmdlet " **Satz-AzApplicationGatewayFrontendIPConfig** " aktualisiert eine Front-End-IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4fe97-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="4fe97-109">Ein Anwendungsgateway unterstützt zwei Arten von Front-End-IP-Adressen:</span><span class="sxs-lookup"><span data-stu-id="4fe97-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="4fe97-110">Öffentliche IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="4fe97-110">Public IP addresses</span></span>
- <span data-ttu-id="4fe97-111">Private IP-Adressen, für die die Konfiguration den internen Lastenausgleich (ILB) verwendet ein Anwendungsgateway kann höchstens eine öffentliche IP-Adresse und eine private IP-Adresse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4fe97-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="4fe97-112">Eine öffentliche IP-Adresse und eine private IP-Adresse sollten separat als Front-End-IP-Adressen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4fe97-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="4fe97-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4fe97-113">EXAMPLES</span></span>

### <span data-ttu-id="4fe97-114">Beispiel 1: Einrichten einer öffentlichen IP-Adresse als Front-End-IP eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="4fe97-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="4fe97-115">Der erste Befehl erstellt ein öffentliches IP-Adressen Objekt und speichert es in der $PublicIp-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4fe97-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="4fe97-116">Der zweite Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4fe97-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4fe97-117">Der dritte Befehl aktualisiert die Front-End-IP-Konfiguration mit dem Namen "FrontEndIp01" für das Gateway in $AppGw unter Verwendung der in $PublicIp gespeicherten Adresse.</span><span class="sxs-lookup"><span data-stu-id="4fe97-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="4fe97-118">Beispiel 2: Einrichten einer statischen privaten IP-Adresse als Front-End-IP eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="4fe97-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="4fe97-119">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4fe97-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="4fe97-120">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4fe97-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="4fe97-121">Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4fe97-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4fe97-122">Der vierte Befehl fügt eine Front-End-IP-Konfiguration mit dem Namen FrontendIP02 mit $Subnet aus dem zweiten Befehl und der privaten IP-Adresse 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="4fe97-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="4fe97-123">Beispiel 3: Einrichten einer dynamischen privaten IP-Adresse als Front-End-IP eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="4fe97-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="4fe97-124">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4fe97-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="4fe97-125">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4fe97-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="4fe97-126">Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4fe97-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4fe97-127">Der vierte Befehl fügt eine Front-End-IP-Konfiguration mit dem Namen FrontendIP02 mithilfe von $Subnet aus dem zweiten Befehl hinzu.</span><span class="sxs-lookup"><span data-stu-id="4fe97-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="4fe97-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fe97-128">PARAMETERS</span></span>

### <span data-ttu-id="4fe97-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fe97-129">-ApplicationGateway</span></span>
<span data-ttu-id="4fe97-130">Gibt ein Application Gateway-Objekt an, in dem die Front-End-IP-Konfiguration geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4fe97-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="4fe97-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe97-131">-DefaultProfile</span></span>
<span data-ttu-id="4fe97-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4fe97-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fe97-133">-Name</span><span class="sxs-lookup"><span data-stu-id="4fe97-133">-Name</span></span>
<span data-ttu-id="4fe97-134">Gibt den Namen der Front-End-IP-Konfiguration an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4fe97-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4fe97-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="4fe97-135">-PrivateIPAddress</span></span>
<span data-ttu-id="4fe97-136">Gibt die private IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="4fe97-136">Specifies the private IP address.</span></span>
<span data-ttu-id="4fe97-137">Falls angegeben, wird diese IP-Adresse statisch vom Subnetz zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="4fe97-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="4fe97-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fe97-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="4fe97-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fe97-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="4fe97-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4fe97-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="4fe97-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4fe97-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="4fe97-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="4fe97-142">-PublicIPAddress</span></span>
<span data-ttu-id="4fe97-143">Gibt die öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="4fe97-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="4fe97-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="4fe97-144">-PublicIPAddressId</span></span>
<span data-ttu-id="4fe97-145">Gibt die ID der öffentlichen IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="4fe97-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="4fe97-146">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="4fe97-146">-Subnet</span></span>
<span data-ttu-id="4fe97-147">Gibt das Subnetz an, das vom Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fe97-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="4fe97-148">Geben Sie diesen Parameter an, wenn das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="4fe97-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="4fe97-149">Wenn die *PrivateIPAddress* -Adresse angegeben wird, sollte Sie zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="4fe97-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="4fe97-150">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="4fe97-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="4fe97-151">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="4fe97-151">-SubnetId</span></span>
<span data-ttu-id="4fe97-152">Gibt die Subnet-ID an.</span><span class="sxs-lookup"><span data-stu-id="4fe97-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="4fe97-153">Geben Sie diesen Parameter an, wenn das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="4fe97-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="4fe97-154">Wenn der Parameter *PrivateIPAddress* angegeben wird, sollte er zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="4fe97-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="4fe97-155">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="4fe97-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="4fe97-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe97-156">CommonParameters</span></span>
<span data-ttu-id="4fe97-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fe97-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe97-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fe97-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe97-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4fe97-159">INPUTS</span></span>

### <span data-ttu-id="4fe97-160">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fe97-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4fe97-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4fe97-161">OUTPUTS</span></span>

### <span data-ttu-id="4fe97-162">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fe97-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4fe97-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="4fe97-163">NOTES</span></span>

## <span data-ttu-id="4fe97-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4fe97-164">RELATED LINKS</span></span>

[<span data-ttu-id="4fe97-165">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4fe97-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4fe97-166">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4fe97-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4fe97-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4fe97-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4fe97-168">Neu – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4fe97-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4fe97-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4fe97-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


