---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 5f91f333cf7983d50ba2984fcf01845a6c555e83
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300639"
---
# <span data-ttu-id="76b78-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76b78-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="76b78-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76b78-102">SYNOPSIS</span></span>
<span data-ttu-id="76b78-103">Erstellt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="76b78-103">Creates an application gateway.</span></span>

## <span data-ttu-id="76b78-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76b78-104">SYNTAX</span></span>

### <span data-ttu-id="76b78-105">IdentityByUserAssignedIdentityId (Standard)</span><span class="sxs-lookup"><span data-stu-id="76b78-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>]
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76b78-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="76b78-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76b78-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="76b78-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76b78-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="76b78-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity>
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76b78-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76b78-109">DESCRIPTION</span></span>
<span data-ttu-id="76b78-110">Mit dem Cmdlet **New-AzApplicationGateway** wird ein Azure Application Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="76b78-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="76b78-111">Für ein Anwendungsgateway ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="76b78-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="76b78-112">Eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="76b78-112">A resource group.</span></span>
- <span data-ttu-id="76b78-113">Ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="76b78-113">A virtual network.</span></span>
- <span data-ttu-id="76b78-114">Ein Back-End-Serverpool mit den IP-Adressen der Back-End-Server.</span><span class="sxs-lookup"><span data-stu-id="76b78-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="76b78-115">Einstellungen für den Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="76b78-115">Back-end server pool settings.</span></span> <span data-ttu-id="76b78-116">Jeder Pool verfügt über Einstellungen wie Port-, Protokoll-und Cookie-basierter Affinität, die auf alle Server innerhalb des Pools angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="76b78-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="76b78-117">Front-End-IP-Adressen, bei denen es sich um die IP-Adressen handelt, die auf dem Anwendungsgateway geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="76b78-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="76b78-118">Eine Front-End-IP-Adresse kann eine öffentliche IP-Adresse oder eine interne IP-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="76b78-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="76b78-119">Front-End-Ports, bei denen es sich um öffentliche Ports handelt, die auf dem Anwendungsgateway geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="76b78-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="76b78-120">Datenverkehr, der auf diese Ports trifft, wird an die Back-End-Server umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="76b78-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="76b78-121">Eine Anforderungs Routingregel, die den Listener und den Back-End-Serverpool bindet.</span><span class="sxs-lookup"><span data-stu-id="76b78-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="76b78-122">Die Regel definiert, an welchen Back-End-Serverpool der Datenverkehr weitergeleitet werden soll, wenn er auf einen bestimmten Listener trifft.</span><span class="sxs-lookup"><span data-stu-id="76b78-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="76b78-123">Ein Listener verfügt über einen Front-End-Port, eine Front-End-IP-Adresse, ein Protokoll (http oder HTTPS) und einen SSL-Zertifikatnamen (Secure Sockets Layer) (wenn die SSL-Verschiebung konfiguriert ist).</span><span class="sxs-lookup"><span data-stu-id="76b78-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="76b78-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76b78-124">EXAMPLES</span></span>

