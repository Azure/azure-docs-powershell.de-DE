---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003566"
---
# <span data-ttu-id="77219-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="77219-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="77219-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77219-102">SYNOPSIS</span></span>
<span data-ttu-id="77219-103">Ruft eine ExpressRouteGateway-Ressource mit ResourceGroupName und Gatewayname ab oder listet alle Gateways nach ResourceGroupName oder Abonnement-Nr auf.</span><span class="sxs-lookup"><span data-stu-id="77219-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="77219-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77219-104">SYNTAX</span></span>

### <span data-ttu-id="77219-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="77219-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77219-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77219-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77219-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="77219-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77219-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77219-108">DESCRIPTION</span></span>
<span data-ttu-id="77219-109">Ruft eine ExpressRouteGateway-Ressource mit ResourceGroupName und Gatewayname ab oder listet alle Gateways nach ResourceGroupName oder Abonnement-Nr auf.</span><span class="sxs-lookup"><span data-stu-id="77219-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="77219-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77219-110">EXAMPLES</span></span>

### <span data-ttu-id="77219-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="77219-111">Example 1</span></span>

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

<span data-ttu-id="77219-112">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuelles Drehkreuz in West Central US in der Ressourcengruppe "testRG" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="77219-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="77219-113">Anschließend wird ein Express Route-Gateway im virtuellen Hub mit zwei Skaleneinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="77219-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="77219-114">Anschließend wird die ExpressRouteGateway-Schnittstelle unter Verwendung ihrer resourceGroupName und des Gateway-namens abgerufen.</span><span class="sxs-lookup"><span data-stu-id="77219-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="77219-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="77219-115">Example 2</span></span>

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

<span data-ttu-id="77219-116">Dieser Befehl erhält alle ExpressRouteGateways, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="77219-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="77219-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="77219-117">PARAMETERS</span></span>

### <span data-ttu-id="77219-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77219-118">-DefaultProfile</span></span>
<span data-ttu-id="77219-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="77219-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77219-120">-Name</span><span class="sxs-lookup"><span data-stu-id="77219-120">-Name</span></span>
<span data-ttu-id="77219-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="77219-121">The resource name.</span></span>

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

### <span data-ttu-id="77219-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77219-122">-ResourceGroupName</span></span>
<span data-ttu-id="77219-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="77219-123">The resource group name.</span></span>

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

### <span data-ttu-id="77219-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="77219-124">-ResourceId</span></span>
<span data-ttu-id="77219-125">Die Azure-Ressourcen-ID für die expressRouteGateway, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="77219-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="77219-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77219-126">CommonParameters</span></span>
<span data-ttu-id="77219-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77219-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77219-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77219-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77219-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77219-129">INPUTS</span></span>

### <span data-ttu-id="77219-130">System. String</span><span class="sxs-lookup"><span data-stu-id="77219-130">System.String</span></span>

## <span data-ttu-id="77219-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77219-131">OUTPUTS</span></span>

### <span data-ttu-id="77219-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="77219-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="77219-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="77219-133">NOTES</span></span>

## <span data-ttu-id="77219-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77219-134">RELATED LINKS</span></span>
