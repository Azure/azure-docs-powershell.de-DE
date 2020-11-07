---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 3d3667e73988b50e5c7cab09d07c6ba1a32d072b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823792"
---
# <span data-ttu-id="864eb-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="864eb-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="864eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="864eb-102">SYNOPSIS</span></span>
<span data-ttu-id="864eb-103">Aktualisiert ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="864eb-103">Updates a virtual network.</span></span>

## <span data-ttu-id="864eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="864eb-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="864eb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="864eb-105">DESCRIPTION</span></span>
<span data-ttu-id="864eb-106">Das Cmdlet " **Satz-AzVirtualNetwork** " aktualisiert ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="864eb-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="864eb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="864eb-107">EXAMPLES</span></span>

### <span data-ttu-id="864eb-108">1: erstellt ein virtuelles Netzwerk und entfernt eines seiner Subnetze</span><span class="sxs-lookup"><span data-stu-id="864eb-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="864eb-109">In diesem Beispiel wird ein virtuelles Netzwerk mit dem Namen TestResourceGroup mit zwei Subnetzen erstellt: frontendSubnet und backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="864eb-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="864eb-110">Anschließend wird backendSubnet-Subnetz aus der speicherinternen Darstellung des virtuellen Netzwerks entfernt.</span><span class="sxs-lookup"><span data-stu-id="864eb-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="864eb-111">Das Cmdlet Set-AzVirtualNetwork wird dann verwendet, um den geänderten virtuellen Netzwerkzustand auf der Dienstseite zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="864eb-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="864eb-112">Wenn das Set-AzVirtualNetwork-Cmdlet ausgeführt wird, wird der backendSubnet entfernt.</span><span class="sxs-lookup"><span data-stu-id="864eb-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="864eb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="864eb-113">PARAMETERS</span></span>

### <span data-ttu-id="864eb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="864eb-114">-AsJob</span></span>
<span data-ttu-id="864eb-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="864eb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="864eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="864eb-116">-DefaultProfile</span></span>
<span data-ttu-id="864eb-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="864eb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="864eb-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="864eb-118">-VirtualNetwork</span></span>
<span data-ttu-id="864eb-119">Gibt ein virtuelles Netzwerkobjekt an, das den Zustand darstellt, in dem das virtuelle Netzwerk festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="864eb-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="864eb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864eb-120">CommonParameters</span></span>
<span data-ttu-id="864eb-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="864eb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864eb-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="864eb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864eb-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="864eb-123">INPUTS</span></span>

### <span data-ttu-id="864eb-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="864eb-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="864eb-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="864eb-125">OUTPUTS</span></span>

### <span data-ttu-id="864eb-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="864eb-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="864eb-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="864eb-127">NOTES</span></span>

## <span data-ttu-id="864eb-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="864eb-128">RELATED LINKS</span></span>

[<span data-ttu-id="864eb-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="864eb-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="864eb-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="864eb-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="864eb-131">Neu – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="864eb-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="864eb-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="864eb-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


