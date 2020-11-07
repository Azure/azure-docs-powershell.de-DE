---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: b6a7854d3ddf3c3d444418e08717577a8a2ac172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663307"
---
# <span data-ttu-id="2b433-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b433-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="2b433-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b433-102">SYNOPSIS</span></span>
<span data-ttu-id="2b433-103">Erstellt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="2b433-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b433-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b433-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
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
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b433-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b433-105">DESCRIPTION</span></span>
<span data-ttu-id="2b433-106">Mit dem Cmdlet **New-AzureRmApplicationGateway** wird ein Azure Application Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="2b433-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="2b433-107">Für ein Anwendungsgateway ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="2b433-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="2b433-108">Eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2b433-108">A resource group.</span></span>
- <span data-ttu-id="2b433-109">Ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2b433-109">A virtual network.</span></span>
- <span data-ttu-id="2b433-110">Ein Back-End-Serverpool mit den IP-Adressen der Back-End-Server.</span><span class="sxs-lookup"><span data-stu-id="2b433-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="2b433-111">Einstellungen für den Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="2b433-111">Back-end server pool settings.</span></span> <span data-ttu-id="2b433-112">Jeder Pool verfügt über Einstellungen wie Port-, Protokoll-und Cookie-basierter Affinität, die auf alle Server innerhalb des Pools angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b433-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="2b433-113">Front-End-IP-Adressen, bei denen es sich um die IP-Adressen handelt, die auf dem Anwendungsgateway geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="2b433-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="2b433-114">Eine Front-End-IP-Adresse kann eine öffentliche IP-Adresse oder eine interne IP-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="2b433-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="2b433-115">Front-End-Ports, bei denen es sich um öffentliche Ports handelt, die auf dem Anwendungsgateway geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="2b433-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="2b433-116">Datenverkehr, der auf diese Ports trifft, wird an die Back-End-Server umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2b433-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="2b433-117">Eine Anforderungs Routingregel, die den Listener und den Back-End-Serverpool bindet.</span><span class="sxs-lookup"><span data-stu-id="2b433-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="2b433-118">Die Regel definiert, an welchen Back-End-Serverpool der Datenverkehr weitergeleitet werden soll, wenn er auf einen bestimmten Listener trifft.</span><span class="sxs-lookup"><span data-stu-id="2b433-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="2b433-119">Ein Listener verfügt über einen Front-End-Port, eine Front-End-IP-Adresse, ein Protokoll (http oder HTTPS) und einen SSL-Zertifikatnamen (Secure Sockets Layer) (wenn die SSL-Verschiebung konfiguriert ist).</span><span class="sxs-lookup"><span data-stu-id="2b433-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="2b433-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b433-120">EXAMPLES</span></span>

