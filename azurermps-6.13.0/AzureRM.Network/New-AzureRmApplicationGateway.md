---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: 67da94a783d932501413008523c744f6695f6024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482317"
---
# <span data-ttu-id="16d22-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16d22-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="16d22-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16d22-102">SYNOPSIS</span></span>
<span data-ttu-id="16d22-103">Erstellt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="16d22-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16d22-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16d22-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
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
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16d22-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16d22-105">DESCRIPTION</span></span>
<span data-ttu-id="16d22-106">Mit dem Cmdlet **New-AzureRmApplicationGateway** wird ein Azure Application Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="16d22-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="16d22-107">Für ein Anwendungsgateway ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="16d22-107">An application gateway requires the following:</span></span>
- <span data-ttu-id="16d22-108">Eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="16d22-108">A resource group.</span></span>
- <span data-ttu-id="16d22-109">Ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="16d22-109">A virtual network.</span></span>
- <span data-ttu-id="16d22-110">Ein Back-End-Serverpool mit den IP-Adressen der Back-End-Server.</span><span class="sxs-lookup"><span data-stu-id="16d22-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="16d22-111">Einstellungen für den Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="16d22-111">Back-end server pool settings.</span></span> <span data-ttu-id="16d22-112">Jeder Pool verfügt über Einstellungen wie Port-, Protokoll-und Cookie-basierter Affinität, die auf alle Server innerhalb des Pools angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="16d22-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="16d22-113">Front-End-IP-Adressen, bei denen es sich um die IP-Adressen handelt, die auf dem Anwendungsgateway geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="16d22-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="16d22-114">Eine Front-End-IP-Adresse kann eine öffentliche IP-Adresse oder eine interne IP-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="16d22-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="16d22-115">Front-End-Ports, bei denen es sich um öffentliche Ports handelt, die auf dem Anwendungsgateway geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="16d22-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="16d22-116">Datenverkehr, der auf diese Ports trifft, wird an die Back-End-Server umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="16d22-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="16d22-117">Eine Anforderungs Routingregel, die den Listener und den Back-End-Serverpool bindet.</span><span class="sxs-lookup"><span data-stu-id="16d22-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="16d22-118">Die Regel definiert, an welchen Back-End-Serverpool der Datenverkehr weitergeleitet werden soll, wenn er auf einen bestimmten Listener trifft.</span><span class="sxs-lookup"><span data-stu-id="16d22-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="16d22-119">Ein Listener verfügt über einen Front-End-Port, eine Front-End-IP-Adresse, ein Protokoll (http oder HTTPS) und einen SSL-Zertifikatnamen (Secure Sockets Layer) (wenn die SSL-Verschiebung konfiguriert ist).</span><span class="sxs-lookup"><span data-stu-id="16d22-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="16d22-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16d22-120">EXAMPLES</span></span>

### <span data-ttu-id="16d22-121">Beispiel 1: Erstellen eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="16d22-121">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="16d22-122">Im folgenden Beispiel wird ein Anwendungsgateway erstellt, indem zunächst eine Ressourcengruppe und ein virtuelles Netzwerk sowie die folgenden Schritte erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="16d22-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="16d22-123">Ein Back-End-Serverpool</span><span class="sxs-lookup"><span data-stu-id="16d22-123">A back-end server pool</span></span>
- <span data-ttu-id="16d22-124">Einstellungen für den Back-End-Serverpool</span><span class="sxs-lookup"><span data-stu-id="16d22-124">Back-end server pool settings</span></span>
- <span data-ttu-id="16d22-125">Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="16d22-125">Front-end ports</span></span>
- <span data-ttu-id="16d22-126">Front-End-IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="16d22-126">Front-end IP addresses</span></span>
- <span data-ttu-id="16d22-127">Eine Anforderungs Routingregel mit diesen vier Befehlen wird ein virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="16d22-127">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="16d22-128">Der erste Befehl erstellt eine Subnet-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="16d22-128">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="16d22-129">Mit dem zweiten Befehl wird ein virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="16d22-129">The second command creates a virtual network.</span></span>
<span data-ttu-id="16d22-130">Der dritte Befehl überprüft die Subnetz-Konfiguration, und der vierte Befehl überprüft, ob das virtuelle Netzwerk erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="16d22-130">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="16d22-131">Mit den folgenden Befehlen wird das Anwendungsgateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="16d22-131">The following commands create the application gateway.</span></span>
<span data-ttu-id="16d22-132">Der erste Befehl erstellt eine IP-Konfiguration mit dem Namen "GatewayIp01" für das zuvor erstellte Subnetz.</span><span class="sxs-lookup"><span data-stu-id="16d22-132">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="16d22-133">Der zweite Befehl erstellt einen Back-End-Serverpool mit dem Namen Pool01 mit einer Liste der Back-End-IP-Adressen und speichert den Pool in der $Pool-Variablen.</span><span class="sxs-lookup"><span data-stu-id="16d22-133">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="16d22-134">Der dritte Befehl erstellt die Einstellungen für den Back-End-Serverpool und speichert die Einstellungen in der $PoolSetting-Variablen.</span><span class="sxs-lookup"><span data-stu-id="16d22-134">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="16d22-135">Der Befehl Forth erstellt einen Front-End-Port auf Port 80, benennt ihn FrontEndPort01 und speichert den Port in der $FrontEndPort-Variablen.</span><span class="sxs-lookup"><span data-stu-id="16d22-135">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="16d22-136">Der fünfte Befehl erstellt eine öffentliche IP-Adresse mithilfe von New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="16d22-136">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="16d22-137">Der sechste Befehl erstellt eine Front-End-IP-Konfiguration mit $PublicIp, benennt Sie FrontEndPortConfig01 und speichert Sie in der $FrontEndIpConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="16d22-137">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="16d22-138">Der siebte Befehl erstellt einen Listener mithilfe der zuvor erstellten $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="16d22-138">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="16d22-139">Der achte Befehl erstellt eine Regel für den Listener.</span><span class="sxs-lookup"><span data-stu-id="16d22-139">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="16d22-140">Der neunte Befehl legt die SKU fest.</span><span class="sxs-lookup"><span data-stu-id="16d22-140">The ninth command sets the SKU.</span></span>
<span data-ttu-id="16d22-141">Der zehnte Befehl erstellt das Gateway unter Verwendung der Objekte, die von den vorherigen Befehlen gesetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="16d22-141">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="16d22-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="16d22-142">PARAMETERS</span></span>

