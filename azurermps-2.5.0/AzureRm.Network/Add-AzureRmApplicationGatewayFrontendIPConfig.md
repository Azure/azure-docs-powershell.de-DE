---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 646aaa2ec5d39089627caa97e74990ac3ce43b5c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849632"
---
# <span data-ttu-id="525b2-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="525b2-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="525b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="525b2-102">SYNOPSIS</span></span>
<span data-ttu-id="525b2-103">Fügt eine Front-End-IP-Konfiguration zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="525b2-103">Adds a front-end IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="525b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="525b2-104">SYNTAX</span></span>

### <span data-ttu-id="525b2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="525b2-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="525b2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="525b2-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="525b2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="525b2-107">DESCRIPTION</span></span>
<span data-ttu-id="525b2-108">Mit dem Cmdlet **Add-AzureRmApplicationGatewayFrontendIPConfig** wird ein Front-End-IP-Konfiguration zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="525b2-108">The **Add-AzureRmApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="525b2-109">Ein Anwendungsgateway unterstützt zwei Arten von Front-End-IP-Konfigurationen:</span><span class="sxs-lookup"><span data-stu-id="525b2-109">An application gateway supports two types of front-end IP configurations:</span></span> 

- <span data-ttu-id="525b2-110">Öffentliche IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="525b2-110">Public IP addresses</span></span>
- <span data-ttu-id="525b2-111">Private IP-Adressen mit internem Lastenausgleich (ILB)</span><span class="sxs-lookup"><span data-stu-id="525b2-111">Private IP addresses using internal load-balancing (ILB)</span></span>

<span data-ttu-id="525b2-112">Ein Anwendungsgateway kann höchstens eine öffentliche IP-Adresse und eine private IP-Adresse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="525b2-112">An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="525b2-113">Fügen Sie die öffentliche IP-Adresse und die private IP-Adresse als separate Front-End-IPS hinzu.</span><span class="sxs-lookup"><span data-stu-id="525b2-113">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="525b2-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="525b2-114">EXAMPLES</span></span>

### <span data-ttu-id="525b2-115">Beispiel 1: Hinzufügen einer öffentlichen IP-Adresse als Front-End-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="525b2-115">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="525b2-116">Der erste Befehl erstellt ein öffentliches IP-Adressen Objekt und speichert es in der $PublicIp-Variablen.</span><span class="sxs-lookup"><span data-stu-id="525b2-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="525b2-117">Der zweite Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="525b2-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="525b2-118">Der dritte Befehl fügt die Front-End-IP-Konfiguration mit dem Namen "FrontEndIp01" für das Gateway in $AppGw unter Verwendung der in $PublicIp gespeicherten Adresse hinzu.</span><span class="sxs-lookup"><span data-stu-id="525b2-118">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="525b2-119">Beispiel 2: Hinzufügen einer statischen privaten IP als Front-End-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="525b2-119">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="525b2-120">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="525b2-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="525b2-121">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="525b2-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="525b2-122">Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="525b2-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="525b2-123">Der vierte Befehl fügt eine Front-End-IP-Konfiguration mit dem Namen FrontendIP02 mit $Subnet aus dem zweiten Befehl und der privaten IP-Adresse 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="525b2-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="525b2-124">Beispiel 3: Hinzufügen einer dynamischen privaten IP als Front-End-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="525b2-124">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="525b2-125">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="525b2-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="525b2-126">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="525b2-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="525b2-127">Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="525b2-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="525b2-128">Der vierte Befehl fügt eine Front-End-IP-Konfiguration mit dem Namen FrontendIP02 mithilfe von $Subnet aus dem zweiten Befehl hinzu.</span><span class="sxs-lookup"><span data-stu-id="525b2-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="525b2-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="525b2-129">PARAMETERS</span></span>

### <span data-ttu-id="525b2-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="525b2-130">-ApplicationGateway</span></span>
<span data-ttu-id="525b2-131">Gibt das Anwendungsgateway an, dem dieses Cmdlet eine Front-End-IP-Konfiguration hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="525b2-131">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="525b2-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="525b2-132">-DefaultProfile</span></span>
<span data-ttu-id="525b2-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="525b2-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="525b2-134">-Name</span><span class="sxs-lookup"><span data-stu-id="525b2-134">-Name</span></span>
<span data-ttu-id="525b2-135">Gibt den Namen der Front-End-IP-Konfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="525b2-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="525b2-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="525b2-136">-PrivateIPAddress</span></span>
<span data-ttu-id="525b2-137">Gibt die private IP-Adresse an, die als Front-End-IP für das Anwendungsgateway hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="525b2-137">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="525b2-138">Falls angegeben, wird diese IP-Adresse statisch vom Subnetz zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="525b2-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="525b2-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="525b2-139">-PublicIPAddress</span></span>
<span data-ttu-id="525b2-140">Gibt die öffentliche IP-Adresse an, die von diesem Cmdlet als Front-End-IP-Adresse für das Anwendungsgateway hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="525b2-140">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="525b2-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="525b2-141">-PublicIPAddressId</span></span>
<span data-ttu-id="525b2-142">Gibt die ID der öffentlichen IP-Adresse an, die von diesem Cmdlet als Front-End-IP-Adresse für das Anwendungsgateway hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="525b2-142">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="525b2-143">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="525b2-143">-Subnet</span></span>
<span data-ttu-id="525b2-144">Gibt das Subnetz an, das dieses Cmdlet als Front-End-IP-Konfiguration hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="525b2-144">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="525b2-145">Wenn Sie diesen Parameter angeben, bedeutet dies, dass das Anwendungsgateway eine private IP-basierte Konfiguration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="525b2-145">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="525b2-146">Wenn der Parameter *PrivateIPAddress* angegeben wird, sollte er zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="525b2-146">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="525b2-147">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="525b2-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="525b2-148">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="525b2-148">-SubnetId</span></span>
<span data-ttu-id="525b2-149">Gibt die Subnetz-ID an, die dieses Cmdlet als Front-End-IP-Konfiguration hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="525b2-149">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="525b2-150">Das übergeben von Subnetz impliziert eine private IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="525b2-150">Passing subnet implies private IP.</span></span>
<span data-ttu-id="525b2-151">Wenn der Parameter *PrivateIPAddresss* angegeben wird, sollte er zu diesem Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="525b2-151">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="525b2-152">Andernfalls wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="525b2-152">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="525b2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="525b2-153">CommonParameters</span></span>
<span data-ttu-id="525b2-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="525b2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="525b2-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="525b2-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="525b2-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="525b2-156">INPUTS</span></span>

### <span data-ttu-id="525b2-157">System. String</span><span class="sxs-lookup"><span data-stu-id="525b2-157">System.String</span></span>

## <span data-ttu-id="525b2-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="525b2-158">OUTPUTS</span></span>

### <span data-ttu-id="525b2-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="525b2-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="525b2-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="525b2-160">NOTES</span></span>

## <span data-ttu-id="525b2-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="525b2-161">RELATED LINKS</span></span>

[<span data-ttu-id="525b2-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="525b2-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="525b2-163">Neu – AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="525b2-163">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="525b2-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="525b2-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="525b2-165">Satz-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="525b2-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


