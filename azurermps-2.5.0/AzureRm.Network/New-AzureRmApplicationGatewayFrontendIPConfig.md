---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 2003d93a50b1730a162cc910ef289748a86a2954
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848444"
---
# <span data-ttu-id="fb557-101">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fb557-101">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="fb557-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb557-102">SYNOPSIS</span></span>
<span data-ttu-id="fb557-103">Erstellt eine Front-End-IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="fb557-103">Creates a front-end IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb557-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb557-104">SYNTAX</span></span>

### <span data-ttu-id="fb557-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb557-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb557-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fb557-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb557-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb557-107">DESCRIPTION</span></span>
<span data-ttu-id="fb557-108">Mit dem Cmdlet **New-AzureRmApplicationGatewayFrontendIPConfig** wird ein Front-End-IP-Konfigurations für ein Azure Application Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="fb557-108">The **New-AzureRmApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuraton for an Azure application gateway.</span></span>
<span data-ttu-id="fb557-109">Ein Anwendungsgateway unterstützt zwei Arten der Front-End-IP-Konfiguration:</span><span class="sxs-lookup"><span data-stu-id="fb557-109">An application gateway supports two types of front-end IP configuration:</span></span> 

- <span data-ttu-id="fb557-110">Öffentliche IP-Adressen – private IP-Adressen mit internem Lastenausgleich (ILB).</span><span class="sxs-lookup"><span data-stu-id="fb557-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>

<span data-ttu-id="fb557-111">Ein Anwendungsgateway kann höchstens eine öffentliche IP-Adresse und eine private IP-Adresse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fb557-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="fb557-112">Die öffentliche IP-Adresse und die private IP-Adresse sollten separat als Front-End-IP-Adressen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fb557-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="fb557-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb557-113">EXAMPLES</span></span>

### <span data-ttu-id="fb557-114">Beispiel 1: Erstellen einer Front-End-IP-Konfiguration mithilfe eines öffentlichen IP-Ressourcenobjekts</span><span class="sxs-lookup"><span data-stu-id="fb557-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="fb557-115">Der erste Befehl erstellt ein öffentliches IP-Ressourcenobjekt und speichert es in der $PublicIP-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fb557-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="fb557-116">Der zweite Befehl verwendet $PublicIP, um eine neue Front-End-IP-Konfiguration mit dem Namen FrontEndIP01 zu erstellen, und speichert Sie in der $Frontend-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fb557-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="fb557-117">Beispiel 2: Erstellen einer statischen privaten IP als Front-End-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="fb557-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="fb557-118">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fb557-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="fb557-119">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fb557-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="fb557-120">Der dritte Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontEndIP02 mit $Subnet aus dem zweiten Befehl und der privaten IP-Adresse 10.0.1.1 und speichert Sie dann in der $Frontend-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fb557-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="fb557-121">Beispiel 3: Erstellen einer dynamischen privaten IP-Adresse als Front-End-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="fb557-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="fb557-122">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fb557-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="fb557-123">Der zweite Befehl ruft eine Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet aus dem ersten Befehl ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fb557-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="fb557-124">Der dritte Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontEndIP03 mit $Subnet aus dem zweiten Befehl und speichert Sie in der $Frontend-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fb557-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="fb557-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb557-125">PARAMETERS</span></span>

### <span data-ttu-id="fb557-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb557-126">-DefaultProfile</span></span>
<span data-ttu-id="fb557-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb557-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb557-128">-Name</span><span class="sxs-lookup"><span data-stu-id="fb557-128">-Name</span></span>
<span data-ttu-id="fb557-129">Gibt den Namen der Front-End-IP-Konfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fb557-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fb557-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="fb557-130">-PrivateIPAddress</span></span>
<span data-ttu-id="fb557-131">Gibt die private IP-Adresse an, die dieses Cmdlet der Front-End-IP-Adresse des Anwendungs Gateways zuordnet.</span><span class="sxs-lookup"><span data-stu-id="fb557-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="fb557-132">Dies kann nur angegeben werden, wenn ein Subnetz angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fb557-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="fb557-133">Diese IP-Adresse wird statisch aus dem Subnetz zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="fb557-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="fb557-134">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="fb557-134">-PublicIPAddress</span></span>
<span data-ttu-id="fb557-135">Gibt das öffentliche IP-Adressen Objekt an, das dieses Cmdlet der Front-End-IP-Adresse des Anwendungs Gateways zuordnet.</span><span class="sxs-lookup"><span data-stu-id="fb557-135">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="fb557-136">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="fb557-136">-PublicIPAddressId</span></span>
<span data-ttu-id="fb557-137">Gibt die öffentliche IP-Adresse an, die dieses Cmdlet der Front-End-IP des Anwendungs Gateways zuordnet.</span><span class="sxs-lookup"><span data-stu-id="fb557-137">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="fb557-138">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="fb557-138">-Subnet</span></span>
<span data-ttu-id="fb557-139">Gibt das Subnet-Objekt an, das dieses Cmdlet der Front-End-IP-Adresse des Anwendungs Gateways zuordnet.</span><span class="sxs-lookup"><span data-stu-id="fb557-139">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="fb557-140">Wenn Sie diesen Parameter angeben, bedeutet dies, dass das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="fb557-140">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="fb557-141">Wenn der *PrivateIPAddresss* -Parameter angegeben wird, sollte er zu dem durch diesen Parameter angegebenen Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="fb557-141">If the *PrivateIPAddresss* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="fb557-142">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="fb557-142">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="fb557-143">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="fb557-143">-SubnetId</span></span>
<span data-ttu-id="fb557-144">Gibt die Subnetz-ID an, die dieses Cmdlet der Front-End-IP-Konfiguration des Anwendungs Gateways zuordnet.</span><span class="sxs-lookup"><span data-stu-id="fb557-144">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="fb557-145">Wenn Sie den Parameter *Subnet* angeben, bedeutet dies, dass das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="fb557-145">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="fb557-146">Wenn der Parameter *PrivateIPAddress* angegeben wird, sollte er zu dem Subnetz gehören, das von *Subnetz* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fb557-146">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="fb557-147">Wenn *PrivateIPAddress* nicht angegeben ist, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungs Gateways übernommen.</span><span class="sxs-lookup"><span data-stu-id="fb557-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="fb557-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb557-148">CommonParameters</span></span>
<span data-ttu-id="fb557-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb557-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb557-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb557-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb557-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb557-151">INPUTS</span></span>

### <span data-ttu-id="fb557-152">System. String</span><span class="sxs-lookup"><span data-stu-id="fb557-152">System.String</span></span>

## <span data-ttu-id="fb557-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb557-153">OUTPUTS</span></span>

### <span data-ttu-id="fb557-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb557-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="fb557-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb557-155">NOTES</span></span>

## <span data-ttu-id="fb557-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb557-156">RELATED LINKS</span></span>

[<span data-ttu-id="fb557-157">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fb557-157">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fb557-158">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fb557-158">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fb557-159">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fb557-159">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fb557-160">Satz-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fb557-160">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