### <span data-ttu-id="76b78-125">Beispiel 1: Erstellen eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="76b78-125">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="76b78-126">Im folgenden Beispiel wird ein Anwendungsgateway erstellt, indem zunächst eine Ressourcengruppe und ein virtuelles Netzwerk sowie die folgenden Schritte erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="76b78-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="76b78-127">Ein Back-End-Serverpool</span><span class="sxs-lookup"><span data-stu-id="76b78-127">A back-end server pool</span></span>
- <span data-ttu-id="76b78-128">Einstellungen für den Back-End-Serverpool</span><span class="sxs-lookup"><span data-stu-id="76b78-128">Back-end server pool settings</span></span>
- <span data-ttu-id="76b78-129">Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="76b78-129">Front-end ports</span></span>
- <span data-ttu-id="76b78-130">Front-End-IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="76b78-130">Front-end IP addresses</span></span>
- <span data-ttu-id="76b78-131">Eine Anforderungs Routingregel mit diesen vier Befehlen wird ein virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="76b78-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="76b78-132">Der erste Befehl erstellt eine Subnet-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="76b78-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="76b78-133">Mit dem zweiten Befehl wird ein virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="76b78-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="76b78-134">Der dritte Befehl überprüft die Subnetz-Konfiguration, und der vierte Befehl überprüft, ob das virtuelle Netzwerk erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="76b78-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="76b78-135">Mit den folgenden Befehlen wird das Anwendungsgateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="76b78-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="76b78-136">Der erste Befehl erstellt eine IP-Konfiguration mit dem Namen "GatewayIp01" für das zuvor erstellte Subnetz.</span><span class="sxs-lookup"><span data-stu-id="76b78-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="76b78-137">Der zweite Befehl erstellt einen Back-End-Serverpool mit dem Namen Pool01 mit einer Liste der Back-End-IP-Adressen und speichert den Pool in der $Pool-Variablen.</span><span class="sxs-lookup"><span data-stu-id="76b78-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="76b78-138">Der dritte Befehl erstellt die Einstellungen für den Back-End-Serverpool und speichert die Einstellungen in der $PoolSetting-Variablen.</span><span class="sxs-lookup"><span data-stu-id="76b78-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="76b78-139">Der Befehl Forth erstellt einen Front-End-Port auf Port 80, benennt ihn FrontEndPort01 und speichert den Port in der $FrontEndPort-Variablen.</span><span class="sxs-lookup"><span data-stu-id="76b78-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="76b78-140">Der fünfte Befehl erstellt eine öffentliche IP-Adresse mithilfe von New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="76b78-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="76b78-141">Der sechste Befehl erstellt eine Front-End-IP-Konfiguration mit $PublicIp, benennt Sie FrontEndPortConfig01 und speichert Sie in der $FrontEndIpConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="76b78-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="76b78-142">Der siebte Befehl erstellt einen Listener mithilfe der zuvor erstellten $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="76b78-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="76b78-143">Der achte Befehl erstellt eine Regel für den Listener.</span><span class="sxs-lookup"><span data-stu-id="76b78-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="76b78-144">Der neunte Befehl legt die SKU fest.</span><span class="sxs-lookup"><span data-stu-id="76b78-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="76b78-145">Der zehnte Befehl erstellt das Gateway unter Verwendung der Objekte, die von den vorherigen Befehlen gesetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="76b78-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="76b78-146">Beispiel 2: Erstellen eines Anwendungs Gateways mit UserAssigned Identity</span><span class="sxs-lookup"><span data-stu-id="76b78-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Identity = New-AzUserAssignedIdentity -Name "Identity01" -ResourceGroupName "ResourceGroup01" -Location "West US"
PS C:\> $AppgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $Identity.Id
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $AppgwIdentity -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

## <span data-ttu-id="76b78-147">Parameter</span><span class="sxs-lookup"><span data-stu-id="76b78-147">PARAMETERS</span></span>

### <span data-ttu-id="76b78-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76b78-148">-AsJob</span></span>
<span data-ttu-id="76b78-149">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="76b78-149">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="76b78-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="76b78-151">Gibt Authentifizierungszertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="76b78-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76b78-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="76b78-153">AutoScale-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="76b78-153">Autoscale Configuration</span></span>

