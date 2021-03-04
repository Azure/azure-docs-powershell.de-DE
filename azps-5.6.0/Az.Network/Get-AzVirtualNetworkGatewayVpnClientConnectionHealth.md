---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayvpnclientconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
ms.openlocfilehash: 560ab8485f9e5860230edeec904d53f57b43aa26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926520"
---
# <span data-ttu-id="1a587-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="1a587-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>

## <span data-ttu-id="1a587-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a587-102">SYNOPSIS</span></span> 
<span data-ttu-id="1a587-103">Hier finden Sie die Liste der Integrität der Vpn-Clientverbindung eines virtuellen Azure-Netzwerkgateways für pro VPN-Clientverbindung.</span><span class="sxs-lookup"><span data-stu-id="1a587-103">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection</span></span>

## <span data-ttu-id="1a587-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a587-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId>
 [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="1a587-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a587-105">DESCRIPTION</span></span>
<span data-ttu-id="1a587-106">Listen Sie den Integritätszustand aller verbundenen Vpn-Client-Verbindungen auf.</span><span class="sxs-lookup"><span data-stu-id="1a587-106">List  all connected vpn client connection health.</span></span> <span data-ttu-id="1a587-107">Dies umfasst: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span><span class="sxs-lookup"><span data-stu-id="1a587-107">This includes: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span></span>

## <span data-ttu-id="1a587-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a587-108">EXAMPLES</span></span>

### <span data-ttu-id="1a587-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1a587-109">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName gatewayName -ResourceGroupName resourceGroup

VpnConnectionId           : OVPN_0085393D-B345-4846-0426-140616833F4C
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39672
PrivateIpAddress          : 10.1.1.131
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104084
EgressBytesTransferred    : 4059276
IngressPacketsTransferred : 1410
IngressBytesTransferred   : 67680
MaxPacketsPerSecond       : 1

VpnConnectionId           : OVPN_00F692AC-2D6F-DE7B-DCAF-07BE896233A0
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39692
PrivateIpAddress          : 10.1.1.79
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104623
EgressBytesTransferred    : 4080297
IngressPacketsTransferred : 1416
IngressBytesTransferred   : 67968
MaxPacketsPerSecond       : 1
```

<span data-ttu-id="1a587-110">Ruft für das azure virtual network gateway named gatewayname in resource group resourceGroup die aktuell verbundene Vpn-Clientverbindung mithilfe von OpenVpn ab.</span><span class="sxs-lookup"><span data-stu-id="1a587-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves the currently connected vpn client connection by using OpenVpn.</span></span> 

### <span data-ttu-id="1a587-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1a587-111">Example 2</span></span>

<span data-ttu-id="1a587-112">Hier finden Sie die Liste der Integrität der Vpn-Clientverbindung eines virtuellen Azure-Netzwerkgateways für pro VPN-Clientverbindung.</span><span class="sxs-lookup"><span data-stu-id="1a587-112">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection.</span></span> <span data-ttu-id="1a587-113">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="1a587-113">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceGroupName resourceGroup -VirtualNetworkGatewayName 'ContosoVirtualNetwork'
```

## <span data-ttu-id="1a587-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1a587-114">PARAMETERS</span></span>

### <span data-ttu-id="1a587-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a587-115">-ResourceGroupName</span></span>
<span data-ttu-id="1a587-116">Name der Ressourcengruppe "Virtuelles Netzwerkgateway"</span><span class="sxs-lookup"><span data-stu-id="1a587-116">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="1a587-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1a587-117">-ResourceName</span></span>
<span data-ttu-id="1a587-118">Name des Virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="1a587-118">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="1a587-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a587-119">-ResourceId</span></span>
<span data-ttu-id="1a587-120">Ressourcen-ID des Virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="1a587-120">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a587-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a587-121">-InputObject</span></span>
<span data-ttu-id="1a587-122">Virtuelles Netzwerkgatewayobjekt</span><span class="sxs-lookup"><span data-stu-id="1a587-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a587-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a587-123">-AsJob</span></span>
<span data-ttu-id="1a587-124">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1a587-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a587-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a587-125">CommonParameters</span></span>
<span data-ttu-id="1a587-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a587-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a587-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a587-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a587-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a587-128">INPUTS</span></span>

### <span data-ttu-id="1a587-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1a587-129">System.String</span></span>

## <span data-ttu-id="1a587-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a587-130">OUTPUTS</span></span>

### <span data-ttu-id="1a587-131">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="1a587-131">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="1a587-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1a587-132">NOTES</span></span>

## <span data-ttu-id="1a587-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1a587-133">RELATED LINKS</span></span>
