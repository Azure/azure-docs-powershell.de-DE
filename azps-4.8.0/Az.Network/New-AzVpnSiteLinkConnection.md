---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: 31679702c1499ac91f41b14057e1bc13ef2dfc32
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174557"
---
# <span data-ttu-id="1be17-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="1be17-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="1be17-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1be17-102">SYNOPSIS</span></span>
<span data-ttu-id="1be17-103">Erstellt ein Azure VpnSiteLinkConnection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1be17-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="1be17-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1be17-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1be17-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1be17-105">DESCRIPTION</span></span>
<span data-ttu-id="1be17-106">Erstellt ein Azure VpnSiteLinkConnection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1be17-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="1be17-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1be17-107">EXAMPLES</span></span>

### <span data-ttu-id="1be17-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1be17-108">Example 1</span></span>
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

<span data-ttu-id="1be17-109">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuellen Hub und einen VpnSite mit 1 VpnSiteLinks in West Amerika in "testRG"-Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="1be17-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="1be17-110">Anschließend wird ein VPN-Gateway im virtuellen Hub erstellt.</span><span class="sxs-lookup"><span data-stu-id="1be17-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="1be17-111">Nachdem das Gateway erstellt wurde, wird es mit dem VpnSite mit dem Befehl New-AzVpnConnection mit 1 VpnSiteLinkConnections zum VpnSiteLink des VpnSite verbunden.</span><span class="sxs-lookup"><span data-stu-id="1be17-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="1be17-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1be17-112">PARAMETERS</span></span>

### <span data-ttu-id="1be17-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="1be17-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="1be17-114">Die Bandbreite, die von dieser Verbindungs Verbindung in Mbit/s verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="1be17-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="1be17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be17-115">-DefaultProfile</span></span>
<span data-ttu-id="1be17-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1be17-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1be17-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="1be17-117">-EnableBgp</span></span>
<span data-ttu-id="1be17-118">Aktivieren von BGP für diese Link Verbindung</span><span class="sxs-lookup"><span data-stu-id="1be17-118">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="1be17-119">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="1be17-119">-IpSecPolicy</span></span>
<span data-ttu-id="1be17-120">IpSec-Richtlinie, die für diese Link Verbindung zu berücksichtigen ist.</span><span class="sxs-lookup"><span data-stu-id="1be17-120">IpSec Policy to be considered for this link connection.</span></span>

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

### <span data-ttu-id="1be17-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1be17-121">-Name</span></span>
<span data-ttu-id="1be17-122">Namen</span><span class="sxs-lookup"><span data-stu-id="1be17-122">Name</span></span>

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

### <span data-ttu-id="1be17-123">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="1be17-123">-RoutingWeight</span></span>
<span data-ttu-id="1be17-124">Arbeitsplan Gewichtung</span><span class="sxs-lookup"><span data-stu-id="1be17-124">Routing Weight</span></span>

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

### <span data-ttu-id="1be17-125">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="1be17-125">-SharedKey</span></span>
<span data-ttu-id="1be17-126">Der freigegebene Schlüssel, der zum Einrichten dieser Verbindungs Verbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1be17-126">The shared key required to set this link connection up.</span></span>

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

### <span data-ttu-id="1be17-127">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="1be17-127">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="1be17-128">Verwenden Sie die lokale Azure-IP-Adresse als Quell-IP für diese Link Verbindung.</span><span class="sxs-lookup"><span data-stu-id="1be17-128">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="1be17-129">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="1be17-129">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="1be17-130">Verwenden Sie richtlinienbasierte Datenverkehrs Auswahl für diese Link Verbindung.</span><span class="sxs-lookup"><span data-stu-id="1be17-130">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="1be17-131">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="1be17-131">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="1be17-132">Gateway-Verbindungsprotokoll: ikev1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="1be17-132">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="1be17-133">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="1be17-133">-VpnSiteLink</span></span>
<span data-ttu-id="1be17-134">Das VPN-Standortverknüpfungsobjekt, mit dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1be17-134">The vpn site link object to connect to.</span></span>

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

### <span data-ttu-id="1be17-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be17-135">CommonParameters</span></span>
<span data-ttu-id="1be17-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1be17-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be17-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1be17-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be17-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1be17-138">INPUTS</span></span>

### <span data-ttu-id="1be17-139">Microsoft. Azure. Commands. Network. Models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="1be17-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="1be17-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1be17-140">OUTPUTS</span></span>

### <span data-ttu-id="1be17-141">Microsoft. Azure. Commands. Network. Models. PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="1be17-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="1be17-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="1be17-142">NOTES</span></span>

## <span data-ttu-id="1be17-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1be17-143">RELATED LINKS</span></span>

[<span data-ttu-id="1be17-144">Neu – AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="1be17-144">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)