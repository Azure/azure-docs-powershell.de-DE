---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 41c94d0dd8401399f360af89f1744cc10e900e1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497037"
---
# <span data-ttu-id="31651-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31651-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="31651-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31651-102">SYNOPSIS</span></span>
<span data-ttu-id="31651-103">Aktualisiert ein virtuelles Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="31651-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31651-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31651-104">SYNTAX</span></span>

### <span data-ttu-id="31651-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="31651-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31651-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="31651-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31651-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31651-107">DESCRIPTION</span></span>
<span data-ttu-id="31651-108">Das Cmdlet " **Satz-AzureRmVirtualNetworkGateway** " aktualisiert ein virtuelles Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="31651-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="31651-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31651-109">EXAMPLES</span></span>

### <span data-ttu-id="31651-110">Beispiel 1: Einrichten des Zielzustands eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="31651-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="31651-111">Der erste Befehl ruft ein virtuelles Netzwerkgateway mit dem Namen Gateway01 ab, das zu Ressourcengruppen-ResourceGroup001 gehört, und speichert es in der Variablen mit dem Namen $Gateway</span><span class="sxs-lookup"><span data-stu-id="31651-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="31651-112">Der zweite Befehl legt den Zielstatus für das virtuelle Netzwerkgateway fest, das in Variablen $Gateway gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="31651-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="31651-113">Der Befehl legt auch die ASN auf 1337 fest.</span><span class="sxs-lookup"><span data-stu-id="31651-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="31651-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="31651-114">PARAMETERS</span></span>

### <span data-ttu-id="31651-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="31651-115">-Asn</span></span>
<span data-ttu-id="31651-116">Gibt den virtuellen Netzwerkgateway (autonome System Nummer) an, der zum Einrichten von BGP-Sitzungen (Border Gateway Protocol) innerhalb von IPSec-Tunneln verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31651-116">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="31651-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31651-117">-DefaultProfile</span></span>
<span data-ttu-id="31651-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31651-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="31651-119">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="31651-119">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="31651-120">Deaktiviert das Active-Active-Feature.</span><span class="sxs-lookup"><span data-stu-id="31651-120">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="31651-121">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="31651-121">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="31651-122">Aktiviert das Active-Active-Feature.</span><span class="sxs-lookup"><span data-stu-id="31651-122">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="31651-123">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="31651-123">-GatewayDefaultSite</span></span>
<span data-ttu-id="31651-124">Gibt die Standardwebsite an, die für das Erzwingen des Tunnelns verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="31651-124">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="31651-125">Wenn eine Standardwebsite angegeben wird, wird der gesamte Internetdatenverkehr vom VPN (virtuelles privates Netzwerk) des Gateways an diese Website weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="31651-125">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="31651-126">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="31651-126">-GatewaySku</span></span>
<span data-ttu-id="31651-127">Gibt die Lagerhaltungs Einheit (SKU) des virtuellen Netzwerkgateways an.</span><span class="sxs-lookup"><span data-stu-id="31651-127">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="31651-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="31651-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31651-129">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="31651-129">Basic</span></span>
- <span data-ttu-id="31651-130">Standard</span><span class="sxs-lookup"><span data-stu-id="31651-130">Standard</span></span>
- <span data-ttu-id="31651-131">Hochleistungs</span><span class="sxs-lookup"><span data-stu-id="31651-131">HighPerformance</span></span>
- <span data-ttu-id="31651-132">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="31651-132">VpnGw1</span></span>
- <span data-ttu-id="31651-133">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="31651-133">VpnGw2</span></span>
- <span data-ttu-id="31651-134">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="31651-134">VpnGw3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31651-135">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="31651-135">-PeerWeight</span></span>
<span data-ttu-id="31651-136">Gibt die Gewichtung von Routen an, die über BGP von diesem virtuellen Netzwerkgateway gelernt wurden.</span><span class="sxs-lookup"><span data-stu-id="31651-136">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="31651-137">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="31651-137">-RadiusServerAddress</span></span>
<span data-ttu-id="31651-138">P2S-externe RADIUS-Serveradresse.</span><span class="sxs-lookup"><span data-stu-id="31651-138">P2S External Radius server address.</span></span>
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

### <span data-ttu-id="31651-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="31651-139">-RadiusServerSecret</span></span>
<span data-ttu-id="31651-140">P2S externer RADIUS-Server-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="31651-140">P2S External Radius server secret.</span></span>
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

### <span data-ttu-id="31651-141">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31651-141">-VirtualNetworkGateway</span></span>
<span data-ttu-id="31651-142">Gibt das virtuelles Netzwerkgateway-Objekt an, auf dem Änderungen basieren sollen.</span><span class="sxs-lookup"><span data-stu-id="31651-142">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="31651-143">Sie können das Get-AzureRmVirtualNetworkGateway-Cmdlet verwenden, um das Virtual Network Gateway-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="31651-143">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="31651-144">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="31651-144">-VpnClientAddressPool</span></span>
<span data-ttu-id="31651-145">Gibt den Adressraum an, von dem dieses Cmdlet für die Zuweisung von VPN-Client-IP-Adressen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31651-145">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="31651-146">Dies sollte sich nicht mit virtuellen Netzwerken oder lokalen Bereichen überlappen.</span><span class="sxs-lookup"><span data-stu-id="31651-146">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31651-147">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="31651-147">-VpnClientProtocol</span></span>
<span data-ttu-id="31651-148">Eine Liste der P2S-VPN-Client Tunneling-Protokolle</span><span class="sxs-lookup"><span data-stu-id="31651-148">A list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31651-149">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="31651-149">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="31651-150">Gibt eine Liste der gesperrten VPN-Clientzertifikate an.</span><span class="sxs-lookup"><span data-stu-id="31651-150">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="31651-151">Ein VPN-Client mit einem Zertifikat, das einem dieser Zertifikate entspricht, wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="31651-151">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31651-152">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="31651-152">-VpnClientRootCertificates</span></span>
<span data-ttu-id="31651-153">Gibt eine Liste der VPN-Client Stammzertifikate an, die für die VPN-Clientauthentifizierung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="31651-153">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="31651-154">Beim Verbinden von VPN-Clients müssen Zertifikate vorhanden sein, die aus einem dieser Stammzertifikate generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="31651-154">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31651-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="31651-155">-Confirm</span></span>
<span data-ttu-id="31651-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="31651-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31651-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31651-157">-WhatIf</span></span>
<span data-ttu-id="31651-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31651-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31651-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31651-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31651-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31651-160">CommonParameters</span></span>
<span data-ttu-id="31651-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31651-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31651-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31651-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31651-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31651-163">INPUTS</span></span>

### <span data-ttu-id="31651-164">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31651-164">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="31651-165">Der Parameter "VirtualNetworkGateway" akzeptiert den Wert vom Typ "PSVirtualNetworkGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="31651-165">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="31651-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31651-166">OUTPUTS</span></span>

### <span data-ttu-id="31651-167">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31651-167">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="31651-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="31651-168">NOTES</span></span>
* <span data-ttu-id="31651-169">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="31651-169">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="31651-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31651-170">RELATED LINKS</span></span>

[<span data-ttu-id="31651-171">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31651-171">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="31651-172">Neu – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31651-172">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="31651-173">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31651-173">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="31651-174">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31651-174">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="31651-175">Größe ändern – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31651-175">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


