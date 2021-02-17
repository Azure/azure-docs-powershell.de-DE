---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172785"
---
# <span data-ttu-id="28397-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="28397-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="28397-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28397-102">SYNOPSIS</span></span>
<span data-ttu-id="28397-103">Erstellt eine Front-End-IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="28397-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="28397-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28397-104">SYNTAX</span></span>

### <span data-ttu-id="28397-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="28397-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28397-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="28397-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28397-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28397-107">DESCRIPTION</span></span>
<span data-ttu-id="28397-108">Das **Cmdlet "New-AzApplicationGatewayFrontendIPConfig"** erstellt eine Front-End-IP-Konfiguration für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="28397-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="28397-109">Ein Anwendungsgateway unterstützt zwei Arten von Front-End-IP-Konfigurationen:</span><span class="sxs-lookup"><span data-stu-id="28397-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="28397-110">Öffentliche IP-Adressen – Private IP-Adressen mit internem Lastenausgleich (ILB).</span><span class="sxs-lookup"><span data-stu-id="28397-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="28397-111">Ein Anwendungsgateway kann mindestens eine öffentliche und eine private IP-Adresse haben.</span><span class="sxs-lookup"><span data-stu-id="28397-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="28397-112">Die öffentliche und die private IP-Adresse sollten separat als Front-End-IP-Adressen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="28397-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="28397-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="28397-113">EXAMPLES</span></span>

### <span data-ttu-id="28397-114">Beispiel 1: Erstellen einer Front-End-IP-Konfiguration mit einem öffentlichen IP-Ressourcenobjekt</span><span class="sxs-lookup"><span data-stu-id="28397-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="28397-115">Der erste Befehl erstellt ein öffentliches IP-Ressourcenobjekt und speichert es in der $PublicIP Variable.</span><span class="sxs-lookup"><span data-stu-id="28397-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="28397-116">Der zweite Befehl verwendet $PublicIP zum Erstellen einer neuen Front-End-IP-Konfiguration namens FrontEndIP01 und speichert sie in der $FrontEnd Variable.</span><span class="sxs-lookup"><span data-stu-id="28397-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="28397-117">Beispiel 2: Erstellen einer statischen privaten IP als Front-End-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="28397-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="28397-118">Der erste Befehl ruft ein virtuelles Netzwerk namens VNet01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $VNet Variable.</span><span class="sxs-lookup"><span data-stu-id="28397-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="28397-119">Der zweite Befehl ruft eine Subnetzkonfiguration namens Subnetz01 mithilfe von $VNet des ersten Befehls ab und speichert ihn in der $Subnet Variable.</span><span class="sxs-lookup"><span data-stu-id="28397-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="28397-120">Der dritte Befehl erstellt eine Front-End-IP-Konfiguration namens FrontEndIP02 mithilfe von $Subnet aus dem zweiten Befehl und der privaten IP-Adresse 10.0.1.1 und speichert sie dann in der $FrontEnd-Variable.</span><span class="sxs-lookup"><span data-stu-id="28397-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="28397-121">Beispiel 3: Erstellen einer dynamischen privaten IP als Front-End-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="28397-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="28397-122">Der erste Befehl ruft ein virtuelles Netzwerk namens VNet01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $VNet Variable.</span><span class="sxs-lookup"><span data-stu-id="28397-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="28397-123">Der zweite Befehl ruft eine Subnetzkonfiguration namens Subnetz01 mithilfe von $VNet des ersten Befehls ab und speichert ihn in der $Subnet Variable.</span><span class="sxs-lookup"><span data-stu-id="28397-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="28397-124">Der dritte Befehl erstellt mithilfe von $Subnet des zweiten Befehls eine Front-End-IP-Konfiguration namens FrontEndIP03 und speichert sie in der $FrontEnd Variable.</span><span class="sxs-lookup"><span data-stu-id="28397-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="28397-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28397-125">PARAMETERS</span></span>

