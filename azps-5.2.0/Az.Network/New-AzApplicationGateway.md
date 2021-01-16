---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 0f3d65c629218fc903035cb9df669f1c3dc7a50c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361079"
---
# <span data-ttu-id="46f0d-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46f0d-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="46f0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="46f0d-103">Erstellt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="46f0d-103">Creates an application gateway.</span></span>

## <span data-ttu-id="46f0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46f0d-104">SYNTAX</span></span>

### <span data-ttu-id="46f0d-105">IdentityByUserAssignedIdentityId (Standard)</span><span class="sxs-lookup"><span data-stu-id="46f0d-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

### <span data-ttu-id="46f0d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="46f0d-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

### <span data-ttu-id="46f0d-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="46f0d-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

### <span data-ttu-id="46f0d-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="46f0d-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

## <span data-ttu-id="46f0d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46f0d-109">DESCRIPTION</span></span>
<span data-ttu-id="46f0d-110">Das **Cmdlet "New-AzApplicationGateway"** erstellt ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="46f0d-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="46f0d-111">Für ein Anwendungsgateway ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="46f0d-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="46f0d-112">Eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="46f0d-112">A resource group.</span></span>
- <span data-ttu-id="46f0d-113">Ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="46f0d-113">A virtual network.</span></span>
- <span data-ttu-id="46f0d-114">Ein Back-End-Serverpool, der die IP-Adressen der Back-End-Server enthält.</span><span class="sxs-lookup"><span data-stu-id="46f0d-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="46f0d-115">Back-End-Serverpooleinstellungen.</span><span class="sxs-lookup"><span data-stu-id="46f0d-115">Back-end server pool settings.</span></span> <span data-ttu-id="46f0d-116">Jeder Pool verfügt über Einstellungen wie Port, Protokoll und cookiebasierte Affinität, die auf alle Server im Pool angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="46f0d-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="46f0d-117">Front-End-IP-Adressen, bei denen es sich um die im Anwendungsgateway geöffneten IP-Adressen handelt.</span><span class="sxs-lookup"><span data-stu-id="46f0d-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="46f0d-118">Eine Front-End-IP-Adresse kann eine öffentliche oder eine interne IP-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="46f0d-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="46f0d-119">Front-End-Ports, bei denen es sich um die öffentlichen Ports handelt, die auf dem Anwendungsgateway geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="46f0d-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="46f0d-120">Datenverkehr, der diese Ports erreicht, wird an die Back-End-Server umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="46f0d-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="46f0d-121">Eine Anforderungsroutingregel, die den Listener und den Back-End-Serverpool bindet.</span><span class="sxs-lookup"><span data-stu-id="46f0d-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="46f0d-122">Die Regel definiert, an welchen Back-End-Serverpool der Datenverkehr geleitet werden soll, wenn er einen bestimmten Listener erreicht.</span><span class="sxs-lookup"><span data-stu-id="46f0d-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="46f0d-123">Ein Listener verfügt über einen Front-End-Port, eine Front-End-IP-Adresse, ein Protokoll (HTTP oder HTTPS) und einen Zertifikatnamen für Secure Sockets Layer (SSL) (wenn die SSL-Auslagerung konfiguriert wird).</span><span class="sxs-lookup"><span data-stu-id="46f0d-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="46f0d-124">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46f0d-124">EXAMPLES</span></span>

