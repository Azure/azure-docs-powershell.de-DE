---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azp2svpngatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2sVpnGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2sVpnGatewayVpnConnection.md
ms.openlocfilehash: ee14842a636ff451e100a75db427934f9f0a1043
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003794"
---
# <span data-ttu-id="75b53-101">Disconnect-AzP2sVpnGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="75b53-101">Disconnect-AzP2sVpnGatewayVpnConnection</span></span>

## <span data-ttu-id="75b53-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75b53-102">SYNOPSIS</span></span>
<span data-ttu-id="75b53-103">Trennen der angegebenen verbundenen VPN-Clientverbindungen mit einem bestimmten P2S-VPN-Gateway</span><span class="sxs-lookup"><span data-stu-id="75b53-103">Disconnect given connected vpn client connections with a given p2s vpn gateway</span></span>

## <span data-ttu-id="75b53-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75b53-104">SYNTAX</span></span>

### <span data-ttu-id="75b53-105">ByP2SVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="75b53-105">ByP2SVpnGatewayName (Default)</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -Name <String> -ResourceGroupName <String>
 -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="75b53-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="75b53-106">ByP2SVpnGatewayObject</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="75b53-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="75b53-107">ByP2SVpnGatewayResourceId</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="75b53-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75b53-108">DESCRIPTION</span></span>
<span data-ttu-id="75b53-109">Mit dem Cmdlet " **Disconnect-AzP2sVpnGatewayVpnConnection** " können Sie den angegebenen aktuellen Punkt mit der Standortverbindung von P2SVpnGateway trennen.</span><span class="sxs-lookup"><span data-stu-id="75b53-109">The **Disconnect-AzP2sVpnGatewayVpnConnection** cmdlet enables you to disconnect given current point to site connection from P2SVpnGateway.</span></span>

## <span data-ttu-id="75b53-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75b53-110">EXAMPLES</span></span>

### <span data-ttu-id="75b53-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75b53-111">Example 1</span></span>
```powershell
PS C:\> Disconnect-AzP2sVpnGatewayVpnConnection -ResourceName 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

## <span data-ttu-id="75b53-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="75b53-112">PARAMETERS</span></span>

### <span data-ttu-id="75b53-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="75b53-113">-InputObject</span></span>
<span data-ttu-id="75b53-114">Das zu ändernde P2S-VPN-Gateway-Objekt</span><span class="sxs-lookup"><span data-stu-id="75b53-114">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75b53-115">-Name</span><span class="sxs-lookup"><span data-stu-id="75b53-115">-Name</span></span>
<span data-ttu-id="75b53-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="75b53-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b53-117">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="75b53-117">-VpnConnectionId</span></span>
<span data-ttu-id="75b53-118">VPN-Verbindung Ida</span><span class="sxs-lookup"><span data-stu-id="75b53-118">Vpn Connection Ida</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b53-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75b53-119">-ResourceGroupName</span></span>
<span data-ttu-id="75b53-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="75b53-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b53-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="75b53-121">-ResourceId</span></span>
<span data-ttu-id="75b53-122">P2s-Ressourcen-ID für virtuelles Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="75b53-122">P2s Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75b53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b53-123">CommonParameters</span></span>
<span data-ttu-id="75b53-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b53-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b53-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b53-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75b53-126">INPUTS</span></span>

### <span data-ttu-id="75b53-127">System. String</span><span class="sxs-lookup"><span data-stu-id="75b53-127">System.String</span></span>

## <span data-ttu-id="75b53-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75b53-128">OUTPUTS</span></span>

### <span data-ttu-id="75b53-129">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="75b53-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="75b53-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="75b53-130">NOTES</span></span>

## <span data-ttu-id="75b53-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75b53-131">RELATED LINKS</span></span>
