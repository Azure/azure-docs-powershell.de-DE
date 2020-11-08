---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayvpnclientconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
ms.openlocfilehash: 21529e75ab32cf4dde0434b9e2d4de8951beeb39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166299"
---
# <span data-ttu-id="62e68-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="62e68-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>

## <span data-ttu-id="62e68-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62e68-102">SYNOPSIS</span></span> 
<span data-ttu-id="62e68-103">Abrufen der Liste der VPN-Client Verbindungsintegrität eines Azure Virtual Network-Gateways für pro VPN-Clientverbindung</span><span class="sxs-lookup"><span data-stu-id="62e68-103">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection</span></span>

## <span data-ttu-id="62e68-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="62e68-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId>
 [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="62e68-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62e68-105">DESCRIPTION</span></span>
<span data-ttu-id="62e68-106">Auflisten aller verbundenen VPN-Client Verbindungsintegrität</span><span class="sxs-lookup"><span data-stu-id="62e68-106">List  all connected vpn client connection health.</span></span> <span data-ttu-id="62e68-107">Dies umfasst: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span><span class="sxs-lookup"><span data-stu-id="62e68-107">This includes: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span></span>

## <span data-ttu-id="62e68-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62e68-108">EXAMPLES</span></span>

### <span data-ttu-id="62e68-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="62e68-109">Example 1</span></span>
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

<span data-ttu-id="62e68-110">Ruft für das Azure Virtual Network Gateway mit dem Namen "Gatewayname" in der Ressourcengruppe "ResourceGroup" die derzeit verbundene VPN-Clientverbindung mithilfe von OpenVpn ab.</span><span class="sxs-lookup"><span data-stu-id="62e68-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves the currently connected vpn client connection by using OpenVpn.</span></span> 

### <span data-ttu-id="62e68-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="62e68-111">Example 2</span></span>

<span data-ttu-id="62e68-112">Rufen Sie die Liste der VPN-Client Verbindungsintegrität eines Azure Virtual Network-Gateways für pro VPN-Clientverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="62e68-112">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection.</span></span> <span data-ttu-id="62e68-113">automatisch</span><span class="sxs-lookup"><span data-stu-id="62e68-113">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceGroupName resourceGroup -VirtualNetworkGatewayName 'ContosoVirtualNetwork'
```

## <span data-ttu-id="62e68-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="62e68-114">PARAMETERS</span></span>

### <span data-ttu-id="62e68-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e68-115">-ResourceGroupName</span></span>
<span data-ttu-id="62e68-116">Name der Ressourcengruppe der virtuellen Netzwerk-Gateway-Ressource</span><span class="sxs-lookup"><span data-stu-id="62e68-116">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="62e68-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="62e68-117">-ResourceName</span></span>
<span data-ttu-id="62e68-118">Name des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="62e68-118">Virtual network gateway name</span></span>

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
### <span data-ttu-id="62e68-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="62e68-119">-ResourceId</span></span>
<span data-ttu-id="62e68-120">Ressourcen-ID des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="62e68-120">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="62e68-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="62e68-121">-InputObject</span></span>
<span data-ttu-id="62e68-122">Virtuelles Netzwerkgateway-Objekt</span><span class="sxs-lookup"><span data-stu-id="62e68-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="62e68-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62e68-123">-AsJob</span></span>
<span data-ttu-id="62e68-124">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="62e68-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62e68-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e68-125">CommonParameters</span></span>
<span data-ttu-id="62e68-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62e68-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e68-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62e68-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e68-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62e68-128">INPUTS</span></span>

### <span data-ttu-id="62e68-129">System. String</span><span class="sxs-lookup"><span data-stu-id="62e68-129">System.String</span></span>

## <span data-ttu-id="62e68-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62e68-130">OUTPUTS</span></span>

### <span data-ttu-id="62e68-131">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="62e68-131">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="62e68-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="62e68-132">NOTES</span></span>

## <span data-ttu-id="62e68-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62e68-133">RELATED LINKS</span></span>
