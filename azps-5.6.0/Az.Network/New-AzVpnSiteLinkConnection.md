---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: 4f61bce910a2dc0f2b177423a5dc199103da378d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934768"
---
# <span data-ttu-id="c98a1-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c98a1-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="c98a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c98a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c98a1-103">Erstellt ein Azure VpnSiteLinkConnection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c98a1-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="c98a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c98a1-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-IngressNatRule <PSResourceId[]>] [-EgressNatRule <PSResourceId[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c98a1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c98a1-105">DESCRIPTION</span></span>
<span data-ttu-id="c98a1-106">Erstellt ein Azure VpnSiteLinkConnection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c98a1-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="c98a1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c98a1-107">EXAMPLES</span></span>

### <span data-ttu-id="c98a1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c98a1-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)


PS C:\> $vpnSiteLinkConnection = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection)
```

<span data-ttu-id="c98a1-109">Mit dem vorstehenden Beispiel werden eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub und eine VpnWebsite mit 1 VpnSiteLinks in West USA in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="c98a1-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="c98a1-110">Anschließend wird im virtuellen Hub ein VPN-Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="c98a1-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="c98a1-111">Nachdem das Gateway erstellt wurde, wird es über den Befehl New-AzVpnConnection mit 1 VpnSiteLinkConnections mit dem VpnSiteLink der VpnSite verbunden.</span><span class="sxs-lookup"><span data-stu-id="c98a1-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="c98a1-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c98a1-112">PARAMETERS</span></span>

### <span data-ttu-id="c98a1-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="c98a1-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="c98a1-114">Die Bandbreite, die von dieser Linkverbindung in Mbit/s verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c98a1-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c98a1-115">-DefaultProfile</span></span>
<span data-ttu-id="c98a1-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c98a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c98a1-117">-EgressNatRule</span><span class="sxs-lookup"><span data-stu-id="c98a1-117">-EgressNatRule</span></span>
<span data-ttu-id="c98a1-118">Die Liste der ausstehenden NAT-Regeln, die diesem Link Verbindung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c98a1-118">The list of egress  NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a1-119">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="c98a1-119">-EnableBgp</span></span>
<span data-ttu-id="c98a1-120">Aktivieren von BGP für diese Linkverbindung</span><span class="sxs-lookup"><span data-stu-id="c98a1-120">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="c98a1-121">-IngressNatRule</span><span class="sxs-lookup"><span data-stu-id="c98a1-121">-IngressNatRule</span></span>
<span data-ttu-id="c98a1-122">Die Liste der ingress-NAT-Regeln, die diesem Link Verbindung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c98a1-122">The list of ingress NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a1-123">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="c98a1-123">-IpSecPolicy</span></span>
<span data-ttu-id="c98a1-124">IpSec-Richtlinie, die für diese Linkverbindung in Betracht gezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c98a1-124">IpSec Policy to be considered for this link connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c98a1-125">-Name</span></span>
<span data-ttu-id="c98a1-126">Name</span><span class="sxs-lookup"><span data-stu-id="c98a1-126">Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a1-127">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="c98a1-127">-RoutingWeight</span></span>
<span data-ttu-id="c98a1-128">Routinggewichtung</span><span class="sxs-lookup"><span data-stu-id="c98a1-128">Routing Weight</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a1-129">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c98a1-129">-SharedKey</span></span>
<span data-ttu-id="c98a1-130">Der freigegebene Schlüssel, der zum Einrichten dieser Linkverbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c98a1-130">The shared key required to set this link connection up.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a1-131">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="c98a1-131">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="c98a1-132">Verwenden Sie die lokale Azure-IP-Adresse als Quell-IP für diese Linkverbindung.</span><span class="sxs-lookup"><span data-stu-id="c98a1-132">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="c98a1-133">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="c98a1-133">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="c98a1-134">Verwenden Sie richtlinienbasierte Datenverkehrsauswahlen für diese Linkverbindung.</span><span class="sxs-lookup"><span data-stu-id="c98a1-134">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="c98a1-135">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="c98a1-135">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="c98a1-136">Gatewayverbindungsprotokoll:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="c98a1-136">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="c98a1-137">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="c98a1-137">-VpnSiteLink</span></span>
<span data-ttu-id="c98a1-138">Das Vpn-Websiteverknüpfungsobjekt, mit dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c98a1-138">The vpn site link object to connect to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c98a1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98a1-139">CommonParameters</span></span>
<span data-ttu-id="c98a1-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c98a1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98a1-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c98a1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98a1-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c98a1-142">INPUTS</span></span>

### <span data-ttu-id="c98a1-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="c98a1-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="c98a1-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c98a1-144">OUTPUTS</span></span>

### <span data-ttu-id="c98a1-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c98a1-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="c98a1-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c98a1-146">NOTES</span></span>

## <span data-ttu-id="c98a1-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c98a1-147">RELATED LINKS</span></span>

[<span data-ttu-id="c98a1-148">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c98a1-148">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)