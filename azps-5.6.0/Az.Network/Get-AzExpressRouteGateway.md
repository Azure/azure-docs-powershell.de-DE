---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 0d7bec7a40ced6ddcd5ffc61f48f233cea115459
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947347"
---
# <span data-ttu-id="edb08-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="edb08-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="edb08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edb08-102">SYNOPSIS</span></span>
<span data-ttu-id="edb08-103">Ruft eine ExpressRouteGateway-Ressource mit ResourceGroupName und GatewayName ODER ab und listet alle Gateways nach ResourceGroupName oder SubscriptionId auf.</span><span class="sxs-lookup"><span data-stu-id="edb08-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="edb08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edb08-104">SYNTAX</span></span>

### <span data-ttu-id="edb08-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="edb08-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edb08-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb08-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edb08-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="edb08-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edb08-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edb08-108">DESCRIPTION</span></span>
<span data-ttu-id="edb08-109">Ruft eine ExpressRouteGateway-Ressource mit ResourceGroupName und GatewayName ODER ab und listet alle Gateways nach ResourceGroupName oder SubscriptionId auf.</span><span class="sxs-lookup"><span data-stu-id="edb08-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="edb08-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="edb08-110">EXAMPLES</span></span>

### <span data-ttu-id="edb08-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="edb08-111">Example 1</span></span>

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

<span data-ttu-id="edb08-112">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in West Central US in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="edb08-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="edb08-113">Anschließend wird im virtuellen Hub ein ExpressRoute-Gateway mit zwei Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="edb08-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="edb08-114">Anschließend ruft es das ExpressRouteGateway mit seinem resourceGroupName und dem Gatewaynamen ab.</span><span class="sxs-lookup"><span data-stu-id="edb08-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="edb08-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="edb08-115">Example 2</span></span>

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

<span data-ttu-id="edb08-116">Dieser Befehl zeigt alle ExpressRouteGateways an, die mit "test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="edb08-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="edb08-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="edb08-117">PARAMETERS</span></span>

### <span data-ttu-id="edb08-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb08-118">-DefaultProfile</span></span>
<span data-ttu-id="edb08-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="edb08-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edb08-120">-Name</span><span class="sxs-lookup"><span data-stu-id="edb08-120">-Name</span></span>
<span data-ttu-id="edb08-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="edb08-121">The resource name.</span></span>

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

### <span data-ttu-id="edb08-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb08-122">-ResourceGroupName</span></span>
<span data-ttu-id="edb08-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="edb08-123">The resource group name.</span></span>

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

### <span data-ttu-id="edb08-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edb08-124">-ResourceId</span></span>
<span data-ttu-id="edb08-125">Die Azure-Ressourcen-ID für das expressRouteGateway, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="edb08-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="edb08-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb08-126">CommonParameters</span></span>
<span data-ttu-id="edb08-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb08-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb08-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edb08-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb08-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="edb08-129">INPUTS</span></span>

### <span data-ttu-id="edb08-130">System.String</span><span class="sxs-lookup"><span data-stu-id="edb08-130">System.String</span></span>

## <span data-ttu-id="edb08-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="edb08-131">OUTPUTS</span></span>

### <span data-ttu-id="edb08-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="edb08-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="edb08-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="edb08-133">NOTES</span></span>

## <span data-ttu-id="edb08-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="edb08-134">RELATED LINKS</span></span>
