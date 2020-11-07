---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 40f84388caed0d332c36ee398e842ae00f2f353f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848695"
---
# <span data-ttu-id="02254-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02254-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="02254-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02254-102">SYNOPSIS</span></span>
<span data-ttu-id="02254-103">Legt den Zielstatus für ein virtuelles Netzwerk fest.</span><span class="sxs-lookup"><span data-stu-id="02254-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02254-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02254-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02254-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02254-105">DESCRIPTION</span></span>
<span data-ttu-id="02254-106">Das Cmdlet " **Set-AzureRmVirtualNetwork** " legt den Zielstatus für ein Azure-virtuelles Netzwerk fest.</span><span class="sxs-lookup"><span data-stu-id="02254-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="02254-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02254-107">EXAMPLES</span></span>

### <span data-ttu-id="02254-108">1: erstellt ein virtuelles Netzwerk und entfernt eines seiner Subnetze</span><span class="sxs-lookup"><span data-stu-id="02254-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="02254-109">In diesem Beispiel wird ein virtuelles Netzwerk mit zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="02254-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="02254-110">Anschließend wird ein Subnetz aus der speicherinternen Darstellung des virtuellen Netzwerks entfernt.</span><span class="sxs-lookup"><span data-stu-id="02254-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="02254-111">Das Cmdlet Set-AzureRmVirtualNetwork wird dann verwendet, um den geänderten virtuellen Netzwerkzustand auf der Dienstseite zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="02254-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="02254-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="02254-112">PARAMETERS</span></span>

### <span data-ttu-id="02254-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02254-113">-AsJob</span></span>
<span data-ttu-id="02254-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="02254-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02254-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02254-115">-DefaultProfile</span></span>
<span data-ttu-id="02254-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02254-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02254-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02254-117">-VirtualNetwork</span></span>
<span data-ttu-id="02254-118">Gibt ein **VirtualNetwork** -Objekt an, das den Zielzustand darstellt.</span><span class="sxs-lookup"><span data-stu-id="02254-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="02254-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02254-119">CommonParameters</span></span>
<span data-ttu-id="02254-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02254-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02254-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02254-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02254-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02254-122">INPUTS</span></span>

### <span data-ttu-id="02254-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02254-123">PSVirtualNetwork</span></span>
<span data-ttu-id="02254-124">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="02254-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="02254-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02254-125">OUTPUTS</span></span>

### <span data-ttu-id="02254-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02254-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="02254-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="02254-127">NOTES</span></span>

## <span data-ttu-id="02254-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02254-128">RELATED LINKS</span></span>

[<span data-ttu-id="02254-129">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02254-129">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="02254-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02254-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="02254-131">Neu – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02254-131">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="02254-132">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02254-132">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


