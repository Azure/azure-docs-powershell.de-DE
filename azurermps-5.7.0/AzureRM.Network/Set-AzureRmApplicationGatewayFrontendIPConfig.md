---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 38a74e6f11516b3a873709dfec118ffd2a1ad6ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503709"
---
# <span data-ttu-id="294d2-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="294d2-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="294d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="294d2-102">SYNOPSIS</span></span>
<span data-ttu-id="294d2-103">Ändert die Konfiguration einer Front-End-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="294d2-103">Modifies a front-end IP address configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="294d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="294d2-104">SYNTAX</span></span>

### <span data-ttu-id="294d2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="294d2-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="294d2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="294d2-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="294d2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="294d2-107">DESCRIPTION</span></span>
<span data-ttu-id="294d2-108">Das Cmdlet " **Satz-AzureRmApplicationGatewayFrontendIPConfig** " aktualisiert eine Front-End-IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="294d2-108">The **Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>

<span data-ttu-id="294d2-109">Ein Anwendungsgateway unterstützt zwei Arten von Front-End-IP-Adressen:</span><span class="sxs-lookup"><span data-stu-id="294d2-109">An application gateway supports two types of front-end IP addresses:</span></span> 

- <span data-ttu-id="294d2-110">Öffentliche IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="294d2-110">Public IP addresses</span></span>
- <span data-ttu-id="294d2-111">Private IP-Adressen, für die die Konfiguration den internen Lastenausgleich verwendet (ILB)</span><span class="sxs-lookup"><span data-stu-id="294d2-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB)</span></span>

<span data-ttu-id="294d2-112">Ein Anwendungsgateway kann höchstens eine öffentliche IP-Adresse und eine private IP-Adresse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="294d2-112">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="294d2-113">Eine öffentliche IP-Adresse und eine private IP-Adresse sollten separat als Front-End-IP-Adressen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="294d2-113">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="294d2-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="294d2-114">EXAMPLES</span></span>

### <span data-ttu-id="294d2-115">Beispiel 1: Einrichten einer öffentlichen IP-Adresse als Front-End-IP eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="294d2-115">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="294d2-116">Der erste Befehl erstellt ein öffentliches IP-Adressen Objekt und speichert es in der $PublicIp-Variablen.</span><span class="sxs-lookup"><span data-stu-id="294d2-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>

<span data-ttu-id="294d2-117">Der zweite Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="294d2-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="294d2-118">Der dritte Befehl aktualisiert die Front-End-IP-Konfiguration mit dem Namen "FrontEndIp01" für das Gateway in $AppGw unter Verwendung der in $PublicIp gespeicherten Adresse.</span><span class="sxs-lookup"><span data-stu-id="294d2-118">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="294d2-119">Beispiel 2: Einrichten einer statischen privaten IP-Adresse als Front-End-IP eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="294d2-119">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="294d2-120">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="294d2-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="294d2-121">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="294d2-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="294d2-122">Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="294d2-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="294d2-123">Der vierte Befehl fügt eine Front-End-IP-Konfiguration mit dem Namen FrontendIP02 mit $Subnet aus dem zweiten Befehl und der privaten IP-Adresse 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="294d2-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="294d2-124">Beispiel 3: Einrichten einer dynamischen privaten IP-Adresse als Front-End-IP eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="294d2-124">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="294d2-125">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="294d2-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="294d2-126">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="294d2-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="294d2-127">Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="294d2-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="294d2-128">Der vierte Befehl fügt eine Front-End-IP-Konfiguration mit dem Namen FrontendIP02 mithilfe von $Subnet aus dem zweiten Befehl hinzu.</span><span class="sxs-lookup"><span data-stu-id="294d2-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="294d2-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="294d2-129">PARAMETERS</span></span>

### <span data-ttu-id="294d2-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="294d2-130">-ApplicationGateway</span></span>
<span data-ttu-id="294d2-131">Gibt ein Application Gateway-Objekt an, in dem die Front-End-IP-Konfiguration geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="294d2-131">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="294d2-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="294d2-132">-DefaultProfile</span></span>
<span data-ttu-id="294d2-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="294d2-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="294d2-134">-Name</span><span class="sxs-lookup"><span data-stu-id="294d2-134">-Name</span></span>
<span data-ttu-id="294d2-135">Gibt den Namen der Front-End-IP-Konfiguration an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="294d2-135">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="294d2-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="294d2-136">-PrivateIPAddress</span></span>
<span data-ttu-id="294d2-137">Gibt die private IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="294d2-137">Specifies the private IP address.</span></span>
<span data-ttu-id="294d2-138">Falls angegeben, wird diese IP-Adresse statisch vom Subnetz zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="294d2-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="294d2-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="294d2-139">-PublicIPAddress</span></span>
<span data-ttu-id="294d2-140">Gibt die öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="294d2-140">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="294d2-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="294d2-141">-PublicIPAddressId</span></span>
<span data-ttu-id="294d2-142">Gibt die ID der öffentlichen IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="294d2-142">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="294d2-143">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="294d2-143">-Subnet</span></span>
<span data-ttu-id="294d2-144">Gibt das Subnetz an, das vom Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="294d2-144">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="294d2-145">Geben Sie diesen Parameter an, wenn das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="294d2-145">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="294d2-146">Wenn die *PrivateIPAddress* -Adresse angegeben wird, sollte Sie zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="294d2-146">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="294d2-147">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="294d2-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="294d2-148">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="294d2-148">-SubnetId</span></span>
<span data-ttu-id="294d2-149">Gibt die Subnet-ID an.</span><span class="sxs-lookup"><span data-stu-id="294d2-149">Specifies the subnet ID.</span></span>
<span data-ttu-id="294d2-150">Geben Sie diesen Parameter an, wenn das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="294d2-150">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="294d2-151">Wenn der Parameter *PrivateIPAddress* angegeben wird, sollte er zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="294d2-151">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="294d2-152">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="294d2-152">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="294d2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="294d2-153">CommonParameters</span></span>
<span data-ttu-id="294d2-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="294d2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="294d2-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="294d2-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="294d2-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="294d2-156">INPUTS</span></span>

### <span data-ttu-id="294d2-157">System. String</span><span class="sxs-lookup"><span data-stu-id="294d2-157">System.String</span></span>

## <span data-ttu-id="294d2-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="294d2-158">OUTPUTS</span></span>

### <span data-ttu-id="294d2-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="294d2-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="294d2-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="294d2-160">NOTES</span></span>

## <span data-ttu-id="294d2-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="294d2-161">RELATED LINKS</span></span>

[<span data-ttu-id="294d2-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="294d2-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="294d2-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="294d2-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="294d2-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="294d2-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="294d2-165">Neu – AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="294d2-165">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="294d2-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="294d2-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)


