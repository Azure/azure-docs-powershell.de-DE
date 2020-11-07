---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 6576cedfa49d2ba2215d72b7f31ea85288f5cbda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660168"
---
# <span data-ttu-id="d8ae2-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d8ae2-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="d8ae2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ae2-103">Aktualisiert ein virtuelles Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="d8ae2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8ae2-104">SYNTAX</span></span>

### <span data-ttu-id="d8ae2-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8ae2-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8ae2-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8ae2-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8ae2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8ae2-107">DESCRIPTION</span></span>
<span data-ttu-id="d8ae2-108">Das Cmdlet " **Satz-AzVirtualNetworkGateway** " aktualisiert ein virtuelles Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-108">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="d8ae2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8ae2-109">EXAMPLES</span></span>

### <span data-ttu-id="d8ae2-110">Beispiel 1: Aktualisieren des ASN eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="d8ae2-110">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="d8ae2-111">Der erste Befehl ruft ein virtuelles Netzwerkgateway mit dem Namen Gateway01 ab, das zu Ressourcengruppen-ResourceGroup001 gehört, und speichert es in der Variablen mit dem Namen $Gateway der zweite Befehl das virtuelle Netzwerkgateway aktualisiert, das in Variablen $Gateway gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="d8ae2-112">Der Befehl legt auch die ASN auf 1337 fest.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="d8ae2-113">Beispiel 2: Hinzufügen einer IPSec-Richtlinie zu einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="d8ae2-113">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="d8ae2-114">Der erste Befehl ruft ein virtuelles Netzwerkgateway mit dem Namen Gateway01 ab, das zu Ressourcengruppen-ResourceGroup001 gehört, und speichert es in der Variablen mit dem Namen $Gateway der zweite Befehl das VPN-IPSec-Richtlinienobjekt als pro angegebene IPSec-Parameter erstellt.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="d8ae2-115">Der dritte Befehl aktualisiert das virtuelle Netzwerkgateway, das in Variablen $Gateway gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-115">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="d8ae2-116">Der Befehl legt auch die benutzerdefinierte VPN-IPSec-Richtlinie fest, die im $vpnclientipsecpolicy-Objekt auf dem virtuellen Netzwerkgateway angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="d8ae2-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8ae2-117">PARAMETERS</span></span>

