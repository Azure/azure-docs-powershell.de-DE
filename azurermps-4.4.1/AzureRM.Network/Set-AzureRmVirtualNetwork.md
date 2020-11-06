---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: a5158b1c2d1439286295a2f84f7273b37d608161
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504822"
---
# <span data-ttu-id="51a6d-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51a6d-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="51a6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="51a6d-103">Legt den Zielstatus für ein virtuelles Netzwerk fest.</span><span class="sxs-lookup"><span data-stu-id="51a6d-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51a6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51a6d-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51a6d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51a6d-105">DESCRIPTION</span></span>
<span data-ttu-id="51a6d-106">Das Cmdlet " **Set-AzureRmVirtualNetwork** " legt den Zielstatus für ein Azure-virtuelles Netzwerk fest.</span><span class="sxs-lookup"><span data-stu-id="51a6d-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="51a6d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51a6d-107">EXAMPLES</span></span>

### <span data-ttu-id="51a6d-108">1: erstellt ein virtuelles Netzwerk und entfernt eines seiner Subnetze</span><span class="sxs-lookup"><span data-stu-id="51a6d-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="51a6d-109">In diesem Beispiel wird ein virtuelles Netzwerk mit zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="51a6d-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="51a6d-110">Anschließend wird ein Subnetz aus der speicherinternen Darstellung des virtuellen Netzwerks entfernt.</span><span class="sxs-lookup"><span data-stu-id="51a6d-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="51a6d-111">Das Cmdlet Set-AzureRmVirtualNetwork wird dann verwendet, um den geänderten virtuellen Netzwerkzustand auf der Dienstseite zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="51a6d-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="51a6d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="51a6d-112">PARAMETERS</span></span>

### <span data-ttu-id="51a6d-113">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51a6d-113">-VirtualNetwork</span></span>
<span data-ttu-id="51a6d-114">Gibt ein **VirtualNetwork** -Objekt an, das den Zielzustand darstellt.</span><span class="sxs-lookup"><span data-stu-id="51a6d-114">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="51a6d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a6d-115">-DefaultProfile</span></span>
<span data-ttu-id="51a6d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51a6d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51a6d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a6d-117">CommonParameters</span></span>
<span data-ttu-id="51a6d-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51a6d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a6d-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51a6d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a6d-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51a6d-120">INPUTS</span></span>

### <span data-ttu-id="51a6d-121">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51a6d-121">PSVirtualNetwork</span></span>
<span data-ttu-id="51a6d-122">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="51a6d-122">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="51a6d-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51a6d-123">OUTPUTS</span></span>

### <span data-ttu-id="51a6d-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51a6d-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="51a6d-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="51a6d-125">NOTES</span></span>

## <span data-ttu-id="51a6d-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51a6d-126">RELATED LINKS</span></span>

[<span data-ttu-id="51a6d-127">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51a6d-127">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="51a6d-128">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51a6d-128">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="51a6d-129">Neu – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51a6d-129">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="51a6d-130">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51a6d-130">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


