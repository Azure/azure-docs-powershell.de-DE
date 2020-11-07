---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: dc780e4b05b2f0ccb92f014f658a9b21aa1bd224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843564"
---
# <span data-ttu-id="783b9-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="783b9-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="783b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="783b9-102">SYNOPSIS</span></span>
<span data-ttu-id="783b9-103">Legt den Zielstatus für ein virtuelles Netzwerk fest.</span><span class="sxs-lookup"><span data-stu-id="783b9-103">Sets the goal state for a virtual network.</span></span>

## <span data-ttu-id="783b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="783b9-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="783b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="783b9-105">DESCRIPTION</span></span>
<span data-ttu-id="783b9-106">Das Cmdlet " **Set-AzVirtualNetwork** " legt den Zielstatus für ein Azure-virtuelles Netzwerk fest.</span><span class="sxs-lookup"><span data-stu-id="783b9-106">The **Set-AzVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="783b9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="783b9-107">EXAMPLES</span></span>

### <span data-ttu-id="783b9-108">1: erstellt ein virtuelles Netzwerk und entfernt eines seiner Subnetze</span><span class="sxs-lookup"><span data-stu-id="783b9-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="783b9-109">In diesem Beispiel wird ein virtuelles Netzwerk mit zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="783b9-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="783b9-110">Anschließend wird ein Subnetz aus der speicherinternen Darstellung des virtuellen Netzwerks entfernt.</span><span class="sxs-lookup"><span data-stu-id="783b9-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="783b9-111">Das Cmdlet Set-AzVirtualNetwork wird dann verwendet, um den geänderten virtuellen Netzwerkzustand auf der Dienstseite zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="783b9-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="783b9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="783b9-112">PARAMETERS</span></span>

### <span data-ttu-id="783b9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="783b9-113">-AsJob</span></span>
<span data-ttu-id="783b9-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="783b9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="783b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="783b9-115">-DefaultProfile</span></span>
<span data-ttu-id="783b9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="783b9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="783b9-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="783b9-117">-VirtualNetwork</span></span>
<span data-ttu-id="783b9-118">Gibt ein **VirtualNetwork** -Objekt an, das den Zielzustand darstellt.</span><span class="sxs-lookup"><span data-stu-id="783b9-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="783b9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="783b9-119">CommonParameters</span></span>
<span data-ttu-id="783b9-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="783b9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="783b9-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="783b9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="783b9-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="783b9-122">INPUTS</span></span>

### <span data-ttu-id="783b9-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="783b9-123">PSVirtualNetwork</span></span>
<span data-ttu-id="783b9-124">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="783b9-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="783b9-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="783b9-125">OUTPUTS</span></span>

### <span data-ttu-id="783b9-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="783b9-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="783b9-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="783b9-127">NOTES</span></span>

## <span data-ttu-id="783b9-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="783b9-128">RELATED LINKS</span></span>

[<span data-ttu-id="783b9-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="783b9-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="783b9-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="783b9-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="783b9-131">Neu – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="783b9-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="783b9-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="783b9-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