### <span data-ttu-id="d8ae2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8ae2-118">-AsJob</span></span>
<span data-ttu-id="d8ae2-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d8ae2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8ae2-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="d8ae2-120">-Asn</span></span>
<span data-ttu-id="d8ae2-121">Gibt den virtuellen Netzwerkgateway (autonome System Nummer) an, der zum Einrichten von BGP-Sitzungen (Border Gateway Protocol) innerhalb von IPSec-Tunneln verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ae2-122">-DefaultProfile</span></span>
<span data-ttu-id="d8ae2-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8ae2-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="d8ae2-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="d8ae2-125">Deaktiviert das Active-Active-Feature.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="d8ae2-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="d8ae2-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="d8ae2-127">Aktiviert das Active-Active-Feature.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="d8ae2-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d8ae2-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="d8ae2-129">Gibt die Standardwebsite an, die für das Erzwingen des Tunnelns verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="d8ae2-130">Wenn eine Standardwebsite angegeben wird, wird der gesamte Internetdatenverkehr vom VPN (virtuelles privates Netzwerk) des Gateways an diese Website weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="d8ae2-131">-GatewaySku</span></span>
<span data-ttu-id="d8ae2-132">Gibt die Lagerhaltungs Einheit (SKU) des virtuellen Netzwerkgateways an.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="d8ae2-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d8ae2-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8ae2-134">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="d8ae2-134">Basic</span></span>
- <span data-ttu-id="d8ae2-135">Standard</span><span class="sxs-lookup"><span data-stu-id="d8ae2-135">Standard</span></span>
- <span data-ttu-id="d8ae2-136">Hochleistungs</span><span class="sxs-lookup"><span data-stu-id="d8ae2-136">HighPerformance</span></span>
- <span data-ttu-id="d8ae2-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="d8ae2-137">VpnGw1</span></span>
- <span data-ttu-id="d8ae2-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="d8ae2-138">VpnGw2</span></span>
- <span data-ttu-id="d8ae2-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="d8ae2-139">VpnGw3</span></span>
- <span data-ttu-id="d8ae2-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="d8ae2-140">VpnGw1AZ</span></span>
- <span data-ttu-id="d8ae2-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="d8ae2-141">VpnGw2AZ</span></span>
- <span data-ttu-id="d8ae2-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="d8ae2-142">VpnGw3AZ</span></span>
- <span data-ttu-id="d8ae2-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="d8ae2-143">ErGw1AZ</span></span>
- <span data-ttu-id="d8ae2-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="d8ae2-144">ErGw2AZ</span></span>
- <span data-ttu-id="d8ae2-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="d8ae2-145">ErGw3AZ</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="d8ae2-146">-PeerWeight</span></span>
<span data-ttu-id="d8ae2-147">Gibt die Gewichtung von Routen an, die über BGP von diesem virtuellen Netzwerkgateway gelernt wurden.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="d8ae2-148">-RadiusServerAddress</span></span>
<span data-ttu-id="d8ae2-149">P2S-externe RADIUS-Serveradresse.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-149">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="d8ae2-150">-RadiusServerSecret</span></span>
<span data-ttu-id="d8ae2-151">P2S externer RADIUS-Server-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-151">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d8ae2-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d8ae2-153">Gibt das virtuelles Netzwerkgateway-Objekt an, auf dem Änderungen basieren sollen.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="d8ae2-154">Sie können das Get-AzVirtualNetworkGateway-Cmdlet verwenden, um das Virtual Network Gateway-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-154">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="d8ae2-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="d8ae2-156">Gibt den Adressraum an, von dem dieses Cmdlet für die Zuweisung von VPN-Client-IP-Adressen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="d8ae2-157">Dies sollte sich nicht mit virtuellen Netzwerken oder lokalen Bereichen überlappen.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-157">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ae2-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="d8ae2-159">Eine Liste der IPSec-Richtlinien für P2S-VPN-Client Tunneling-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="d8ae2-160">-VpnClientProtocol</span></span>
<span data-ttu-id="d8ae2-161">Eine Liste der P2S-VPN-Client Tunneling-Protokolle</span><span class="sxs-lookup"><span data-stu-id="d8ae2-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="d8ae2-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="d8ae2-163">Gibt eine Liste der gesperrten VPN-Clientzertifikate an.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="d8ae2-164">Ein VPN-Client mit einem Zertifikat, das einem dieser Zertifikate entspricht, wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="d8ae2-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="d8ae2-166">Gibt eine Liste der VPN-Client Stammzertifikate an, die für die VPN-Clientauthentifizierung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="d8ae2-167">Beim Verbinden von VPN-Clients müssen Zertifikate vorhanden sein, die aus einem dieser Stammzertifikate generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d8ae2-168">-Confirm</span></span>
<span data-ttu-id="d8ae2-169">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8ae2-170">-WhatIf</span></span>
<span data-ttu-id="d8ae2-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8ae2-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-172">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ae2-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ae2-173">CommonParameters</span></span>
<span data-ttu-id="d8ae2-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ae2-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ae2-175">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8ae2-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ae2-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8ae2-176">INPUTS</span></span>

### <span data-ttu-id="d8ae2-177">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d8ae2-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="d8ae2-178">System. String</span><span class="sxs-lookup"><span data-stu-id="d8ae2-178">System.String</span></span>

### <span data-ttu-id="d8ae2-179">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d8ae2-179">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="d8ae2-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="d8ae2-180">System.String[]</span></span>

### <span data-ttu-id="d8ae2-181">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="d8ae2-181">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="d8ae2-182">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="d8ae2-182">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="d8ae2-183">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="d8ae2-183">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="d8ae2-184">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="d8ae2-184">System.UInt32</span></span>

### <span data-ttu-id="d8ae2-185">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d8ae2-185">System.Int32</span></span>

### <span data-ttu-id="d8ae2-186">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="d8ae2-186">System.Security.SecureString</span></span>

## <span data-ttu-id="d8ae2-187">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8ae2-187">OUTPUTS</span></span>

### <span data-ttu-id="d8ae2-188">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d8ae2-188">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d8ae2-189">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8ae2-189">NOTES</span></span>
* <span data-ttu-id="d8ae2-190">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="d8ae2-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d8ae2-191">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8ae2-191">RELATED LINKS</span></span>

[<span data-ttu-id="d8ae2-192">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d8ae2-192">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d8ae2-193">Neu – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d8ae2-193">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d8ae2-194">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d8ae2-194">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d8ae2-195">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d8ae2-195">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d8ae2-196">Größe ändern – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d8ae2-196">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