### <span data-ttu-id="16d22-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16d22-143">-AsJob</span></span>
<span data-ttu-id="16d22-144">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="16d22-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16d22-145">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="16d22-145">-AuthenticationCertificates</span></span>
<span data-ttu-id="16d22-146">Gibt Authentifizierungszertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="16d22-146">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="16d22-147">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="16d22-147">-AutoscaleConfiguration</span></span>
<span data-ttu-id="16d22-148">AutoScale-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="16d22-148">Autoscale Configuration</span></span>

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

### <span data-ttu-id="16d22-149">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="16d22-149">-BackendAddressPools</span></span>
<span data-ttu-id="16d22-150">Gibt die Liste der Back-End-Adresspools für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="16d22-150">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="16d22-151">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="16d22-151">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="16d22-152">Gibt die Liste der Back-End-HTTP-Einstellungen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="16d22-152">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="16d22-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d22-153">-DefaultProfile</span></span>
<span data-ttu-id="16d22-154">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16d22-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16d22-155">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="16d22-155">-EnableFIPS</span></span>
<span data-ttu-id="16d22-156">Gibt an, ob FIPS aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="16d22-156">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="16d22-157">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="16d22-157">-EnableHttp2</span></span>
<span data-ttu-id="16d22-158">Gibt an, ob HTTP2 aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="16d22-158">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="16d22-159">-Force</span><span class="sxs-lookup"><span data-stu-id="16d22-159">-Force</span></span>
<span data-ttu-id="16d22-160">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="16d22-160">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="16d22-161">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="16d22-161">-FrontendIPConfigurations</span></span>
<span data-ttu-id="16d22-162">Gibt eine Liste der Front-End-IP-Konfigurationen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="16d22-162">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="16d22-163">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="16d22-163">-FrontendPorts</span></span>
<span data-ttu-id="16d22-164">Gibt eine Liste der Front-End-Ports für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="16d22-164">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="16d22-165">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="16d22-165">-GatewayIPConfigurations</span></span>
<span data-ttu-id="16d22-166">Gibt eine Liste der IP-Konfigurationen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="16d22-166">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="16d22-167">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="16d22-167">-HttpListeners</span></span>
<span data-ttu-id="16d22-168">Gibt eine Liste der HTTP-Listener für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="16d22-168">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="16d22-169">-Standort</span><span class="sxs-lookup"><span data-stu-id="16d22-169">-Location</span></span>
<span data-ttu-id="16d22-170">Gibt den Bereich an, in dem das Anwendungsgateway erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="16d22-170">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="16d22-171">-Name</span><span class="sxs-lookup"><span data-stu-id="16d22-171">-Name</span></span>
<span data-ttu-id="16d22-172">Gibt den Namen des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="16d22-172">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="16d22-173">-Sonden</span><span class="sxs-lookup"><span data-stu-id="16d22-173">-Probes</span></span>
<span data-ttu-id="16d22-174">Gibt Prüfpunkte für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="16d22-174">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="16d22-175">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="16d22-175">-RedirectConfigurations</span></span>
<span data-ttu-id="16d22-176">Die Liste der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="16d22-176">The list of redirect configuration</span></span>

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

