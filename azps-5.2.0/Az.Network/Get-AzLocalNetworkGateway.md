---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 14c0ec31f10a6405fb2a3f412f004d53dbdeb9a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308544"
---
# <span data-ttu-id="3be44-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be44-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="3be44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3be44-102">SYNOPSIS</span></span>
<span data-ttu-id="3be44-103">Ruft ein lokales Netzwerkgateway ab</span><span class="sxs-lookup"><span data-stu-id="3be44-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="3be44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3be44-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3be44-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3be44-105">DESCRIPTION</span></span>
<span data-ttu-id="3be44-106">Das lokale Netzwerkgateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="3be44-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="3be44-107">Das **Cmdlet "Get-AzLocalNetworkGateway"** gibt das Objekt zurück, das Ihr lokales Gateway basierend auf "Name" und "Ressourcengruppenname" darstellt.</span><span class="sxs-lookup"><span data-stu-id="3be44-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="3be44-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3be44-108">EXAMPLES</span></span>

### <span data-ttu-id="3be44-109">Beispiel 1: Erhalten eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="3be44-109">Example 1: Get a Local Network Gateway</span></span>
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW1 -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="3be44-110">Gibt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW1" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="3be44-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="3be44-111">Beispiel 2: Erhalten lokaler Netzwerkgateways mithilfe der Filterung</span><span class="sxs-lookup"><span data-stu-id="3be44-111">Example 2: Get Local Network Gateways using filtering</span></span>
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW* -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null

Name                     : myLocalGW2
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="3be44-112">Gibt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW" in der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="3be44-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="3be44-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3be44-113">PARAMETERS</span></span>

### <span data-ttu-id="3be44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3be44-114">-DefaultProfile</span></span>
<span data-ttu-id="3be44-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3be44-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3be44-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3be44-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3be44-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3be44-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3be44-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be44-118">CommonParameters</span></span>
<span data-ttu-id="3be44-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3be44-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be44-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3be44-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be44-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3be44-121">INPUTS</span></span>

### <span data-ttu-id="3be44-122">System.String</span><span class="sxs-lookup"><span data-stu-id="3be44-122">System.String</span></span>

## <span data-ttu-id="3be44-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3be44-123">OUTPUTS</span></span>

### <span data-ttu-id="3be44-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be44-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="3be44-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3be44-125">NOTES</span></span>

## <span data-ttu-id="3be44-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3be44-126">RELATED LINKS</span></span>

[<span data-ttu-id="3be44-127">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be44-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="3be44-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be44-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="3be44-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3be44-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
