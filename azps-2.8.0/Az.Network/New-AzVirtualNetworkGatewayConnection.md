---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c25b311a4f99814c718ce825d61433d7c2fee192
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822991"
---
# <span data-ttu-id="05d8a-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="05d8a-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="05d8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="05d8a-103">Erstellt die Standort-zu-Standort-VPN-Verbindung zwischen dem virtuellen Netzwerkgateway und dem auf-Prem-VPN-Gerät.</span><span class="sxs-lookup"><span data-stu-id="05d8a-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="05d8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05d8a-104">SYNTAX</span></span>

### <span data-ttu-id="05d8a-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="05d8a-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] 
 [-AsJob] [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05d8a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="05d8a-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] 
 [-AsJob] [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05d8a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05d8a-107">DESCRIPTION</span></span>
<span data-ttu-id="05d8a-108">Erstellt die Standort-zu-Standort-VPN-Verbindung zwischen dem virtuellen Netzwerkgateway und dem auf-Prem-VPN-Gerät.</span><span class="sxs-lookup"><span data-stu-id="05d8a-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="05d8a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05d8a-109">EXAMPLES</span></span>

### <span data-ttu-id="05d8a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="05d8a-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="05d8a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="05d8a-111">PARAMETERS</span></span>

### <span data-ttu-id="05d8a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05d8a-112">-AsJob</span></span>
<span data-ttu-id="05d8a-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="05d8a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05d8a-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="05d8a-114">-AuthorizationKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8a-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="05d8a-115">-ConnectionProtocol</span></span>
<span data-ttu-id="05d8a-116">Gateway-Verbindungsprotokoll: ikev1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="05d8a-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05d8a-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="05d8a-117">-ConnectionType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d8a-118">-DefaultProfile</span></span>
<span data-ttu-id="05d8a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05d8a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05d8a-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="05d8a-120">-EnableBgp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8a-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="05d8a-121">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="05d8a-122">-Force</span></span>

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

### <span data-ttu-id="05d8a-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="05d8a-123">-IpsecPolicies</span></span>
<span data-ttu-id="05d8a-124">Eine Liste der IPSec-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="05d8a-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="05d8a-125">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="05d8a-125">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="05d8a-126">Eine Liste der Datenverkehrs Auswahlrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="05d8a-126">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8a-127">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="05d8a-127">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="05d8a-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="05d8a-128">-Location</span></span>

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

### <span data-ttu-id="05d8a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="05d8a-129">-Name</span></span>

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

### <span data-ttu-id="05d8a-130">-Peer</span><span class="sxs-lookup"><span data-stu-id="05d8a-130">-Peer</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8a-131">-Peer-Nr</span><span class="sxs-lookup"><span data-stu-id="05d8a-131">-PeerId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05d8a-132">-ResourceGroupName</span></span>

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

### <span data-ttu-id="05d8a-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="05d8a-133">-RoutingWeight</span></span>

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

### <span data-ttu-id="05d8a-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="05d8a-134">-SharedKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8a-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="05d8a-135">-Tag</span></span>
<span data-ttu-id="05d8a-136">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="05d8a-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="05d8a-137">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="05d8a-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="05d8a-138">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="05d8a-138">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="05d8a-139">Verwenden richtlinienbasierter Datenverkehrs Auswahlen für eine S2S-Verbindung</span><span class="sxs-lookup"><span data-stu-id="05d8a-139">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05d8a-140">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="05d8a-140">-VirtualNetworkGateway1</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8a-141">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="05d8a-141">-VirtualNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8a-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05d8a-142">-Confirm</span></span>
<span data-ttu-id="05d8a-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05d8a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05d8a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05d8a-144">-WhatIf</span></span>
<span data-ttu-id="05d8a-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05d8a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05d8a-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05d8a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05d8a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d8a-147">CommonParameters</span></span>
<span data-ttu-id="05d8a-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05d8a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d8a-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05d8a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d8a-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05d8a-150">INPUTS</span></span>

### <span data-ttu-id="05d8a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="05d8a-151">System.String</span></span>

### <span data-ttu-id="05d8a-152">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="05d8a-152">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="05d8a-153">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="05d8a-153">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="05d8a-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="05d8a-154">System.Int32</span></span>

### <span data-ttu-id="05d8a-155">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="05d8a-155">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="05d8a-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05d8a-156">System.Boolean</span></span>

### <span data-ttu-id="05d8a-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="05d8a-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="05d8a-158">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="05d8a-158">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="05d8a-159">Microsoft. Azure. Commands. Network. Models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="05d8a-159">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="05d8a-160">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="05d8a-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="05d8a-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05d8a-161">OUTPUTS</span></span>

### <span data-ttu-id="05d8a-162">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="05d8a-162">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="05d8a-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="05d8a-163">NOTES</span></span>

## <span data-ttu-id="05d8a-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05d8a-164">RELATED LINKS</span></span>

[<span data-ttu-id="05d8a-165">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="05d8a-165">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="05d8a-166">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="05d8a-166">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="05d8a-167">Satz-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="05d8a-167">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
