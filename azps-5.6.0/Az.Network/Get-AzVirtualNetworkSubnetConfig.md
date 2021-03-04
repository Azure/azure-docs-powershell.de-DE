---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: bee7857751b9553314085ab3fee4f5edbadce1b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931752"
---
# <span data-ttu-id="5a75f-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5a75f-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="5a75f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a75f-102">SYNOPSIS</span></span>
<span data-ttu-id="5a75f-103">Ruft ein Subnetz in einem virtuellen Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="5a75f-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="5a75f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a75f-104">SYNTAX</span></span>

### <span data-ttu-id="5a75f-105">GetByVirtualNetwork (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a75f-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a75f-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a75f-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a75f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a75f-107">DESCRIPTION</span></span>
<span data-ttu-id="5a75f-108">Das **Get-AzVirtualNetworkSubnetConfig-Cmdlet** ruft eine oder mehrere Subnetzkonfigurationen in einem virtuellen Azure-Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="5a75f-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="5a75f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a75f-109">EXAMPLES</span></span>

### <span data-ttu-id="5a75f-110">1: Erhalten eines Subnetzes in einem virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="5a75f-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="5a75f-111">In diesem Beispiel werden eine Ressourcengruppe und ein virtuelles Netzwerk mit einem einzelnen Subnetz in dieser Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a75f-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="5a75f-112">Anschließend werden Daten zu diesem Subnetz abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5a75f-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="5a75f-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5a75f-113">PARAMETERS</span></span>

### <span data-ttu-id="5a75f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a75f-114">-DefaultProfile</span></span>
<span data-ttu-id="5a75f-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a75f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a75f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5a75f-116">-Name</span></span>
<span data-ttu-id="5a75f-117">Gibt den Namen der Subnetzkonfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5a75f-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5a75f-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a75f-118">-ResourceId</span></span>
<span data-ttu-id="5a75f-119">Gibt die Ressourcen-ID des Subnetzes an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5a75f-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5a75f-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5a75f-120">-VirtualNetwork</span></span>
<span data-ttu-id="5a75f-121">Gibt das **VirtualNetwork-Objekt** an, das die Subnetzkonfiguration enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5a75f-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5a75f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a75f-122">CommonParameters</span></span>
<span data-ttu-id="5a75f-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a75f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a75f-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a75f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a75f-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a75f-125">INPUTS</span></span>

### <span data-ttu-id="5a75f-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5a75f-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="5a75f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5a75f-127">System.String</span></span>

## <span data-ttu-id="5a75f-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a75f-128">OUTPUTS</span></span>

### <span data-ttu-id="5a75f-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5a75f-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5a75f-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5a75f-130">NOTES</span></span>

## <span data-ttu-id="5a75f-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5a75f-131">RELATED LINKS</span></span>

[<span data-ttu-id="5a75f-132">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5a75f-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5a75f-133">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5a75f-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5a75f-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5a75f-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5a75f-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5a75f-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