```yaml
Type: PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="76b78-154">-BackendAddressPools</span></span>
<span data-ttu-id="76b78-155">Gibt die Liste der Back-End-Adresspools für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="76b78-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="76b78-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="76b78-157">Gibt die Liste der Back-End-HTTP-Einstellungen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="76b78-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="76b78-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="76b78-159">Kunden Fehler eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="76b78-159">Customer error of an application gateway</span></span>

```yaml
Type: PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b78-160">-DefaultProfile</span></span>
<span data-ttu-id="76b78-161">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76b78-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76b78-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="76b78-162">-EnableFIPS</span></span>
<span data-ttu-id="76b78-163">Gibt an, ob FIPS aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="76b78-163">Whether FIPS is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="76b78-164">-EnableHttp2</span></span>
<span data-ttu-id="76b78-165">Gibt an, ob HTTP2 aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="76b78-165">Whether HTTP2 is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="76b78-166">-FirewallPolicy</span></span>
<span data-ttu-id="76b78-167">Firewall-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="76b78-167">Firewall configuration</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="76b78-168">-FirewallPolicyId</span></span>
<span data-ttu-id="76b78-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="76b78-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="76b78-170">-Force</span><span class="sxs-lookup"><span data-stu-id="76b78-170">-Force</span></span>
<span data-ttu-id="76b78-171">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="76b78-171">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="76b78-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="76b78-173">Ob Force firewallPolicy Association aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="76b78-173">Whether Force firewallPolicy association is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="76b78-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="76b78-175">Gibt eine Liste der Front-End-IP-Konfigurationen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="76b78-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="76b78-176">-FrontendPorts</span></span>
<span data-ttu-id="76b78-177">Gibt eine Liste der Front-End-Ports für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="76b78-177">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="76b78-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="76b78-179">Gibt eine Liste der IP-Konfigurationen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="76b78-179">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="76b78-180">-HttpListeners</span></span>
<span data-ttu-id="76b78-181">Gibt eine Liste der HTTP-Listener für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="76b78-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-182">-Identity</span><span class="sxs-lookup"><span data-stu-id="76b78-182">-Identity</span></span>
<span data-ttu-id="76b78-183">Application Gateway Identity, die dem Application Gateway zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="76b78-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-184">-Standort</span><span class="sxs-lookup"><span data-stu-id="76b78-184">-Location</span></span>
<span data-ttu-id="76b78-185">Gibt den Bereich an, in dem das Anwendungsgateway erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76b78-185">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-186">-Name</span><span class="sxs-lookup"><span data-stu-id="76b78-186">-Name</span></span>
<span data-ttu-id="76b78-187">Gibt den Namen des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="76b78-187">Specifies the name of application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-188">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="76b78-188">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="76b78-189">Die Liste der privateLink-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="76b78-189">The list of privateLink Configuration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-190">-Sonden</span><span class="sxs-lookup"><span data-stu-id="76b78-190">-Probes</span></span>
<span data-ttu-id="76b78-191">Gibt Prüfpunkte für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="76b78-191">Specifies probes for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-192">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="76b78-192">-RedirectConfigurations</span></span>
<span data-ttu-id="76b78-193">Die Liste der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="76b78-193">The list of redirect configuration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-194">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="76b78-194">-RequestRoutingRules</span></span>
<span data-ttu-id="76b78-195">Gibt eine Liste der Anforderungs Routingregeln für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="76b78-195">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76b78-196">-ResourceGroupName</span></span>
<span data-ttu-id="76b78-197">Gibt den Namen der Ressourcengruppe an, in der das Anwendungsgateway erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76b78-197">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-198">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="76b78-198">-RewriteRuleSet</span></span>
<span data-ttu-id="76b78-199">Die Liste der RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="76b78-199">The list of RewriteRuleSet</span></span>

