---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: e85976f77ece9af89ecd532ff0a3236039abb9fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843692"
---
# <span data-ttu-id="a5547-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a5547-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="a5547-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5547-102">SYNOPSIS</span></span>
<span data-ttu-id="a5547-103">Ändert die Konfiguration einer Front-End-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="a5547-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="a5547-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5547-104">SYNTAX</span></span>

### <span data-ttu-id="a5547-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5547-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5547-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a5547-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5547-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5547-107">DESCRIPTION</span></span>
<span data-ttu-id="a5547-108">Das Cmdlet " **Satz-AzApplicationGatewayFrontendIPConfig** " aktualisiert eine Front-End-IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a5547-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>

<span data-ttu-id="a5547-109">Ein Anwendungsgateway unterstützt zwei Arten von Front-End-IP-Adressen:</span><span class="sxs-lookup"><span data-stu-id="a5547-109">An application gateway supports two types of front-end IP addresses:</span></span> 

- <span data-ttu-id="a5547-110">Öffentliche IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="a5547-110">Public IP addresses</span></span>
- <span data-ttu-id="a5547-111">Private IP-Adressen, für die die Konfiguration den internen Lastenausgleich verwendet (ILB)</span><span class="sxs-lookup"><span data-stu-id="a5547-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB)</span></span>

<span data-ttu-id="a5547-112">Ein Anwendungsgateway kann höchstens eine öffentliche IP-Adresse und eine private IP-Adresse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a5547-112">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="a5547-113">Eine öffentliche IP-Adresse und eine private IP-Adresse sollten separat als Front-End-IP-Adressen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a5547-113">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="a5547-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5547-114">EXAMPLES</span></span>

### <span data-ttu-id="a5547-115">Beispiel 1: Einrichten einer öffentlichen IP-Adresse als Front-End-IP eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="a5547-115">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="a5547-116">Der erste Befehl erstellt ein öffentliches IP-Adressen Objekt und speichert es in der $PublicIp-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5547-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>

<span data-ttu-id="a5547-117">Der zweite Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5547-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a5547-118">Der dritte Befehl aktualisiert die Front-End-IP-Konfiguration mit dem Namen "FrontEndIp01" für das Gateway in $AppGw unter Verwendung der in $PublicIp gespeicherten Adresse.</span><span class="sxs-lookup"><span data-stu-id="a5547-118">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="a5547-119">Beispiel 2: Einrichten einer statischen privaten IP-Adresse als Front-End-IP eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="a5547-119">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="a5547-120">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5547-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="a5547-121">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5547-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="a5547-122">Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5547-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a5547-123">Der vierte Befehl fügt eine Front-End-IP-Konfiguration mit dem Namen FrontendIP02 mit $Subnet aus dem zweiten Befehl und der privaten IP-Adresse 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="a5547-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="a5547-124">Beispiel 3: Einrichten einer dynamischen privaten IP-Adresse als Front-End-IP eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="a5547-124">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="a5547-125">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5547-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="a5547-126">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5547-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="a5547-127">Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5547-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a5547-128">Der vierte Befehl fügt eine Front-End-IP-Konfiguration mit dem Namen FrontendIP02 mithilfe von $Subnet aus dem zweiten Befehl hinzu.</span><span class="sxs-lookup"><span data-stu-id="a5547-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="a5547-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5547-129">PARAMETERS</span></span>

### <span data-ttu-id="a5547-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5547-130">-ApplicationGateway</span></span>
<span data-ttu-id="a5547-131">Gibt ein Application Gateway-Objekt an, in dem die Front-End-IP-Konfiguration geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5547-131">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="a5547-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5547-132">-DefaultProfile</span></span>
<span data-ttu-id="a5547-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5547-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5547-134">-Name</span><span class="sxs-lookup"><span data-stu-id="a5547-134">-Name</span></span>
<span data-ttu-id="a5547-135">Gibt den Namen der Front-End-IP-Konfiguration an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a5547-135">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a5547-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="a5547-136">-PrivateIPAddress</span></span>
<span data-ttu-id="a5547-137">Gibt die private IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="a5547-137">Specifies the private IP address.</span></span>
<span data-ttu-id="a5547-138">Falls angegeben, wird diese IP-Adresse statisch vom Subnetz zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a5547-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="a5547-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="a5547-139">-PublicIPAddress</span></span>
<span data-ttu-id="a5547-140">Gibt die öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="a5547-140">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="a5547-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="a5547-141">-PublicIPAddressId</span></span>
<span data-ttu-id="a5547-142">Gibt die ID der öffentlichen IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="a5547-142">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="a5547-143">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="a5547-143">-Subnet</span></span>
<span data-ttu-id="a5547-144">Gibt das Subnetz an, das vom Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a5547-144">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="a5547-145">Geben Sie diesen Parameter an, wenn das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5547-145">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="a5547-146">Wenn die *PrivateIPAddress* -Adresse angegeben wird, sollte Sie zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="a5547-146">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="a5547-147">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="a5547-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="a5547-148">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="a5547-148">-SubnetId</span></span>
<span data-ttu-id="a5547-149">Gibt die Subnet-ID an.</span><span class="sxs-lookup"><span data-stu-id="a5547-149">Specifies the subnet ID.</span></span>
<span data-ttu-id="a5547-150">Geben Sie diesen Parameter an, wenn das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5547-150">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="a5547-151">Wenn der Parameter *PrivateIPAddress* angegeben wird, sollte er zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="a5547-151">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="a5547-152">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="a5547-152">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="a5547-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5547-153">CommonParameters</span></span>
<span data-ttu-id="a5547-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5547-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5547-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5547-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5547-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5547-156">INPUTS</span></span>

### <span data-ttu-id="a5547-157">System. String</span><span class="sxs-lookup"><span data-stu-id="a5547-157">System.String</span></span>

## <span data-ttu-id="a5547-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5547-158">OUTPUTS</span></span>

### <span data-ttu-id="a5547-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5547-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a5547-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5547-160">NOTES</span></span>

## <span data-ttu-id="a5547-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5547-161">RELATED LINKS</span></span>

[<span data-ttu-id="a5547-162">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a5547-162">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a5547-163">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a5547-163">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a5547-164">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a5547-164">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a5547-165">Neu – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a5547-165">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a5547-166">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a5547-166">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


