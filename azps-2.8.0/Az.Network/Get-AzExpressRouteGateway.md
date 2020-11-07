---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: d5314453be4d2f9042fd5034cc864d94caf1dbd1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821843"
---
# <span data-ttu-id="8f912-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="8f912-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="8f912-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f912-102">SYNOPSIS</span></span>
<span data-ttu-id="8f912-103">Ruft eine ExpressRouteGateway-Ressource mit ResourceGroupName und Gatewayname ab oder listet alle Gateways nach ResourceGroupName oder Abonnement-Nr auf.</span><span class="sxs-lookup"><span data-stu-id="8f912-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="8f912-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f912-104">SYNTAX</span></span>

### <span data-ttu-id="8f912-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f912-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f912-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f912-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f912-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="8f912-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f912-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f912-108">DESCRIPTION</span></span>
<span data-ttu-id="8f912-109">Ruft eine ExpressRouteGateway-Ressource mit ResourceGroupName und Gatewayname ab oder listet alle Gateways nach ResourceGroupName oder Abonnement-Nr auf.</span><span class="sxs-lookup"><span data-stu-id="8f912-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="8f912-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f912-110">EXAMPLES</span></span>

### <span data-ttu-id="8f912-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8f912-111">Example 1</span></span>

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

<span data-ttu-id="8f912-112">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuelles Drehkreuz in West Central US in der Ressourcengruppe "testRG" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f912-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="8f912-113">Anschließend wird ein Express Route-Gateway im virtuellen Hub mit zwei Skaleneinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="8f912-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="8f912-114">Anschließend wird die ExpressRouteGateway-Schnittstelle unter Verwendung ihrer resourceGroupName und des Gateway-namens abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8f912-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="8f912-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8f912-115">Example 2</span></span>

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

<span data-ttu-id="8f912-116">Dieser Befehl erhält alle ExpressRouteGateways, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="8f912-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="8f912-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f912-117">PARAMETERS</span></span>

### <span data-ttu-id="8f912-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f912-118">-DefaultProfile</span></span>
<span data-ttu-id="8f912-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f912-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f912-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8f912-120">-Name</span></span>
<span data-ttu-id="8f912-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8f912-121">The resource name.</span></span>

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

### <span data-ttu-id="8f912-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f912-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f912-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8f912-123">The resource group name.</span></span>

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

### <span data-ttu-id="8f912-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8f912-124">-ResourceId</span></span>
<span data-ttu-id="8f912-125">Die Azure-Ressourcen-ID für die expressRouteGateway, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f912-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="8f912-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f912-126">CommonParameters</span></span>
<span data-ttu-id="8f912-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f912-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f912-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f912-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f912-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f912-129">INPUTS</span></span>

### <span data-ttu-id="8f912-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8f912-130">System.String</span></span>

## <span data-ttu-id="8f912-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f912-131">OUTPUTS</span></span>

### <span data-ttu-id="8f912-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="8f912-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="8f912-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f912-133">NOTES</span></span>

## <span data-ttu-id="8f912-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f912-134">RELATED LINKS</span></span>
