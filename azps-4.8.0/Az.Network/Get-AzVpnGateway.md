---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: b6537b9b8501aa2ec0aa76c9ede080893bf136ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166297"
---
# <span data-ttu-id="970ed-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="970ed-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="970ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="970ed-102">SYNOPSIS</span></span>
<span data-ttu-id="970ed-103">Ruft eine VpnGateway-Ressource mit ResourceGroupName und Gatewayname ab oder listet alle Gateways nach ResourceGroupName oder Abonnement-Nr auf.</span><span class="sxs-lookup"><span data-stu-id="970ed-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="970ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="970ed-104">SYNTAX</span></span>

### <span data-ttu-id="970ed-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="970ed-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="970ed-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="970ed-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="970ed-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="970ed-107">DESCRIPTION</span></span>
<span data-ttu-id="970ed-108">Ruft eine VpnGateway-Ressource mit ResourceGroupName und Gatewayname ab oder listet alle Gateways nach ResourceGroupName oder Abonnement-Nr auf.</span><span class="sxs-lookup"><span data-stu-id="970ed-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="970ed-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="970ed-109">EXAMPLES</span></span>

### <span data-ttu-id="970ed-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="970ed-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="970ed-111">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuelles Drehkreuz in West US in der Ressourcengruppe "testRG" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="970ed-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="970ed-112">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="970ed-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="970ed-113">Anschließend wird die VpnGateway-Schnittstelle unter Verwendung ihrer resourceGroupName und des Gateway-namens abgerufen.</span><span class="sxs-lookup"><span data-stu-id="970ed-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="970ed-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="970ed-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="970ed-115">Dieses Cmdlet ruft alle Gateways ab, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="970ed-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="970ed-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="970ed-116">PARAMETERS</span></span>

### <span data-ttu-id="970ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="970ed-117">-DefaultProfile</span></span>
<span data-ttu-id="970ed-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="970ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="970ed-119">-Name</span><span class="sxs-lookup"><span data-stu-id="970ed-119">-Name</span></span>
<span data-ttu-id="970ed-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="970ed-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="970ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="970ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="970ed-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="970ed-122">The resource group name.</span></span>

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

### <span data-ttu-id="970ed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="970ed-123">CommonParameters</span></span>
<span data-ttu-id="970ed-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="970ed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="970ed-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="970ed-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="970ed-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="970ed-126">INPUTS</span></span>

### <span data-ttu-id="970ed-127">Keine</span><span class="sxs-lookup"><span data-stu-id="970ed-127">None</span></span>

## <span data-ttu-id="970ed-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="970ed-128">OUTPUTS</span></span>

### <span data-ttu-id="970ed-129">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="970ed-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="970ed-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="970ed-130">NOTES</span></span>

## <span data-ttu-id="970ed-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="970ed-131">RELATED LINKS</span></span>

[<span data-ttu-id="970ed-132">Neu – AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="970ed-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="970ed-133">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="970ed-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="970ed-134">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="970ed-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
