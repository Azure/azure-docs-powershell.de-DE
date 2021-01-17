---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365125"
---
# <span data-ttu-id="5163e-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="5163e-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="5163e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5163e-102">SYNOPSIS</span></span>
<span data-ttu-id="5163e-103">Ruft eine "ExpressRouteGateway"-Ressource mit "ResourceGroupName" und "GatewayName OR" ab und listet alle Gateways nach "ResourceGroupName" oder "SubscriptionId" auf.</span><span class="sxs-lookup"><span data-stu-id="5163e-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="5163e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5163e-104">SYNTAX</span></span>

### <span data-ttu-id="5163e-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="5163e-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5163e-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5163e-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5163e-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="5163e-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5163e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5163e-108">DESCRIPTION</span></span>
<span data-ttu-id="5163e-109">Ruft eine "ExpressRouteGateway"-Ressource mit "ResourceGroupName" und "GatewayName OR" ab und listet alle Gateways nach "ResourceGroupName" oder "SubscriptionId" auf.</span><span class="sxs-lookup"><span data-stu-id="5163e-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="5163e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5163e-110">EXAMPLES</span></span>

### <span data-ttu-id="5163e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5163e-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"

ResourceGroupName   : testRG
Name                : testExpressRoutegw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="5163e-112">Im vorstehenden Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtuelles Netzwerk und ein virtueller Hub in der Us-amerikanischen Westzentrale in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="5163e-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5163e-113">Anschließend wird im virtuellen Hub ein "ExpressRoute"-Gateway mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="5163e-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="5163e-114">Anschließend ruft es das ExpressRouteGateway unter Verwendung seines resourceGroupName und des Gatewaynamens ab.</span><span class="sxs-lookup"><span data-stu-id="5163e-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="5163e-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5163e-115">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteGateway -Name test*

ResourceGroupName   : testRG
Name                : testExpressRoutegw1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw1
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : testExpressRoutegw2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw2
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="5163e-116">Mit diesem Befehl werden alle ExpressRouteGateways erhalten, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="5163e-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="5163e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5163e-117">PARAMETERS</span></span>

### <span data-ttu-id="5163e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5163e-118">-DefaultProfile</span></span>
<span data-ttu-id="5163e-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5163e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5163e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5163e-120">-Name</span></span>
<span data-ttu-id="5163e-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="5163e-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, ExpressRouteGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="5163e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5163e-122">-ResourceGroupName</span></span>
<span data-ttu-id="5163e-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5163e-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="5163e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5163e-124">-ResourceId</span></span>
<span data-ttu-id="5163e-125">Die Azure-Ressourcen-ID für das zu löschende expressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="5163e-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5163e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5163e-126">CommonParameters</span></span>
<span data-ttu-id="5163e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5163e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5163e-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5163e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5163e-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5163e-129">INPUTS</span></span>

### <span data-ttu-id="5163e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5163e-130">System.String</span></span>

## <span data-ttu-id="5163e-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5163e-131">OUTPUTS</span></span>

### <span data-ttu-id="5163e-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="5163e-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="5163e-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5163e-133">NOTES</span></span>

## <span data-ttu-id="5163e-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5163e-134">RELATED LINKS</span></span>
