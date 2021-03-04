---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: f3df825c7907921885809fa866bcc894a981f7f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919747"
---
# <span data-ttu-id="7aee7-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7aee7-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="7aee7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7aee7-102">SYNOPSIS</span></span>
<span data-ttu-id="7aee7-103">Ruft den aktuellen aggregared point to website connections health information from P2SVpnGateway ab.</span><span class="sxs-lookup"><span data-stu-id="7aee7-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="7aee7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7aee7-104">SYNTAX</span></span>

### <span data-ttu-id="7aee7-105">ByP2SVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7aee7-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7aee7-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7aee7-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7aee7-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7aee7-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7aee7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7aee7-108">DESCRIPTION</span></span>
<span data-ttu-id="7aee7-109">Mit **dem Cmdlet Get-AzP2sVpnGatewayConnectionHealth** können Sie den aktuellen aggregierten Status von Punkt-zu-Website-Verbindungen von P2SVpnGateway erhalten.</span><span class="sxs-lookup"><span data-stu-id="7aee7-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="7aee7-110">Der aggregierte Integritätszustand zeigt die Anzahl der mit P2SVpnGateway verbundenen Punkt-zu-Website-Clients, die Gesamtzahl der über P2SVpnGateway übertragenen Bytes und die zugewiesenen IP-Adressen für verbundene Punkte mit Websiteclients an.</span><span class="sxs-lookup"><span data-stu-id="7aee7-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="7aee7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7aee7-111">EXAMPLES</span></span>

### <span data-ttu-id="7aee7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7aee7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayConnectionHealth -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : { 
                  "VpnClientConnectionsCount": 2,
                      "AllocatedIpAddresses": { "192.168.2.1", "192.168.2.2" },
                      "TotalIngressBytesTransferred": 100,
                      "TotalEgressBytesTransferred": 200
                 }
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

<span data-ttu-id="7aee7-113">Mit **dem Cmdlet Get-AzP2sVpnGatewayConnectionHealth** können Sie den aktuellen aggregierten Status von Punkt-zu-Website-Verbindungen von P2SVpnGateway erhalten.</span><span class="sxs-lookup"><span data-stu-id="7aee7-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="7aee7-114">Mit dem Befehl "Ausgabezustand" oben wird angezeigt, dass die Anzahl der mit P2SVpnGateway verbundenen Punkt-zu-Website-Clients 2 ist.</span><span class="sxs-lookup"><span data-stu-id="7aee7-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="7aee7-115">Die Gesamtzahl der über P2SVpnGateway übertragenen Ein- und Ausstiegsbytes beträgt 100 bzw. 200.</span><span class="sxs-lookup"><span data-stu-id="7aee7-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="7aee7-116">Zugewiesene IP-Adressen für verbundene Punkte zu Websiteclients sind "192.168.2.1", "192.168.2.2".</span><span class="sxs-lookup"><span data-stu-id="7aee7-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="7aee7-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7aee7-117">PARAMETERS</span></span>

### <span data-ttu-id="7aee7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aee7-118">-DefaultProfile</span></span>
<span data-ttu-id="7aee7-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7aee7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7aee7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7aee7-120">-InputObject</span></span>
<span data-ttu-id="7aee7-121">Das zu ändernde p2s-Vpn-Gatewayobjekt</span><span class="sxs-lookup"><span data-stu-id="7aee7-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aee7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7aee7-122">-Name</span></span>
<span data-ttu-id="7aee7-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="7aee7-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aee7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aee7-124">-ResourceGroupName</span></span>
<span data-ttu-id="7aee7-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7aee7-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aee7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7aee7-126">-ResourceId</span></span>
<span data-ttu-id="7aee7-127">Die Azure-Ressourcen-ID des zu ändernden P2SVpnGateways.</span><span class="sxs-lookup"><span data-stu-id="7aee7-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aee7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aee7-128">CommonParameters</span></span>
<span data-ttu-id="7aee7-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aee7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aee7-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aee7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aee7-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7aee7-131">INPUTS</span></span>

### <span data-ttu-id="7aee7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7aee7-132">System.String</span></span>
<span data-ttu-id="7aee7-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7aee7-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="7aee7-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7aee7-134">OUTPUTS</span></span>

### <span data-ttu-id="7aee7-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7aee7-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="7aee7-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7aee7-136">NOTES</span></span>

## <span data-ttu-id="7aee7-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7aee7-137">RELATED LINKS</span></span>