```yaml
Type: PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-200">-SKU</span><span class="sxs-lookup"><span data-stu-id="76b78-200">-Sku</span></span>
<span data-ttu-id="76b78-201">Gibt die Lagerhaltungs Einheit (SKU) des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="76b78-201">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-202">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="76b78-202">-SslCertificates</span></span>
<span data-ttu-id="76b78-203">Gibt die Liste der SSL-Zertifikate (Secure Sockets Layer) für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="76b78-203">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-204">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="76b78-204">-SslPolicy</span></span>
<span data-ttu-id="76b78-205">Gibt eine SSL-Richtlinie für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="76b78-205">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-206">-Tag</span><span class="sxs-lookup"><span data-stu-id="76b78-206">-Tag</span></span>
<span data-ttu-id="76b78-207">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="76b78-207">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="76b78-208">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="76b78-208">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-209">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="76b78-209">-TrustedRootCertificate</span></span>
<span data-ttu-id="76b78-210">Liste der vertrauenswürdigen Stammzertifikate</span><span class="sxs-lookup"><span data-stu-id="76b78-210">The list of trusted root certificates</span></span>

```yaml
Type: PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-211">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="76b78-211">-UrlPathMaps</span></span>
<span data-ttu-id="76b78-212">Gibt URL-Pfad Zuordnungen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="76b78-212">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-213">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="76b78-213">-UserAssignedIdentityId</span></span>
<span data-ttu-id="76b78-214">Die ID des Benutzers, der dem Application Gateway zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="76b78-214">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-215">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="76b78-215">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="76b78-216">Gibt eine WAF-Konfiguration (Web Application Firewall) an.</span><span class="sxs-lookup"><span data-stu-id="76b78-216">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="76b78-217">Sie können das Get-AzApplicationGatewayWebApplicationFirewallConfiguration-Cmdlet verwenden, um eine WAF abzurufen.</span><span class="sxs-lookup"><span data-stu-id="76b78-217">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-218">-Zone</span><span class="sxs-lookup"><span data-stu-id="76b78-218">-Zone</span></span>
<span data-ttu-id="76b78-219">Eine Liste der Verfügbarkeits Zonen, die angibt, woher das Anwendungsgateway stammen muss.</span><span class="sxs-lookup"><span data-stu-id="76b78-219">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-220">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76b78-220">-Confirm</span></span>
<span data-ttu-id="76b78-221">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76b78-221">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-222">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76b78-222">-WhatIf</span></span>
<span data-ttu-id="76b78-223">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76b78-223">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76b78-224">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76b78-224">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b78-225">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b78-225">CommonParameters</span></span>
<span data-ttu-id="76b78-226">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76b78-226">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b78-227">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76b78-227">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b78-228">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76b78-228">INPUTS</span></span>

### <span data-ttu-id="76b78-229">System. String</span><span class="sxs-lookup"><span data-stu-id="76b78-229">System.String</span></span>

### <span data-ttu-id="76b78-230">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="76b78-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="76b78-231">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="76b78-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="76b78-232">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="76b78-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="76b78-233">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate []</span><span class="sxs-lookup"><span data-stu-id="76b78-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="76b78-234">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate []</span><span class="sxs-lookup"><span data-stu-id="76b78-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="76b78-235">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="76b78-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="76b78-236">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="76b78-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="76b78-237">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort []</span><span class="sxs-lookup"><span data-stu-id="76b78-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="76b78-238">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe []</span><span class="sxs-lookup"><span data-stu-id="76b78-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="76b78-239">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="76b78-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="76b78-240">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings []</span><span class="sxs-lookup"><span data-stu-id="76b78-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="76b78-241">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener []</span><span class="sxs-lookup"><span data-stu-id="76b78-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="76b78-242">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap []</span><span class="sxs-lookup"><span data-stu-id="76b78-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="76b78-243">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule []</span><span class="sxs-lookup"><span data-stu-id="76b78-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="76b78-244">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet []</span><span class="sxs-lookup"><span data-stu-id="76b78-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="76b78-245">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration []</span><span class="sxs-lookup"><span data-stu-id="76b78-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="76b78-246">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="76b78-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="76b78-247">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76b78-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="76b78-248">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="76b78-248">System.Collections.Hashtable</span></span>

### <span data-ttu-id="76b78-249">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="76b78-249">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="76b78-250">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76b78-250">OUTPUTS</span></span>

### <span data-ttu-id="76b78-251">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76b78-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="76b78-252">Notizen</span><span class="sxs-lookup"><span data-stu-id="76b78-252">NOTES</span></span>

## <span data-ttu-id="76b78-253">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76b78-253">RELATED LINKS</span></span>

[<span data-ttu-id="76b78-254">Neu – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="76b78-254">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="76b78-255">Neu – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="76b78-255">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="76b78-256">Neu – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="76b78-256">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="76b78-257">Neu – AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="76b78-257">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="76b78-258">Neu – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="76b78-258">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="76b78-259">Neu – AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="76b78-259">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="76b78-260">Neu – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="76b78-260">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="76b78-261">Neu – AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="76b78-261">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="76b78-262">Neu – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="76b78-262">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="76b78-263">Neu – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="76b78-263">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