### <span data-ttu-id="16d22-177">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="16d22-177">-RequestRoutingRules</span></span>
<span data-ttu-id="16d22-178">Gibt eine Liste der Anforderungs Routingregeln für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="16d22-178">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="16d22-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16d22-179">-ResourceGroupName</span></span>
<span data-ttu-id="16d22-180">Gibt den Namen der Ressourcengruppe an, in der das Anwendungsgateway erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="16d22-180">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="16d22-181">-SKU</span><span class="sxs-lookup"><span data-stu-id="16d22-181">-Sku</span></span>
<span data-ttu-id="16d22-182">Gibt die Lagerhaltungs Einheit (SKU) des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="16d22-182">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="16d22-183">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="16d22-183">-SslCertificates</span></span>
<span data-ttu-id="16d22-184">Gibt die Liste der SSL-Zertifikate (Secure Sockets Layer) für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="16d22-184">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="16d22-185">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="16d22-185">-SslPolicy</span></span>
<span data-ttu-id="16d22-186">Gibt eine SSL-Richtlinie für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="16d22-186">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="16d22-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="16d22-187">-Tag</span></span>
<span data-ttu-id="16d22-188">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="16d22-188">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="16d22-189">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="16d22-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="16d22-190">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="16d22-190">-TrustedRootCertificate</span></span>
<span data-ttu-id="16d22-191">Liste der vertrauenswürdigen Stammzertifikate</span><span class="sxs-lookup"><span data-stu-id="16d22-191">The list of trusted root certificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d22-192">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="16d22-192">-UrlPathMaps</span></span>
<span data-ttu-id="16d22-193">Gibt URL-Pfad Zuordnungen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="16d22-193">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="16d22-194">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="16d22-194">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="16d22-195">Gibt eine WAF-Konfiguration (Web Application Firewall) an.</span><span class="sxs-lookup"><span data-stu-id="16d22-195">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="16d22-196">Sie können das Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration-Cmdlet verwenden, um eine WAF abzurufen.</span><span class="sxs-lookup"><span data-stu-id="16d22-196">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="16d22-197">-Zone</span><span class="sxs-lookup"><span data-stu-id="16d22-197">-Zone</span></span>
<span data-ttu-id="16d22-198">Eine Liste der Verfügbarkeits Zonen, die angibt, woher das Anwendungsgateway stammen muss.</span><span class="sxs-lookup"><span data-stu-id="16d22-198">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d22-199">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16d22-199">-Confirm</span></span>
<span data-ttu-id="16d22-200">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16d22-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16d22-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16d22-201">-WhatIf</span></span>
<span data-ttu-id="16d22-202">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16d22-202">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16d22-203">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16d22-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16d22-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d22-204">CommonParameters</span></span>
<span data-ttu-id="16d22-205">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16d22-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d22-206">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16d22-206">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d22-207">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16d22-207">INPUTS</span></span>

### <span data-ttu-id="16d22-208">System. String</span><span class="sxs-lookup"><span data-stu-id="16d22-208">System.String</span></span>

### <span data-ttu-id="16d22-209">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="16d22-209">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="16d22-210">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="16d22-210">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="16d22-211">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16d22-211">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16d22-212">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16d22-212">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16d22-213">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16d22-213">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16d22-214">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16d22-214">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16d22-215">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16d22-215">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16d22-216">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16d22-216">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16d22-217">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16d22-217">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16d22-218">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16d22-218">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16d22-219">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16d22-219">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16d22-220">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16d22-220">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16d22-221">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16d22-221">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16d22-222">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16d22-222">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16d22-223">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="16d22-223">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="16d22-224">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="16d22-224">System.Collections.Hashtable</span></span>

## <span data-ttu-id="16d22-225">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16d22-225">OUTPUTS</span></span>

### <span data-ttu-id="16d22-226">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16d22-226">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16d22-227">Notizen</span><span class="sxs-lookup"><span data-stu-id="16d22-227">NOTES</span></span>

## <span data-ttu-id="16d22-228">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16d22-228">RELATED LINKS</span></span>

[<span data-ttu-id="16d22-229">Neu – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="16d22-229">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="16d22-230">Neu – AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="16d22-230">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="16d22-231">Neu – AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="16d22-231">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="16d22-232">Neu – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="16d22-232">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="16d22-233">Neu – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="16d22-233">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="16d22-234">Neu – AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="16d22-234">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="16d22-235">Neu – AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="16d22-235">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="16d22-236">Neu – AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="16d22-236">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="16d22-237">Neu – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="16d22-237">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="16d22-238">Neu – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="16d22-238">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