### <span data-ttu-id="46f0d-125">Beispiel 1: Erstellen eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="46f0d-125">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="46f0d-126">Im folgenden Beispiel wird ein Anwendungsgateway erstellt, indem zuerst eine Ressourcengruppe und ein virtuelles Netzwerk erstellt werden, sowie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="46f0d-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="46f0d-127">Back-End-Serverpool</span><span class="sxs-lookup"><span data-stu-id="46f0d-127">A back-end server pool</span></span>
- <span data-ttu-id="46f0d-128">Back-End-Serverpooleinstellungen</span><span class="sxs-lookup"><span data-stu-id="46f0d-128">Back-end server pool settings</span></span>
- <span data-ttu-id="46f0d-129">Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="46f0d-129">Front-end ports</span></span>
- <span data-ttu-id="46f0d-130">Front-End-IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="46f0d-130">Front-end IP addresses</span></span>
- <span data-ttu-id="46f0d-131">Anforderungsroutingregel Mit diesen vier Befehlen wird ein virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="46f0d-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="46f0d-132">Der erste Befehl erstellt eine Subnetzkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="46f0d-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="46f0d-133">Der zweite Befehl erstellt ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="46f0d-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="46f0d-134">Mit dem dritten Befehl wird die Subnetzkonfiguration überprüft, und mit dem vierten Befehl wird überprüft, ob das virtuelle Netzwerk erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="46f0d-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="46f0d-135">Mit den folgenden Befehlen wird das Anwendungsgateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="46f0d-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="46f0d-136">Der erste Befehl erstellt eine IP-Konfiguration namens GatewayIp01 für das zuvor erstellte Subnetz.</span><span class="sxs-lookup"><span data-stu-id="46f0d-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="46f0d-137">Der zweite Befehl erstellt einen Back-End-Serverpool namens Pool01 mit einer Liste von Back-End-IP-Adressen und speichert den Pool in der $Pool Variable.</span><span class="sxs-lookup"><span data-stu-id="46f0d-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="46f0d-138">Der dritte Befehl erstellt die Einstellungen für den Back-End-Serverpool und speichert die Einstellungen in der $PoolSetting Variable.</span><span class="sxs-lookup"><span data-stu-id="46f0d-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="46f0d-139">Der vierte Befehl erstellt einen Front-End-Port auf Port 80, nennt ihn "FrontEndPort01" und speichert den Port in der $FrontEndPort Variable.</span><span class="sxs-lookup"><span data-stu-id="46f0d-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="46f0d-140">Der fünfte Befehl erstellt mithilfe von "New-AzPublicIpAddress" eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="46f0d-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="46f0d-141">Der sechste Befehl erstellt eine Front-End-IP-Konfiguration mit $PublicIp, nennt sie "FrontEndPortConfig01" und speichert sie in der $FrontEndIpConfig Variable.</span><span class="sxs-lookup"><span data-stu-id="46f0d-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="46f0d-142">Der siebte Befehl erstellt einen Listener mithilfe der zuvor erstellten $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="46f0d-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="46f0d-143">Mit dem achten Befehl wird eine Regel für den Listener erstellt.</span><span class="sxs-lookup"><span data-stu-id="46f0d-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="46f0d-144">Mit dem neunten Befehl wird die SKU bestimmt.</span><span class="sxs-lookup"><span data-stu-id="46f0d-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="46f0d-145">Der zehnte Befehl erstellt das Gateway mit den Objekten, die in den vorherigen Befehlen festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="46f0d-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="46f0d-146">Beispiel 2: Erstellen eines Anwendungsgateways mit "UserAssigned Identity"</span><span class="sxs-lookup"><span data-stu-id="46f0d-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
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

## <span data-ttu-id="46f0d-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46f0d-147">PARAMETERS</span></span>

