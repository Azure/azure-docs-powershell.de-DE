---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: e5bbe82276cb356da1e5a66c45145c7daa1d8769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495853"
---
# <span data-ttu-id="3898c-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3898c-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="3898c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3898c-102">SYNOPSIS</span></span>
<span data-ttu-id="3898c-103">Ändert die Konfiguration einer Front-End-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="3898c-103">Modifies a front-end IP address configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3898c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3898c-104">SYNTAX</span></span>

### <span data-ttu-id="3898c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3898c-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3898c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3898c-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3898c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3898c-107">DESCRIPTION</span></span>
<span data-ttu-id="3898c-108">Das Cmdlet " **Satz-AzureRmApplicationGatewayFrontendIPConfig** " aktualisiert eine Front-End-IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3898c-108">The **Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="3898c-109">Ein Anwendungsgateway unterstützt zwei Arten von Front-End-IP-Adressen:</span><span class="sxs-lookup"><span data-stu-id="3898c-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="3898c-110">Öffentliche IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="3898c-110">Public IP addresses</span></span>
- <span data-ttu-id="3898c-111">Private IP-Adressen, für die die Konfiguration den internen Lastenausgleich (ILB) verwendet ein Anwendungsgateway kann höchstens eine öffentliche IP-Adresse und eine private IP-Adresse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3898c-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="3898c-112">Eine öffentliche IP-Adresse und eine private IP-Adresse sollten separat als Front-End-IP-Adressen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3898c-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="3898c-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3898c-113">EXAMPLES</span></span>

### <span data-ttu-id="3898c-114">Beispiel 1: Einrichten einer öffentlichen IP-Adresse als Front-End-IP eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="3898c-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="3898c-115">Der erste Befehl erstellt ein öffentliches IP-Adressen Objekt und speichert es in der $PublicIp-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3898c-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="3898c-116">Der zweite Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3898c-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3898c-117">Der dritte Befehl aktualisiert die Front-End-IP-Konfiguration mit dem Namen "FrontEndIp01" für das Gateway in $AppGw unter Verwendung der in $PublicIp gespeicherten Adresse.</span><span class="sxs-lookup"><span data-stu-id="3898c-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="3898c-118">Beispiel 2: Einrichten einer statischen privaten IP-Adresse als Front-End-IP eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="3898c-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="3898c-119">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3898c-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="3898c-120">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3898c-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="3898c-121">Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3898c-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3898c-122">Der vierte Befehl fügt eine Front-End-IP-Konfiguration mit dem Namen FrontendIP02 mit $Subnet aus dem zweiten Befehl und der privaten IP-Adresse 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="3898c-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="3898c-123">Beispiel 3: Einrichten einer dynamischen privaten IP-Adresse als Front-End-IP eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="3898c-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="3898c-124">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3898c-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="3898c-125">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3898c-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="3898c-126">Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3898c-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3898c-127">Der vierte Befehl fügt eine Front-End-IP-Konfiguration mit dem Namen FrontendIP02 mithilfe von $Subnet aus dem zweiten Befehl hinzu.</span><span class="sxs-lookup"><span data-stu-id="3898c-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="3898c-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="3898c-128">PARAMETERS</span></span>

### <span data-ttu-id="3898c-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3898c-129">-ApplicationGateway</span></span>
<span data-ttu-id="3898c-130">Gibt ein Application Gateway-Objekt an, in dem die Front-End-IP-Konfiguration geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3898c-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="3898c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3898c-131">-DefaultProfile</span></span>
<span data-ttu-id="3898c-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3898c-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3898c-133">-Name</span><span class="sxs-lookup"><span data-stu-id="3898c-133">-Name</span></span>
<span data-ttu-id="3898c-134">Gibt den Namen der Front-End-IP-Konfiguration an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3898c-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3898c-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="3898c-135">-PrivateIPAddress</span></span>
<span data-ttu-id="3898c-136">Gibt die private IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="3898c-136">Specifies the private IP address.</span></span>
<span data-ttu-id="3898c-137">Falls angegeben, wird diese IP-Adresse statisch vom Subnetz zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3898c-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="3898c-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="3898c-138">-PublicIPAddress</span></span>
<span data-ttu-id="3898c-139">Gibt die öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="3898c-139">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="3898c-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="3898c-140">-PublicIPAddressId</span></span>
<span data-ttu-id="3898c-141">Gibt die ID der öffentlichen IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="3898c-141">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="3898c-142">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="3898c-142">-Subnet</span></span>
<span data-ttu-id="3898c-143">Gibt das Subnetz an, das vom Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3898c-143">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="3898c-144">Geben Sie diesen Parameter an, wenn das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="3898c-144">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="3898c-145">Wenn die *PrivateIPAddress* -Adresse angegeben wird, sollte Sie zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="3898c-145">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="3898c-146">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="3898c-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="3898c-147">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="3898c-147">-SubnetId</span></span>
<span data-ttu-id="3898c-148">Gibt die Subnet-ID an.</span><span class="sxs-lookup"><span data-stu-id="3898c-148">Specifies the subnet ID.</span></span>
<span data-ttu-id="3898c-149">Geben Sie diesen Parameter an, wenn das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="3898c-149">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="3898c-150">Wenn der Parameter *PrivateIPAddress* angegeben wird, sollte er zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="3898c-150">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="3898c-151">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="3898c-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="3898c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3898c-152">CommonParameters</span></span>
<span data-ttu-id="3898c-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3898c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3898c-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3898c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3898c-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3898c-155">INPUTS</span></span>

### <span data-ttu-id="3898c-156">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3898c-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="3898c-157">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3898c-157">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="3898c-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3898c-158">OUTPUTS</span></span>

### <span data-ttu-id="3898c-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3898c-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3898c-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="3898c-160">NOTES</span></span>

## <span data-ttu-id="3898c-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3898c-161">RELATED LINKS</span></span>

[<span data-ttu-id="3898c-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3898c-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3898c-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3898c-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3898c-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3898c-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3898c-165">Neu – AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3898c-165">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3898c-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3898c-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)


