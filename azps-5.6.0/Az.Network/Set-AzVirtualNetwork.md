---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 1c5a5bc119c481c47c865ca72896b832f3a82b2b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942400"
---
# <span data-ttu-id="f2ed4-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f2ed4-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="f2ed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ed4-103">Aktualisiert ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-103">Updates a virtual network.</span></span>

## <span data-ttu-id="f2ed4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2ed4-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2ed4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2ed4-105">DESCRIPTION</span></span>
<span data-ttu-id="f2ed4-106">Das **Cmdlet Set-AzVirtualNetwork** aktualisiert ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="f2ed4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f2ed4-107">EXAMPLES</span></span>

### <span data-ttu-id="f2ed4-108">1: Erstellt ein virtuelles Netzwerk und entfernt eines seiner Subnetze</span><span class="sxs-lookup"><span data-stu-id="f2ed4-108">1: Creates a virtual network and removes one of its subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus ## Create resource group 
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create frontend subnet 
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="f2ed4-109">In diesem Beispiel wird ein virtuelles Netzwerk namens TestResourceGroup mit zwei Subnetzen erstellt: frontendSubnet und back-EndSubnet.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="f2ed4-110">Anschließend wird das Back-EndSubnet-Subnetz aus der Speicherdarstellung des virtuellen Netzwerks entfernt.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="f2ed4-111">Das Set-AzVirtualNetwork-Cmdlet wird dann zum Schreiben des geänderten virtuellen Netzwerkzustands auf der Dienstseite verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="f2ed4-112">Wenn das Set-AzVirtualNetwork-Cmdlet ausgeführt wird, wird das backendSubnet entfernt.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="f2ed4-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f2ed4-113">PARAMETERS</span></span>

### <span data-ttu-id="f2ed4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2ed4-114">-AsJob</span></span>
<span data-ttu-id="f2ed4-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f2ed4-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ed4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ed4-116">-DefaultProfile</span></span>
<span data-ttu-id="f2ed4-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2ed4-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f2ed4-118">-VirtualNetwork</span></span>
<span data-ttu-id="f2ed4-119">Gibt ein virtuelles Netzwerkobjekt an, das den Zustand darstellt, auf den das virtuelle Netzwerk festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2ed4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ed4-120">CommonParameters</span></span>
<span data-ttu-id="f2ed4-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ed4-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2ed4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ed4-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f2ed4-123">INPUTS</span></span>

### <span data-ttu-id="f2ed4-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f2ed4-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="f2ed4-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f2ed4-125">OUTPUTS</span></span>

### <span data-ttu-id="f2ed4-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f2ed4-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="f2ed4-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f2ed4-127">NOTES</span></span>

## <span data-ttu-id="f2ed4-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f2ed4-128">RELATED LINKS</span></span>

[<span data-ttu-id="f2ed4-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f2ed4-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f2ed4-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f2ed4-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f2ed4-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f2ed4-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="f2ed4-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f2ed4-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