### <span data-ttu-id="46f0d-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46f0d-148">-AsJob</span></span>
<span data-ttu-id="46f0d-149">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="46f0d-149">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="46f0d-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="46f0d-151">Gibt Authentifizierungszertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="46f0d-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="46f0d-153">Konfiguration der automatischen Skala</span><span class="sxs-lookup"><span data-stu-id="46f0d-153">Autoscale Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-154">-Back-EndAddressPools</span><span class="sxs-lookup"><span data-stu-id="46f0d-154">-BackendAddressPools</span></span>
<span data-ttu-id="46f0d-155">Gibt die Liste der Back-End-Adresspools für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-156">-Back-EndHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="46f0d-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="46f0d-157">Gibt die Liste der Back-End-HTTP-Einstellungen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="46f0d-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="46f0d-159">Kundenfehler eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="46f0d-159">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f0d-160">-DefaultProfile</span></span>
<span data-ttu-id="46f0d-161">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46f0d-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="46f0d-162">-EnableFIPS</span></span>
<span data-ttu-id="46f0d-163">Gibt an, ob FIPS aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="46f0d-163">Whether FIPS is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="46f0d-164">-EnableHttp2</span></span>
<span data-ttu-id="46f0d-165">Gibt an, ob HTTP2 aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="46f0d-165">Whether HTTP2 is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="46f0d-166">-FirewallPolicy</span></span>
<span data-ttu-id="46f0d-167">Firewallkonfiguration</span><span class="sxs-lookup"><span data-stu-id="46f0d-167">Firewall configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="46f0d-168">-FirewallPolicyId</span></span>
<span data-ttu-id="46f0d-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="46f0d-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="46f0d-170">-Force</span><span class="sxs-lookup"><span data-stu-id="46f0d-170">-Force</span></span>
<span data-ttu-id="46f0d-171">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="46f0d-171">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="46f0d-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="46f0d-173">Ob die Zuordnung "firewallPolicy erzwingen" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="46f0d-173">Whether Force firewallPolicy association is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="46f0d-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="46f0d-175">Gibt eine Liste der Front-End-IP-Konfigurationen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="46f0d-176">-FrontendPorts</span></span>
<span data-ttu-id="46f0d-177">Gibt eine Liste der Front-End-Ports für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-177">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="46f0d-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="46f0d-179">Gibt eine Liste der IP-Konfigurationen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-179">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="46f0d-180">-HttpListeners</span></span>
<span data-ttu-id="46f0d-181">Gibt eine Liste der HTTP-Listener für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-182">-Identity</span><span class="sxs-lookup"><span data-stu-id="46f0d-182">-Identity</span></span>
<span data-ttu-id="46f0d-183">Anwendungsgatewayidentität, die dem Anwendungsgateway zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="46f0d-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-184">-Location</span><span class="sxs-lookup"><span data-stu-id="46f0d-184">-Location</span></span>
<span data-ttu-id="46f0d-185">Gibt den Bereich an, in dem das Anwendungsgateway erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="46f0d-185">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-186">-Name</span><span class="sxs-lookup"><span data-stu-id="46f0d-186">-Name</span></span>
<span data-ttu-id="46f0d-187">Gibt den Namen des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-187">Specifies the name of application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-188">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="46f0d-188">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="46f0d-189">Die Liste der Konfiguration von "privateLink"</span><span class="sxs-lookup"><span data-stu-id="46f0d-189">The list of privateLink Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-190">-Probes</span><span class="sxs-lookup"><span data-stu-id="46f0d-190">-Probes</span></span>
<span data-ttu-id="46f0d-191">Gibt Probes für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-191">Specifies probes for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-192">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="46f0d-192">-RedirectConfigurations</span></span>
<span data-ttu-id="46f0d-193">Die Liste der Umleitungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="46f0d-193">The list of redirect configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-194">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="46f0d-194">-RequestRoutingRules</span></span>
<span data-ttu-id="46f0d-195">Gibt eine Liste der Anforderungsroutingregeln für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-195">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f0d-196">-ResourceGroupName</span></span>
<span data-ttu-id="46f0d-197">Gibt den Namen der Ressourcengruppe an, in der das Anwendungsgateway erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="46f0d-197">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-198">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46f0d-198">-RewriteRuleSet</span></span>
<span data-ttu-id="46f0d-199">Die Liste von "RewriteRuleSet"</span><span class="sxs-lookup"><span data-stu-id="46f0d-199">The list of RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-200">-SKU</span><span class="sxs-lookup"><span data-stu-id="46f0d-200">-Sku</span></span>
<span data-ttu-id="46f0d-201">Gibt die SKU (Stock Keeping Unit) des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-201">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-202">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="46f0d-202">-SslCertificates</span></span>
<span data-ttu-id="46f0d-203">Gibt die Liste der Secure Sockets Layer (SSL)-Zertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-203">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-204">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="46f0d-204">-SslPolicy</span></span>
<span data-ttu-id="46f0d-205">Gibt eine "SSL"-Richtlinie für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-205">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-206">-SslProfiles</span><span class="sxs-lookup"><span data-stu-id="46f0d-206">-SslProfiles</span></span>
<span data-ttu-id="46f0d-207">Die Liste der Ssl-Profile</span><span class="sxs-lookup"><span data-stu-id="46f0d-207">The list of ssl profiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-208">-Tag</span><span class="sxs-lookup"><span data-stu-id="46f0d-208">-Tag</span></span>
<span data-ttu-id="46f0d-209">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="46f0d-209">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="46f0d-210">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="46f0d-210">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-211">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="46f0d-211">-TrustedClientCertificates</span></span>
<span data-ttu-id="46f0d-212">Liste der Zertifikatketten einer vertrauenswürdigen Client-Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="46f0d-212">The list of trusted client CA certificate chains</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-213">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="46f0d-213">-TrustedRootCertificate</span></span>
<span data-ttu-id="46f0d-214">Liste der vertrauenswürdigen Stammzertifikate</span><span class="sxs-lookup"><span data-stu-id="46f0d-214">The list of trusted root certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-215">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="46f0d-215">-UrlPathMaps</span></span>
<span data-ttu-id="46f0d-216">Gibt die URL-Pfadzuordnungen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-216">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-217">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="46f0d-217">-UserAssignedIdentityId</span></span>
<span data-ttu-id="46f0d-218">ResourceId der dem Anwendungsgateway zugewiesenen Benutzeridentität.</span><span class="sxs-lookup"><span data-stu-id="46f0d-218">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-219">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="46f0d-219">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="46f0d-220">Gibt eine Konfiguration der Webanwendungsfirewall (Web Application Firewall, WAF) an.</span><span class="sxs-lookup"><span data-stu-id="46f0d-220">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="46f0d-221">Sie können das cmdlet Get-AzApplicationGatewayWebApplicationFirewallConfiguration A0 verwenden, um ein WAF zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="46f0d-221">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-222">-Zone</span><span class="sxs-lookup"><span data-stu-id="46f0d-222">-Zone</span></span>
<span data-ttu-id="46f0d-223">Eine Liste der Verfügbarkeitszonen, in denen aufgeführt ist, woher das Anwendungsgateway stammen muss.</span><span class="sxs-lookup"><span data-stu-id="46f0d-223">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-224">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46f0d-224">-Confirm</span></span>
<span data-ttu-id="46f0d-225">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46f0d-225">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-226">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="46f0d-226">-WhatIf</span></span>
<span data-ttu-id="46f0d-227">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46f0d-227">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46f0d-228">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46f0d-228">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f0d-229">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f0d-229">CommonParameters</span></span>
<span data-ttu-id="46f0d-230">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f0d-230">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f0d-231">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46f0d-231">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f0d-232">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46f0d-232">INPUTS</span></span>