### <span data-ttu-id="2b433-121">Beispiel 1: Erstellen eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="2b433-121">Example 1: Create an application gateway</span></span>
```
PS C:\>$ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} PS C:\>$Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet PS C:\>$GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name $PublicIpName -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name $listenerName  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $ FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="2b433-122">Im folgenden Beispiel wird ein Anwendungsgateway erstellt, indem zunächst eine Ressourcengruppe und ein virtuelles Netzwerk sowie die folgenden Schritte erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="2b433-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="2b433-123">Ein Back-End-Serverpool</span><span class="sxs-lookup"><span data-stu-id="2b433-123">A back-end server pool</span></span>
- <span data-ttu-id="2b433-124">Einstellungen für den Back-End-Serverpool</span><span class="sxs-lookup"><span data-stu-id="2b433-124">Back-end server pool settings</span></span>
- <span data-ttu-id="2b433-125">Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="2b433-125">Front-end ports</span></span>
- <span data-ttu-id="2b433-126">Front-End-IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="2b433-126">Front-end IP addresses</span></span>
- <span data-ttu-id="2b433-127">Eine Anforderungs Routingregel</span><span class="sxs-lookup"><span data-stu-id="2b433-127">A request routing rule</span></span>

<span data-ttu-id="2b433-128">Mit diesen vier Befehlen wird ein virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="2b433-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="2b433-129">Der erste Befehl erstellt eine Subnet-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2b433-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="2b433-130">Mit dem zweiten Befehl wird ein virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="2b433-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="2b433-131">Der dritte Befehl überprüft die Subnetz-Konfiguration, und der vierte Befehl überprüft, ob das virtuelle Netzwerk erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2b433-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="2b433-132">Mit den folgenden Befehlen wird das Anwendungsgateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="2b433-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="2b433-133">Der erste Befehl erstellt eine IP-Konfiguration mit dem Namen "GatewayIp01" für das zuvor erstellte Subnetz.</span><span class="sxs-lookup"><span data-stu-id="2b433-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="2b433-134">Der zweite Befehl erstellt einen Back-End-Serverpool mit dem Namen Pool01 mit einer Liste der Back-End-IP-Adressen und speichert den Pool in der $Pool-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2b433-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="2b433-135">Der dritte Befehl erstellt die Einstellungen für den Back-End-Serverpool und speichert die Einstellungen in der $PoolSetting-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2b433-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="2b433-136">Der Befehl Forth erstellt einen Front-End-Port auf Port 80, benennt ihn FrontEndPort01 und speichert den Port in der $FrontEndPort-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2b433-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="2b433-137">Der fünfte Befehl erstellt eine öffentliche IP-Adresse mithilfe von New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="2b433-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="2b433-138">Der sechste Befehl erstellt eine Front-End-IP-Konfiguration mit $PublicIp, benennt Sie FrontEndPortConfig01 und speichert Sie in der $FrontEndIpConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2b433-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="2b433-139">Der siebte Befehl erstellt einen Listener mithilfe der zuvor erstellten $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="2b433-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="2b433-140">Der achte Befehl erstellt eine Regel für den Listener.</span><span class="sxs-lookup"><span data-stu-id="2b433-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="2b433-141">Der neunte Befehl legt die SKU fest.</span><span class="sxs-lookup"><span data-stu-id="2b433-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="2b433-142">Der zehnte Befehl erstellt das Gateway unter Verwendung der Objekte, die von den vorherigen Befehlen gesetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="2b433-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="2b433-143">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b433-143">PARAMETERS</span></span>

### <span data-ttu-id="2b433-144">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="2b433-144">-AuthenticationCertificates</span></span>
<span data-ttu-id="2b433-145">Gibt Authentifizierungszertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="2b433-145">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="2b433-146">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="2b433-146">-BackendAddressPools</span></span>
<span data-ttu-id="2b433-147">Gibt die Liste der Back-End-Adresspools für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="2b433-147">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="2b433-148">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="2b433-148">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="2b433-149">Gibt die Liste der Back-End-HTTP-Einstellungen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="2b433-149">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="2b433-150">-Force</span><span class="sxs-lookup"><span data-stu-id="2b433-150">-Force</span></span>
<span data-ttu-id="2b433-151">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2b433-151">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2b433-152">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="2b433-152">-FrontendIPConfigurations</span></span>
<span data-ttu-id="2b433-153">Gibt eine Liste der Front-End-IP-Konfigurationen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="2b433-153">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="2b433-154">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="2b433-154">-FrontendPorts</span></span>
<span data-ttu-id="2b433-155">Gibt eine Liste der Front-End-Ports für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="2b433-155">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="2b433-156">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="2b433-156">-GatewayIPConfigurations</span></span>
<span data-ttu-id="2b433-157">Gibt eine Liste der IP-Konfigurationen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="2b433-157">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="2b433-158">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="2b433-158">-HttpListeners</span></span>
<span data-ttu-id="2b433-159">Gibt eine Liste der HTTP-Listener für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="2b433-159">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="2b433-160">-Standort</span><span class="sxs-lookup"><span data-stu-id="2b433-160">-Location</span></span>
<span data-ttu-id="2b433-161">Gibt den Bereich an, in dem das Anwendungsgateway erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b433-161">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="2b433-162">-Name</span><span class="sxs-lookup"><span data-stu-id="2b433-162">-Name</span></span>
<span data-ttu-id="2b433-163">Gibt den Namen des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="2b433-163">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="2b433-164">-Sonden</span><span class="sxs-lookup"><span data-stu-id="2b433-164">-Probes</span></span>
<span data-ttu-id="2b433-165">Gibt Prüfpunkte für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="2b433-165">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="2b433-166">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="2b433-166">-RedirectConfigurations</span></span>
<span data-ttu-id="2b433-167">Die Liste der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="2b433-167">The list of redirect configuration</span></span>

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

### <span data-ttu-id="2b433-168">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="2b433-168">-RequestRoutingRules</span></span>
<span data-ttu-id="2b433-169">Gibt eine Liste der Anforderungs Routingregeln für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="2b433-169">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="2b433-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b433-170">-ResourceGroupName</span></span>
<span data-ttu-id="2b433-171">Gibt den Namen der Ressourcengruppe an, in der das Anwendungsgateway erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b433-171">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="2b433-172">-SKU</span><span class="sxs-lookup"><span data-stu-id="2b433-172">-Sku</span></span>
<span data-ttu-id="2b433-173">Gibt die Lagerhaltungs Einheit (SKU) des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="2b433-173">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="2b433-174">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="2b433-174">-SslCertificates</span></span>
<span data-ttu-id="2b433-175">Gibt die Liste der SSL-Zertifikate (Secure Sockets Layer) für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="2b433-175">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="2b433-176">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="2b433-176">-SslPolicy</span></span>
<span data-ttu-id="2b433-177">Gibt eine SSL-Richtlinie für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="2b433-177">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="2b433-178">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b433-178">-Tag</span></span>
<span data-ttu-id="2b433-179">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="2b433-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2b433-180">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2b433-180">For example:</span></span>

<span data-ttu-id="2b433-181">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="2b433-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2b433-182">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="2b433-182">-UrlPathMaps</span></span>
<span data-ttu-id="2b433-183">Gibt URL-Pfad Zuordnungen für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="2b433-183">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="2b433-184">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b433-184">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="2b433-185">Gibt eine WAF-Konfiguration (Web Application Firewall) an.</span><span class="sxs-lookup"><span data-stu-id="2b433-185">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="2b433-186">Sie können das Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration-Cmdlet verwenden, um eine WAF abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2b433-186">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="2b433-187">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b433-187">-Confirm</span></span>
<span data-ttu-id="2b433-188">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b433-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b433-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b433-189">-WhatIf</span></span>
<span data-ttu-id="2b433-190">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b433-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b433-191">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b433-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b433-192">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b433-192">-DefaultProfile</span></span>
<span data-ttu-id="2b433-193">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2b433-193">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b433-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b433-194">CommonParameters</span></span>
<span data-ttu-id="2b433-195">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b433-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b433-196">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b433-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b433-197">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b433-197">INPUTS</span></span>

## <span data-ttu-id="2b433-198">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b433-198">OUTPUTS</span></span>

### <span data-ttu-id="2b433-199">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b433-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2b433-200">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b433-200">NOTES</span></span>

## <span data-ttu-id="2b433-201">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b433-201">RELATED LINKS</span></span>

[<span data-ttu-id="2b433-202">Neu – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2b433-202">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="2b433-203">Neu – AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2b433-203">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="2b433-204">Neu – AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2b433-204">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2b433-205">Neu – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2b433-205">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2b433-206">Neu – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="2b433-206">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="2b433-207">Neu – AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b433-207">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2b433-208">Neu – AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2b433-208">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2b433-209">Neu – AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="2b433-209">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="2b433-210">Neu – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2b433-210">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2b433-211">Neu – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2b433-211">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
