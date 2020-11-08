---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: 4b9778275f58025c82922133cb5d6f6142df4fc8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995066"
---
# <span data-ttu-id="50171-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="50171-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="50171-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50171-102">SYNOPSIS</span></span>
<span data-ttu-id="50171-103">Ruft den aktuellen aggregared-Punkt zu den Integritätsinformationen für Standortverbindungen von P2SVpnGateway ab.</span><span class="sxs-lookup"><span data-stu-id="50171-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="50171-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50171-104">SYNTAX</span></span>

### <span data-ttu-id="50171-105">ByP2SVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="50171-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50171-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="50171-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50171-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="50171-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50171-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50171-108">DESCRIPTION</span></span>
<span data-ttu-id="50171-109">Mit dem Cmdlet **Get-AzP2sVpnGatewayConnectionHealth** können Sie die aktuelle aggregierte Integrität von Point-to-Site-Verbindungen von P2SVpnGateway abrufen.</span><span class="sxs-lookup"><span data-stu-id="50171-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="50171-110">"Aggregierter Zustand" zeigt die Anzahl der auf P2SVpnGateway verbundenen Website Clients, die Gesamtzahl der Ingress-und Ausgangsbytes, die über P2SVpnGateway und zugewiesene IP-Adressen für verbundene Punkte an Website Clients übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="50171-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="50171-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50171-111">EXAMPLES</span></span>

### <span data-ttu-id="50171-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="50171-112">Example 1</span></span>
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

<span data-ttu-id="50171-113">Mit dem Cmdlet **Get-AzP2sVpnGatewayConnectionHealth** können Sie die aktuelle aggregierte Integrität von Point-to-Site-Verbindungen von P2SVpnGateway abrufen.</span><span class="sxs-lookup"><span data-stu-id="50171-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="50171-114">Über den Befehl "Ausgabestatus" wird angezeigt, dass die Anzahl von Punkten für Website Clients, die mit P2SVpnGateway verbunden sind, 2 ist.</span><span class="sxs-lookup"><span data-stu-id="50171-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="50171-115">Die Gesamtzahl der Ingress-und Ausgangsbytes, die über P2SVpnGateway übertragen werden, sind 100 und 200.</span><span class="sxs-lookup"><span data-stu-id="50171-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="50171-116">Zugewiesene IP-Adressen für verbundene Punkte zu Website Clients sind "192.168.2.1", "192.168.2.2".</span><span class="sxs-lookup"><span data-stu-id="50171-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="50171-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="50171-117">PARAMETERS</span></span>

### <span data-ttu-id="50171-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50171-118">-DefaultProfile</span></span>
<span data-ttu-id="50171-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50171-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50171-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="50171-120">-InputObject</span></span>
<span data-ttu-id="50171-121">Das zu ändernde P2S-VPN-Gateway-Objekt</span><span class="sxs-lookup"><span data-stu-id="50171-121">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="50171-122">-Name</span><span class="sxs-lookup"><span data-stu-id="50171-122">-Name</span></span>
<span data-ttu-id="50171-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="50171-123">The resource name.</span></span>

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

### <span data-ttu-id="50171-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50171-124">-ResourceGroupName</span></span>
<span data-ttu-id="50171-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="50171-125">The resource group name.</span></span>

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

### <span data-ttu-id="50171-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="50171-126">-ResourceId</span></span>
<span data-ttu-id="50171-127">Die Azure-Ressourcen-ID des zu ändernden P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="50171-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="50171-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50171-128">CommonParameters</span></span>
<span data-ttu-id="50171-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50171-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50171-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50171-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50171-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50171-131">INPUTS</span></span>

### <span data-ttu-id="50171-132">System. String</span><span class="sxs-lookup"><span data-stu-id="50171-132">System.String</span></span>
<span data-ttu-id="50171-133">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="50171-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="50171-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50171-134">OUTPUTS</span></span>

### <span data-ttu-id="50171-135">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="50171-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="50171-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="50171-136">NOTES</span></span>

## <span data-ttu-id="50171-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50171-137">RELATED LINKS</span></span>