### <span data-ttu-id="46f0d-233">System.String</span><span class="sxs-lookup"><span data-stu-id="46f0d-233">System.String</span></span>

### <span data-ttu-id="46f0d-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="46f0d-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="46f0d-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="46f0d-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="46f0d-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="46f0d-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="46f0d-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="46f0d-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="46f0d-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="46f0d-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="46f0d-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="46f0d-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="46f0d-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="46f0d-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="46f0d-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="46f0d-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="46f0d-248">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-248">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="46f0d-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="46f0d-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="46f0d-250">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="46f0d-250">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="46f0d-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="46f0d-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="46f0d-252">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="46f0d-252">System.Collections.Hashtable</span></span>

### <span data-ttu-id="46f0d-253">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="46f0d-253">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="46f0d-254">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46f0d-254">OUTPUTS</span></span>

### <span data-ttu-id="46f0d-255">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46f0d-255">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="46f0d-256">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="46f0d-256">NOTES</span></span>

## <span data-ttu-id="46f0d-257">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="46f0d-257">RELATED LINKS</span></span>

[<span data-ttu-id="46f0d-258">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="46f0d-258">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="46f0d-259">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="46f0d-259">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="46f0d-260">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="46f0d-260">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="46f0d-261">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="46f0d-261">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="46f0d-262">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="46f0d-262">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="46f0d-263">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="46f0d-263">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="46f0d-264">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="46f0d-264">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="46f0d-265">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="46f0d-265">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="46f0d-266">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46f0d-266">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="46f0d-267">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="46f0d-267">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
