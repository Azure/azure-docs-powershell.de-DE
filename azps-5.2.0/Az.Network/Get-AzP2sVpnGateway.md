---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
ms.openlocfilehash: 541115347cfca85e0259e425912e83c4649e0952
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294437"
---
# <span data-ttu-id="d8847-101">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d8847-101">Get-AzP2sVpnGateway</span></span>

## <span data-ttu-id="d8847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8847-102">SYNOPSIS</span></span>
<span data-ttu-id="d8847-103">Ruft ein vorhandenes P2SVpnGateway unter VirtualHub ab.</span><span class="sxs-lookup"><span data-stu-id="d8847-103">Gets an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="d8847-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8847-104">SYNTAX</span></span>

### <span data-ttu-id="d8847-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8847-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzP2sVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8847-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8847-106">ListByResourceGroupName</span></span>
```
Get-AzP2sVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8847-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8847-107">DESCRIPTION</span></span>
<span data-ttu-id="d8847-108">Mit **dem Cmdlet "Get-AzP2sVpnGateway"** können Sie ein vorhandenes P2SVpnGateway unter VirtualHub abrufen.</span><span class="sxs-lookup"><span data-stu-id="d8847-108">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="d8847-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8847-109">EXAMPLES</span></span>

### <span data-ttu-id="d8847-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d8847-110">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

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
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="d8847-111">Mit **dem Cmdlet "Get-AzP2sVpnGateway"** können Sie ein vorhandenes P2SVpnGateway unter VirtualHub abrufen, das für die Point-to-Site-Konnektivität verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8847-111">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub that is used for Point to site connectivity.</span></span>

## <span data-ttu-id="d8847-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8847-112">PARAMETERS</span></span>

### <span data-ttu-id="d8847-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8847-113">-DefaultProfile</span></span>
<span data-ttu-id="d8847-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8847-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8847-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d8847-115">-Name</span></span>
<span data-ttu-id="d8847-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d8847-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, P2SVpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8847-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8847-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8847-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d8847-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8847-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8847-119">CommonParameters</span></span>
<span data-ttu-id="d8847-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8847-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8847-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8847-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8847-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8847-122">INPUTS</span></span>

### <span data-ttu-id="d8847-123">Keine</span><span class="sxs-lookup"><span data-stu-id="d8847-123">None</span></span>

## <span data-ttu-id="d8847-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8847-124">OUTPUTS</span></span>

### <span data-ttu-id="d8847-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d8847-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="d8847-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d8847-126">NOTES</span></span>

## <span data-ttu-id="d8847-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d8847-127">RELATED LINKS</span></span>
