---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: dcc5e688838508e6917a6732b24d7de3b27b2737
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458815"
---
# <span data-ttu-id="d122b-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d122b-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="d122b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d122b-102">SYNOPSIS</span></span>
<span data-ttu-id="d122b-103">Ruft ein Subnetz in einem virtuellen Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="d122b-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="d122b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d122b-104">SYNTAX</span></span>

### <span data-ttu-id="d122b-105">GetByVirtualNetwork (Standard)</span><span class="sxs-lookup"><span data-stu-id="d122b-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d122b-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d122b-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d122b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d122b-107">DESCRIPTION</span></span>
<span data-ttu-id="d122b-108">Das **Cmdlet "Get-AzVirtualNetworkSubnetConfig"** ruft eine oder mehrere Subnetzkonfigurationen in einem virtuellen Azure-Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="d122b-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="d122b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d122b-109">EXAMPLES</span></span>

### <span data-ttu-id="d122b-110">1: Erhalten eines Subnetzes in einem virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="d122b-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="d122b-111">In diesem Beispiel werden eine Ressourcengruppe und ein virtuelles Netzwerk mit einem einzelnen Subnetz in dieser Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="d122b-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="d122b-112">Anschließend werden Daten zu diesem Subnetz abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d122b-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="d122b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d122b-113">PARAMETERS</span></span>

### <span data-ttu-id="d122b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d122b-114">-DefaultProfile</span></span>
<span data-ttu-id="d122b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d122b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d122b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d122b-116">-Name</span></span>
<span data-ttu-id="d122b-117">Gibt den Namen der Subnetzkonfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d122b-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d122b-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d122b-118">-ResourceId</span></span>
<span data-ttu-id="d122b-119">Gibt die Ressourcen-ID des Subnetzes an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d122b-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d122b-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d122b-120">-VirtualNetwork</span></span>
<span data-ttu-id="d122b-121">Gibt das **VirtualNetwork-Objekt** an, das die Subnetzkonfiguration enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d122b-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d122b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d122b-122">CommonParameters</span></span>
<span data-ttu-id="d122b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d122b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d122b-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d122b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d122b-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d122b-125">INPUTS</span></span>

### <span data-ttu-id="d122b-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d122b-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="d122b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d122b-127">System.String</span></span>

## <span data-ttu-id="d122b-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d122b-128">OUTPUTS</span></span>

### <span data-ttu-id="d122b-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="d122b-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="d122b-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d122b-130">NOTES</span></span>

## <span data-ttu-id="d122b-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d122b-131">RELATED LINKS</span></span>

[<span data-ttu-id="d122b-132">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d122b-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d122b-133">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d122b-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d122b-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d122b-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d122b-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d122b-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
