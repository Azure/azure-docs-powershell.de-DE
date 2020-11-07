---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dfbdebf2815bf94fcda5fb5a69804b55bb226d67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841435"
---
# <span data-ttu-id="293c0-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="293c0-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="293c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="293c0-102">SYNOPSIS</span></span>
<span data-ttu-id="293c0-103">Erstellt eine Front-End-IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="293c0-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="293c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="293c0-104">SYNTAX</span></span>

### <span data-ttu-id="293c0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="293c0-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="293c0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="293c0-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="293c0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="293c0-107">DESCRIPTION</span></span>
<span data-ttu-id="293c0-108">Mit dem Cmdlet **New-AzApplicationGatewayFrontendIPConfig** wird ein Front-End-IP-Konfigurations für ein Azure Application Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="293c0-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuraton for an Azure application gateway.</span></span>
<span data-ttu-id="293c0-109">Ein Anwendungsgateway unterstützt zwei Arten der Front-End-IP-Konfiguration:</span><span class="sxs-lookup"><span data-stu-id="293c0-109">An application gateway supports two types of front-end IP configuration:</span></span> 

- <span data-ttu-id="293c0-110">Öffentliche IP-Adressen – private IP-Adressen mit internem Lastenausgleich (ILB).</span><span class="sxs-lookup"><span data-stu-id="293c0-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>

<span data-ttu-id="293c0-111">Ein Anwendungsgateway kann höchstens eine öffentliche IP-Adresse und eine private IP-Adresse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="293c0-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="293c0-112">Die öffentliche IP-Adresse und die private IP-Adresse sollten separat als Front-End-IP-Adressen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="293c0-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="293c0-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="293c0-113">EXAMPLES</span></span>

### <span data-ttu-id="293c0-114">Beispiel 1: Erstellen einer Front-End-IP-Konfiguration mithilfe eines öffentlichen IP-Ressourcenobjekts</span><span class="sxs-lookup"><span data-stu-id="293c0-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="293c0-115">Der erste Befehl erstellt ein öffentliches IP-Ressourcenobjekt und speichert es in der $PublicIP-Variablen.</span><span class="sxs-lookup"><span data-stu-id="293c0-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="293c0-116">Der zweite Befehl verwendet $PublicIP, um eine neue Front-End-IP-Konfiguration mit dem Namen FrontEndIP01 zu erstellen, und speichert Sie in der $Frontend-Variablen.</span><span class="sxs-lookup"><span data-stu-id="293c0-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="293c0-117">Beispiel 2: Erstellen einer statischen privaten IP als Front-End-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="293c0-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="293c0-118">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="293c0-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="293c0-119">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="293c0-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="293c0-120">Der dritte Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontEndIP02 mit $Subnet aus dem zweiten Befehl und der privaten IP-Adresse 10.0.1.1 und speichert Sie dann in der $Frontend-Variablen.</span><span class="sxs-lookup"><span data-stu-id="293c0-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="293c0-121">Beispiel 3: Erstellen einer dynamischen privaten IP-Adresse als Front-End-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="293c0-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="293c0-122">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="293c0-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="293c0-123">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="293c0-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="293c0-124">Der dritte Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontEndIP03 mit $Subnet aus dem zweiten Befehl und speichert Sie in der $Frontend-Variablen.</span><span class="sxs-lookup"><span data-stu-id="293c0-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="293c0-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="293c0-125">PARAMETERS</span></span>

### <span data-ttu-id="293c0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293c0-126">-DefaultProfile</span></span>
<span data-ttu-id="293c0-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="293c0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="293c0-128">-Name</span><span class="sxs-lookup"><span data-stu-id="293c0-128">-Name</span></span>
<span data-ttu-id="293c0-129">Gibt den Namen der Front-End-IP-Konfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="293c0-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="293c0-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="293c0-130">-PrivateIPAddress</span></span>
<span data-ttu-id="293c0-131">Gibt die private IP-Adresse an, die dieses Cmdlet der Front-End-IP-Adresse des Anwendungs Gateways zuordnet.</span><span class="sxs-lookup"><span data-stu-id="293c0-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="293c0-132">Dies kann nur angegeben werden, wenn ein Subnetz angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="293c0-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="293c0-133">Diese IP-Adresse wird statisch aus dem Subnetz zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="293c0-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="293c0-134">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="293c0-134">-PublicIPAddress</span></span>
<span data-ttu-id="293c0-135">Gibt das öffentliche IP-Adressen Objekt an, das dieses Cmdlet der Front-End-IP-Adresse des Anwendungs Gateways zuordnet.</span><span class="sxs-lookup"><span data-stu-id="293c0-135">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="293c0-136">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="293c0-136">-PublicIPAddressId</span></span>
<span data-ttu-id="293c0-137">Gibt die öffentliche IP-Adresse an, die dieses Cmdlet der Front-End-IP des Anwendungs Gateways zuordnet.</span><span class="sxs-lookup"><span data-stu-id="293c0-137">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="293c0-138">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="293c0-138">-Subnet</span></span>
<span data-ttu-id="293c0-139">Gibt das Subnet-Objekt an, das dieses Cmdlet der Front-End-IP-Adresse des Anwendungs Gateways zuordnet.</span><span class="sxs-lookup"><span data-stu-id="293c0-139">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="293c0-140">Wenn Sie diesen Parameter angeben, bedeutet dies, dass das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="293c0-140">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="293c0-141">Wenn der *PrivateIPAddresss* -Parameter angegeben wird, sollte er zu dem durch diesen Parameter angegebenen Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="293c0-141">If the *PrivateIPAddresss* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="293c0-142">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="293c0-142">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="293c0-143">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="293c0-143">-SubnetId</span></span>
<span data-ttu-id="293c0-144">Gibt die Subnetz-ID an, die dieses Cmdlet der Front-End-IP-Konfiguration des Anwendungs Gateways zuordnet.</span><span class="sxs-lookup"><span data-stu-id="293c0-144">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="293c0-145">Wenn Sie den Parameter *Subnet* angeben, bedeutet dies, dass das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="293c0-145">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="293c0-146">Wenn der Parameter *PrivateIPAddress* angegeben wird, sollte er zu dem Subnetz gehören, das von *Subnetz* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="293c0-146">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="293c0-147">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="293c0-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="293c0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293c0-148">CommonParameters</span></span>
<span data-ttu-id="293c0-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="293c0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293c0-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="293c0-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293c0-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="293c0-151">INPUTS</span></span>

### <span data-ttu-id="293c0-152">System. String</span><span class="sxs-lookup"><span data-stu-id="293c0-152">System.String</span></span>

## <span data-ttu-id="293c0-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="293c0-153">OUTPUTS</span></span>

### <span data-ttu-id="293c0-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="293c0-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="293c0-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="293c0-155">NOTES</span></span>

## <span data-ttu-id="293c0-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="293c0-156">RELATED LINKS</span></span>

[<span data-ttu-id="293c0-157">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="293c0-157">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="293c0-158">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="293c0-158">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="293c0-159">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="293c0-159">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="293c0-160">Satz-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="293c0-160">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


