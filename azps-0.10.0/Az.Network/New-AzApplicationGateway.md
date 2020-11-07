---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 1945ceb84f6ccc9af38f4336ab12b01e0021f337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841451"
---
# <span data-ttu-id="4032b-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4032b-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="4032b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4032b-102">SYNOPSIS</span></span>
<span data-ttu-id="4032b-103">Erstellt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="4032b-103">Creates an application gateway.</span></span>

## <span data-ttu-id="4032b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4032b-104">SYNTAX</span></span>

```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-FrontendIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]>]
 -FrontendPorts <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]>
 [-Probes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]>]
 -BackendAddressPools <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>
 -BackendHttpSettingsCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]>
 -HttpListeners <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]>
 [-UrlPathMaps <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]>]
 -RequestRoutingRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]>
 [-RedirectConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4032b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4032b-105">DESCRIPTION</span></span>
<span data-ttu-id="4032b-106">Mit dem Cmdlet **New-AzApplicationGateway** wird ein Azure Application Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="4032b-106">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="4032b-107">Für ein Anwendungsgateway ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="4032b-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="4032b-108">Eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4032b-108">A resource group.</span></span>
- <span data-ttu-id="4032b-109">Ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4032b-109">A virtual network.</span></span>
- <span data-ttu-id="4032b-110">Ein Back-End-Serverpool mit den IP-Adressen der Back-End-Server.</span><span class="sxs-lookup"><span data-stu-id="4032b-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="4032b-111">Einstellungen für den Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="4032b-111">Back-end server pool settings.</span></span> <span data-ttu-id="4032b-112">Jeder Pool verfügt über Einstellungen wie Port-, Protokoll-und Cookie-basierter Affinität, die auf alle Server innerhalb des Pools angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="4032b-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="4032b-113">Front-End-IP-Adressen, bei denen es sich um die IP-Adressen handelt, die auf dem Anwendungsgateway geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="4032b-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="4032b-114">Eine Front-End-IP-Adresse kann eine öffentliche IP-Adresse oder eine interne IP-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="4032b-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="4032b-115">Front-End-Ports, bei denen es sich um öffentliche Ports handelt, die auf dem Anwendungsgateway geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="4032b-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="4032b-116">Datenverkehr, der auf diese Ports trifft, wird an die Back-End-Server umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4032b-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="4032b-117">Eine Anforderungs Routingregel, die den Listener und den Back-End-Serverpool bindet.</span><span class="sxs-lookup"><span data-stu-id="4032b-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="4032b-118">Die Regel definiert, an welchen Back-End-Serverpool der Datenverkehr weitergeleitet werden soll, wenn er auf einen bestimmten Listener trifft.</span><span class="sxs-lookup"><span data-stu-id="4032b-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="4032b-119">Ein Listener verfügt über einen Front-End-Port, eine Front-End-IP-Adresse, ein Protokoll (http oder HTTPS) und einen SSL-Zertifikatnamen (Secure Sockets Layer) (wenn die SSL-Verschiebung konfiguriert ist).</span><span class="sxs-lookup"><span data-stu-id="4032b-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="4032b-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4032b-120">EXAMPLES</span></span>

### <span data-ttu-id="4032b-121">Beispiel 1: Erstellen eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="4032b-121">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSetting -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="4032b-122">Im folgenden Beispiel wird ein Anwendungsgateway erstellt, indem zunächst eine Ressourcengruppe und ein virtuelles Netzwerk sowie die folgenden Schritte erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="4032b-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="4032b-123">Ein Back-End-Serverpool</span><span class="sxs-lookup"><span data-stu-id="4032b-123">A back-end server pool</span></span>
- <span data-ttu-id="4032b-124">Einstellungen für den Back-End-Serverpool</span><span class="sxs-lookup"><span data-stu-id="4032b-124">Back-end server pool settings</span></span>
- <span data-ttu-id="4032b-125">Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="4032b-125">Front-end ports</span></span>
- <span data-ttu-id="4032b-126">Front-End-IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="4032b-126">Front-end IP addresses</span></span>
- <span data-ttu-id="4032b-127">Eine Anforderungs Routingregel</span><span class="sxs-lookup"><span data-stu-id="4032b-127">A request routing rule</span></span>

<span data-ttu-id="4032b-128">Mit diesen vier Befehlen wird ein virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="4032b-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="4032b-129">Der erste Befehl erstellt eine Subnet-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4032b-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="4032b-130">Mit dem zweiten Befehl wird ein virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="4032b-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="4032b-131">Der dritte Befehl überprüft die Subnetz-Konfiguration, und der vierte Befehl überprüft, ob das virtuelle Netzwerk erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4032b-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="4032b-132">Mit den folgenden Befehlen wird das Anwendungsgateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="4032b-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="4032b-133">Der erste Befehl erstellt eine IP-Konfiguration mit dem Namen "GatewayIp01" für das zuvor erstellte Subnetz.</span><span class="sxs-lookup"><span data-stu-id="4032b-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="4032b-134">Der zweite Befehl erstellt einen Back-End-Serverpool mit dem Namen Pool01 mit einer Liste der Back-End-IP-Adressen und speichert den Pool in der $Pool-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4032b-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="4032b-135">Der dritte Befehl erstellt die Einstellungen für den Back-End-Serverpool und speichert die Einstellungen in der $PoolSetting-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4032b-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="4032b-136">Der Befehl Forth erstellt einen Front-End-Port auf Port 80, benennt ihn FrontEndPort01 und speichert den Port in der $FrontEndPort-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4032b-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="4032b-137">Der fünfte Befehl erstellt eine öffentliche IP-Adresse mithilfe von New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="4032b-137">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="4032b-138">Der sechste Befehl erstellt eine Front-End-IP-Konfiguration mit $PublicIp, benennt Sie FrontEndPortConfig01 und speichert Sie in der $FrontEndIpConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4032b-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="4032b-139">Der siebte Befehl erstellt einen Listener mithilfe der zuvor erstellten $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="4032b-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="4032b-140">Der achte Befehl erstellt eine Regel für den Listener.</span><span class="sxs-lookup"><span data-stu-id="4032b-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="4032b-141">Der neunte Befehl legt die SKU fest.</span><span class="sxs-lookup"><span data-stu-id="4032b-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="4032b-142">Der zehnte Befehl erstellt das Gateway unter Verwendung der Objekte, die von den vorherigen Befehlen gesetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="4032b-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="4032b-143">Parameter</span><span class="sxs-lookup"><span data-stu-id="4032b-143">PARAMETERS</span></span>

### <span data-ttu-id="4032b-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4032b-144">-AsJob</span></span>
<span data-ttu-id="4032b-145">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4032b-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4032b-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="4032b-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="4032b-147">Gibt Authentifizierungszertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="4032b-147">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4032b-148">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="4032b-148">-BackendAddressPools</span></span>
<span data-ttu-id="4032b-149">Gibt die Liste der Back-End-Adresspools für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="4032b-149">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4032b-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="4032b-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="4032b-151">Gibt die Liste der Back-End-HTTP-Einstellungen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="4032b-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4032b-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4032b-152">-DefaultProfile</span></span>
<span data-ttu-id="4032b-153">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4032b-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4032b-154">-Force</span><span class="sxs-lookup"><span data-stu-id="4032b-154">-Force</span></span>
<span data-ttu-id="4032b-155">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4032b-155">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4032b-156">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="4032b-156">-FrontendIPConfigurations</span></span>
<span data-ttu-id="4032b-157">Gibt eine Liste der Front-End-IP-Konfigurationen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="4032b-157">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4032b-158">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="4032b-158">-FrontendPorts</span></span>
<span data-ttu-id="4032b-159">Gibt eine Liste der Front-End-Ports für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="4032b-159">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4032b-160">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="4032b-160">-GatewayIPConfigurations</span></span>
<span data-ttu-id="4032b-161">Gibt eine Liste der IP-Konfigurationen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="4032b-161">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4032b-162">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="4032b-162">-HttpListeners</span></span>
<span data-ttu-id="4032b-163">Gibt eine Liste der HTTP-Listener für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="4032b-163">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4032b-164">-Standort</span><span class="sxs-lookup"><span data-stu-id="4032b-164">-Location</span></span>
<span data-ttu-id="4032b-165">Gibt den Bereich an, in dem das Anwendungsgateway erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4032b-165">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="4032b-166">-Name</span><span class="sxs-lookup"><span data-stu-id="4032b-166">-Name</span></span>
<span data-ttu-id="4032b-167">Gibt den Namen des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="4032b-167">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="4032b-168">-Sonden</span><span class="sxs-lookup"><span data-stu-id="4032b-168">-Probes</span></span>
<span data-ttu-id="4032b-169">Gibt Prüfpunkte für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="4032b-169">Specifies probes for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4032b-170">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="4032b-170">-RedirectConfigurations</span></span>
<span data-ttu-id="4032b-171">Die Liste der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="4032b-171">The list of redirect configuration</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4032b-172">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="4032b-172">-RequestRoutingRules</span></span>
<span data-ttu-id="4032b-173">Gibt eine Liste der Anforderungs Routingregeln für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="4032b-173">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4032b-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4032b-174">-ResourceGroupName</span></span>
<span data-ttu-id="4032b-175">Gibt den Namen der Ressourcengruppe an, in der das Anwendungsgateway erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4032b-175">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="4032b-176">-SKU</span><span class="sxs-lookup"><span data-stu-id="4032b-176">-Sku</span></span>
<span data-ttu-id="4032b-177">Gibt die Lagerhaltungs Einheit (SKU) des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="4032b-177">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="4032b-178">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="4032b-178">-SslCertificates</span></span>
<span data-ttu-id="4032b-179">Gibt die Liste der SSL-Zertifikate (Secure Sockets Layer) für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="4032b-179">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4032b-180">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="4032b-180">-SslPolicy</span></span>
<span data-ttu-id="4032b-181">Gibt eine SSL-Richtlinie für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="4032b-181">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="4032b-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="4032b-182">-Tag</span></span>
<span data-ttu-id="4032b-183">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="4032b-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4032b-184">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4032b-184">For example:</span></span>

<span data-ttu-id="4032b-185">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="4032b-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4032b-186">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="4032b-186">-UrlPathMaps</span></span>
<span data-ttu-id="4032b-187">Gibt URL-Pfad Zuordnungen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="4032b-187">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4032b-188">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4032b-188">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="4032b-189">Gibt eine WAF-Konfiguration (Web Application Firewall) an.</span><span class="sxs-lookup"><span data-stu-id="4032b-189">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="4032b-190">Sie können das Get-AzApplicationGatewayWebApplicationFirewallConfiguration-Cmdlet verwenden, um eine WAF abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4032b-190">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="4032b-191">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4032b-191">-Confirm</span></span>
<span data-ttu-id="4032b-192">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4032b-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4032b-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4032b-193">-WhatIf</span></span>
<span data-ttu-id="4032b-194">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4032b-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4032b-195">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4032b-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4032b-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4032b-196">CommonParameters</span></span>
<span data-ttu-id="4032b-197">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4032b-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4032b-198">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4032b-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4032b-199">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4032b-199">INPUTS</span></span>

## <span data-ttu-id="4032b-200">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4032b-200">OUTPUTS</span></span>

### <span data-ttu-id="4032b-201">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4032b-201">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4032b-202">Notizen</span><span class="sxs-lookup"><span data-stu-id="4032b-202">NOTES</span></span>

## <span data-ttu-id="4032b-203">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4032b-203">RELATED LINKS</span></span>

[<span data-ttu-id="4032b-204">Neu – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4032b-204">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4032b-205">Neu – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4032b-205">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="4032b-206">Neu – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4032b-206">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4032b-207">Neu – AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4032b-207">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4032b-208">Neu – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4032b-208">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4032b-209">Neu – AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4032b-209">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4032b-210">Neu – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4032b-210">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4032b-211">Neu – AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="4032b-211">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="4032b-212">Neu – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4032b-212">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="4032b-213">Neu – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4032b-213">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
