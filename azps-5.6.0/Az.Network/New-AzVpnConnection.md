---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 92eab91d06a8624c00973bb35cc1a56dfd096a89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934816"
---
# <span data-ttu-id="27d15-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="27d15-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="27d15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27d15-102">SYNOPSIS</span></span>
<span data-ttu-id="27d15-103">Erstellt eine IPSec-Verbindung, die ein VpnGateway mit einer Remotekundenverzweigung verbindet, die in RM als VpnSite dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="27d15-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="27d15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27d15-104">SYNTAX</span></span>

### <span data-ttu-id="27d15-105">ByVpnGatewayNameByVpnSiteObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="27d15-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27d15-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="27d15-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27d15-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="27d15-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27d15-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="27d15-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27d15-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="27d15-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27d15-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="27d15-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27d15-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27d15-111">DESCRIPTION</span></span>
<span data-ttu-id="27d15-112">Erstellt eine IPSec-Verbindung, die ein VpnGateway mit einer Remotekundenverzweigung verbindet, die in RM als VpnSite dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="27d15-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="27d15-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27d15-113">EXAMPLES</span></span>

### <span data-ttu-id="27d15-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="27d15-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="27d15-115">Mit dem vorstehenden Beispiel werden eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub und eine VpnWebsite in West USA in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="27d15-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="27d15-116">Anschließend wird im virtuellen Hub ein VPN-Gateway mit zwei Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="27d15-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="27d15-117">Nachdem das Gateway erstellt wurde, wird es mithilfe des Befehls New-AzVpnConnection mit der VpnSite verbunden.</span><span class="sxs-lookup"><span data-stu-id="27d15-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="27d15-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="27d15-118">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink1 = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)


PS C:\> $vpnSiteLinkConnection1 = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100
PS C:\> $vpnSiteLinkConnection2 = New-AzVpnSiteLinkConnection -Name "testLinkConnection2" -VpnSiteLink $vpnSite.VpnSiteLinks[1] -ConnectionBandwidth 10

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection1, $vpnSiteLinkConnection2)
```

<span data-ttu-id="27d15-119">Mit dem vorstehenden Beispiel werden eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub und eine VpnWebsite mit 1 VpnSiteLinks in West USA in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="27d15-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="27d15-120">Anschließend wird im virtuellen Hub ein VPN-Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="27d15-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="27d15-121">Nachdem das Gateway erstellt wurde, wird es über den Befehl New-AzVpnConnection mit 1 VpnSiteLinkConnections mit dem VpnSiteLink der VpnSite verbunden.</span><span class="sxs-lookup"><span data-stu-id="27d15-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="27d15-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="27d15-122">PARAMETERS</span></span>

### <span data-ttu-id="27d15-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27d15-123">-AsJob</span></span>
<span data-ttu-id="27d15-124">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="27d15-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27d15-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="27d15-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="27d15-126">Die Bandbreite, die von dieser Verbindung in Mbit/s verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="27d15-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d15-127">-DefaultProfile</span></span>
<span data-ttu-id="27d15-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27d15-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27d15-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="27d15-129">-EnableBgp</span></span>
<span data-ttu-id="27d15-130">Aktivieren von BGP für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="27d15-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="27d15-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="27d15-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="27d15-132">Aktivieren der Internetsicherheit für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="27d15-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="27d15-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="27d15-133">-IpSecPolicy</span></span>
<span data-ttu-id="27d15-134">Die Bandbreite, die von dieser Verbindung in Mbit/s verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="27d15-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-135">-Name</span><span class="sxs-lookup"><span data-stu-id="27d15-135">-Name</span></span>
<span data-ttu-id="27d15-136">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="27d15-136">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="27d15-137">-ParentObject</span></span>
<span data-ttu-id="27d15-138">Das übergeordnete VpnGateway für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="27d15-138">The parent VpnGateway for this connection.</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-139">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="27d15-139">-ParentResourceId</span></span>
<span data-ttu-id="27d15-140">Die Ressourcen-ID des übergeordneten VpnGateways für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="27d15-140">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-141">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="27d15-141">-ParentResourceName</span></span>
<span data-ttu-id="27d15-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="27d15-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27d15-143">-ResourceGroupName</span></span>
<span data-ttu-id="27d15-144">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="27d15-144">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="27d15-145">-RoutingConfiguration</span></span>
<span data-ttu-id="27d15-146">Routingkonfiguration für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="27d15-146">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="27d15-147">-SharedKey</span></span>
<span data-ttu-id="27d15-148">Der freigegebene Schlüssel, der zum Einrichten dieser Verbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="27d15-148">The shared key required to set this connection up.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="27d15-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="27d15-150">Verwenden Sie beim Initiieren der Verbindung die lokale Azure-IP-Adresse als Quelladresse.</span><span class="sxs-lookup"><span data-stu-id="27d15-150">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="27d15-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="27d15-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="27d15-152">Verwenden Sie richtlinienbasierte Datenverkehrsauswahlen für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="27d15-152">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="27d15-153">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="27d15-153">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="27d15-154">Gatewayverbindungsprotokoll:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="27d15-154">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-155">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="27d15-155">-VpnSite</span></span>
<span data-ttu-id="27d15-156">Die Remote-VPN-Website, mit der diese virtuelle Netzwerkverbindung des Hubs verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="27d15-156">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-157">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="27d15-157">-VpnSiteId</span></span>
<span data-ttu-id="27d15-158">Die Remote-VPN-Website, mit der diese virtuelle Netzwerkverbindung des Hubs verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="27d15-158">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-159">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="27d15-159">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="27d15-160">Die Liste der VpnSiteLinkConnections, über die diese VpnConnection verfügt.</span><span class="sxs-lookup"><span data-stu-id="27d15-160">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

```yaml
Type: PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="27d15-161">-Confirm</span></span>
<span data-ttu-id="27d15-162">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27d15-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27d15-163">-WhatIf</span></span>
<span data-ttu-id="27d15-164">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27d15-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27d15-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27d15-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d15-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d15-166">CommonParameters</span></span>
<span data-ttu-id="27d15-167">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27d15-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d15-168">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27d15-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d15-169">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27d15-169">INPUTS</span></span>

### <span data-ttu-id="27d15-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="27d15-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="27d15-171">System.String</span><span class="sxs-lookup"><span data-stu-id="27d15-171">System.String</span></span>

## <span data-ttu-id="27d15-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27d15-172">OUTPUTS</span></span>

### <span data-ttu-id="27d15-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="27d15-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="27d15-174">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="27d15-174">NOTES</span></span>

## <span data-ttu-id="27d15-175">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="27d15-175">RELATED LINKS</span></span>

[<span data-ttu-id="27d15-176">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="27d15-176">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="27d15-177">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="27d15-177">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="27d15-178">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="27d15-178">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="27d15-179">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="27d15-179">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