### <span data-ttu-id="28397-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28397-126">-DefaultProfile</span></span>
<span data-ttu-id="28397-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28397-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28397-128">-Name</span><span class="sxs-lookup"><span data-stu-id="28397-128">-Name</span></span>
<span data-ttu-id="28397-129">Gibt den Namen der Front-End-IP-Konfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="28397-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="28397-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="28397-130">-PrivateIPAddress</span></span>
<span data-ttu-id="28397-131">Gibt die private IP-Adresse an, die dieses Cmdlet der Front-End-IP-Adresse des Anwendungsgateways zugibt.</span><span class="sxs-lookup"><span data-stu-id="28397-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="28397-132">Dies kann nur angegeben werden, wenn ein Subnetz angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="28397-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="28397-133">Diese IP wird statisch aus dem Subnetz zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="28397-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="28397-134">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="28397-134">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="28397-135">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="28397-135">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="28397-136">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="28397-136">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="28397-137">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="28397-137">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="28397-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="28397-138">-PublicIPAddress</span></span>
<span data-ttu-id="28397-139">Gibt das öffentliche IP-Adressobjekt an, das dieses Cmdlet der Front-End-IP-Adresse des Anwendungsgateways zugibt.</span><span class="sxs-lookup"><span data-stu-id="28397-139">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="28397-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="28397-140">-PublicIPAddressId</span></span>
<span data-ttu-id="28397-141">Gibt die öffentliche IP-Adress-ID an, die dieses Cmdlet der Front-End-IP des Anwendungsgateways zugibt.</span><span class="sxs-lookup"><span data-stu-id="28397-141">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="28397-142">-Subnet</span><span class="sxs-lookup"><span data-stu-id="28397-142">-Subnet</span></span>
<span data-ttu-id="28397-143">Gibt das Subnetzobjekt an, das dieses Cmdlet der Front-End-IP-Adresse des Anwendungsgateways zugibt.</span><span class="sxs-lookup"><span data-stu-id="28397-143">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="28397-144">Wenn Sie diesen Parameter angeben, bedeutet dies, dass das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="28397-144">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="28397-145">Wenn der *Parameter "PrivateIPAddress"* angegeben wird, sollte er zu dem subnetz gehören, das durch diesen Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="28397-145">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="28397-146">Wenn *"PrivateIPAddress"* nicht angegeben wird, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungsgateways aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="28397-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="28397-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="28397-147">-SubnetId</span></span>
<span data-ttu-id="28397-148">Gibt die Subnetz-ID an, die dieses Cmdlet der Front-End-IP-Konfiguration des Anwendungsgateways zugibt.</span><span class="sxs-lookup"><span data-stu-id="28397-148">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="28397-149">Wenn Sie den Parameter *"Subnet"* angeben, bedeutet dies, dass das Gateway eine private IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="28397-149">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="28397-150">Wenn der *Parameter "PrivateIPAddress"* angegeben ist, sollte er zu dem Subnetz gehören, das durch Subnetz *angegeben ist.*</span><span class="sxs-lookup"><span data-stu-id="28397-150">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="28397-151">Wenn *"PrivateIPAddress"* nicht angegeben wird, wird eine der IP-Adressen aus diesem Subnetz dynamisch als Front-End-IP-Adresse des Anwendungsgateways aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="28397-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="28397-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28397-152">CommonParameters</span></span>
<span data-ttu-id="28397-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28397-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28397-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28397-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28397-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="28397-155">INPUTS</span></span>

### <span data-ttu-id="28397-156">Keine</span><span class="sxs-lookup"><span data-stu-id="28397-156">None</span></span>

## <span data-ttu-id="28397-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="28397-157">OUTPUTS</span></span>

### <span data-ttu-id="28397-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="28397-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="28397-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="28397-159">NOTES</span></span>

## <span data-ttu-id="28397-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="28397-160">RELATED LINKS</span></span>

[<span data-ttu-id="28397-161">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="28397-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="28397-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="28397-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="28397-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="28397-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="28397-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="28397-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


