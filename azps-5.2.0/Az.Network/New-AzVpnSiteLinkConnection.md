---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: 31679702c1499ac91f41b14057e1bc13ef2dfc32
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364802"
---
# <span data-ttu-id="7ebf9-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7ebf9-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="7ebf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ebf9-102">SYNOPSIS</span></span>
<span data-ttu-id="7ebf9-103">Erstellt ein Azure VpnSiteLinkConnection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7ebf9-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="7ebf9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ebf9-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ebf9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ebf9-105">DESCRIPTION</span></span>
<span data-ttu-id="7ebf9-106">Erstellt ein Azure VpnSiteLinkConnection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7ebf9-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="7ebf9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ebf9-107">EXAMPLES</span></span>

### <span data-ttu-id="7ebf9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ebf9-108">Example 1</span></span>
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

<span data-ttu-id="7ebf9-109">Im vorstehenden Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtuelles Netzwerk, ein virtueller Hub und eine VpnSite mit 1 VpnSiteLinks in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="7ebf9-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="7ebf9-110">Anschließend wird im virtuellen Hub ein VPN-Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="7ebf9-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="7ebf9-111">Nachdem das Gateway erstellt wurde, wird es über den Befehl New-AzVpnConnection mit 1 VpnSiteLinkConnections mit dem VpnSiteLink der VpnSite verbunden.</span><span class="sxs-lookup"><span data-stu-id="7ebf9-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="7ebf9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ebf9-112">PARAMETERS</span></span>

### <span data-ttu-id="7ebf9-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="7ebf9-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="7ebf9-114">Die Bandbreite, die von dieser Verknüpfungsverbindung in Mbit/s behandelt werden muss.</span><span class="sxs-lookup"><span data-stu-id="7ebf9-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="7ebf9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ebf9-115">-DefaultProfile</span></span>
<span data-ttu-id="7ebf9-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ebf9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ebf9-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7ebf9-117">-EnableBgp</span></span>
<span data-ttu-id="7ebf9-118">Aktivieren von BGP für diese Verknüpfungsverbindung</span><span class="sxs-lookup"><span data-stu-id="7ebf9-118">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="7ebf9-119">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="7ebf9-119">-IpSecPolicy</span></span>
<span data-ttu-id="7ebf9-120">Für diese Verknüpfungsverbindung zu berücksichtigende IpSec-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="7ebf9-120">IpSec Policy to be considered for this link connection.</span></span>

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

### <span data-ttu-id="7ebf9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7ebf9-121">-Name</span></span>
<span data-ttu-id="7ebf9-122">Name</span><span class="sxs-lookup"><span data-stu-id="7ebf9-122">Name</span></span>

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

### <span data-ttu-id="7ebf9-123">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="7ebf9-123">-RoutingWeight</span></span>
<span data-ttu-id="7ebf9-124">Routing Weight</span><span class="sxs-lookup"><span data-stu-id="7ebf9-124">Routing Weight</span></span>

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

### <span data-ttu-id="7ebf9-125">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7ebf9-125">-SharedKey</span></span>
<span data-ttu-id="7ebf9-126">Der freigegebene Schlüssel, der zum Einrichten dieser Linkverbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7ebf9-126">The shared key required to set this link connection up.</span></span>

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

### <span data-ttu-id="7ebf9-127">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ebf9-127">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="7ebf9-128">Verwenden Sie die lokale Azure-IP-Adresse als Quell-IP für diese Linkverbindung.</span><span class="sxs-lookup"><span data-stu-id="7ebf9-128">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="7ebf9-129">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="7ebf9-129">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="7ebf9-130">Verwenden Sie richtlinienbasierte Datenverkehrsauswahlen für diese Verknüpfungsverbindung.</span><span class="sxs-lookup"><span data-stu-id="7ebf9-130">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="7ebf9-131">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="7ebf9-131">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="7ebf9-132">Gatewayverbindungsprotokoll:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="7ebf9-132">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="7ebf9-133">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="7ebf9-133">-VpnSiteLink</span></span>
<span data-ttu-id="7ebf9-134">Das Vpn-Website-Link-Objekt, mit dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ebf9-134">The vpn site link object to connect to.</span></span>

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

### <span data-ttu-id="7ebf9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ebf9-135">CommonParameters</span></span>
<span data-ttu-id="7ebf9-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ebf9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ebf9-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ebf9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ebf9-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ebf9-138">INPUTS</span></span>

### <span data-ttu-id="7ebf9-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="7ebf9-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="7ebf9-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ebf9-140">OUTPUTS</span></span>

### <span data-ttu-id="7ebf9-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7ebf9-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="7ebf9-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7ebf9-142">NOTES</span></span>

## <span data-ttu-id="7ebf9-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7ebf9-143">RELATED LINKS</span></span>

[<span data-ttu-id="7ebf9-144">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7ebf9-144">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)