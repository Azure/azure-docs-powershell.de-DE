---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 22ea0a6a28a24503413fa9b8958002616c03b884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479662"
---
# <span data-ttu-id="0132a-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0132a-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="0132a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0132a-102">SYNOPSIS</span></span>
<span data-ttu-id="0132a-103">Legt den Zielstatus für ein virtuelles Netzwerk fest.</span><span class="sxs-lookup"><span data-stu-id="0132a-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0132a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0132a-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0132a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0132a-105">DESCRIPTION</span></span>
<span data-ttu-id="0132a-106">Das Cmdlet " **Set-AzureRmVirtualNetwork** " legt den Zielstatus für ein Azure-virtuelles Netzwerk fest.</span><span class="sxs-lookup"><span data-stu-id="0132a-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="0132a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0132a-107">EXAMPLES</span></span>

### <span data-ttu-id="0132a-108">1: erstellt ein virtuelles Netzwerk und entfernt eines seiner Subnetze</span><span class="sxs-lookup"><span data-stu-id="0132a-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="0132a-109">In diesem Beispiel wird ein virtuelles Netzwerk mit zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="0132a-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="0132a-110">Anschließend wird ein Subnetz aus der speicherinternen Darstellung des virtuellen Netzwerks entfernt.</span><span class="sxs-lookup"><span data-stu-id="0132a-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="0132a-111">Das Cmdlet Set-AzureRmVirtualNetwork wird dann verwendet, um den geänderten virtuellen Netzwerkzustand auf der Dienstseite zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="0132a-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="0132a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0132a-112">PARAMETERS</span></span>

### <span data-ttu-id="0132a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0132a-113">-AsJob</span></span>
<span data-ttu-id="0132a-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0132a-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0132a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0132a-115">-DefaultProfile</span></span>
<span data-ttu-id="0132a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0132a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0132a-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0132a-117">-VirtualNetwork</span></span>
<span data-ttu-id="0132a-118">Gibt ein **VirtualNetwork** -Objekt an, das den Zielzustand darstellt.</span><span class="sxs-lookup"><span data-stu-id="0132a-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0132a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0132a-119">CommonParameters</span></span>
<span data-ttu-id="0132a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0132a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0132a-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0132a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0132a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0132a-122">INPUTS</span></span>

### <span data-ttu-id="0132a-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0132a-123">PSVirtualNetwork</span></span>
<span data-ttu-id="0132a-124">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0132a-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="0132a-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0132a-125">OUTPUTS</span></span>

### <span data-ttu-id="0132a-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0132a-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="0132a-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="0132a-127">NOTES</span></span>

## <span data-ttu-id="0132a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0132a-128">RELATED LINKS</span></span>

[<span data-ttu-id="0132a-129">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0132a-129">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="0132a-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0132a-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="0132a-131">Neu – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0132a-131">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="0132a-132">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0132a-132">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


