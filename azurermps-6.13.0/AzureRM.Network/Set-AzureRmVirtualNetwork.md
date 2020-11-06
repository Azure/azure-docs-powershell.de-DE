---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 2a81b7bf5420bdbf4fa5252d71c511c7152e47fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482198"
---
# <span data-ttu-id="285b9-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="285b9-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="285b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="285b9-102">SYNOPSIS</span></span>
<span data-ttu-id="285b9-103">Legt den Zielstatus für ein virtuelles Netzwerk fest.</span><span class="sxs-lookup"><span data-stu-id="285b9-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="285b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="285b9-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="285b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="285b9-105">DESCRIPTION</span></span>
<span data-ttu-id="285b9-106">Das Cmdlet " **Set-AzureRmVirtualNetwork** " legt den Zielstatus für ein Azure-virtuelles Netzwerk fest.</span><span class="sxs-lookup"><span data-stu-id="285b9-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="285b9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="285b9-107">EXAMPLES</span></span>

### <span data-ttu-id="285b9-108">1: erstellt ein virtuelles Netzwerk und entfernt eines seiner Subnetze</span><span class="sxs-lookup"><span data-stu-id="285b9-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzureRmVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="285b9-109">In diesem Beispiel wird ein virtuelles Netzwerk mit dem Namen TestResourceGroup mit zwei Subnetzen erstellt: frontendSubnet und backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="285b9-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="285b9-110">Anschließend wird backendSubnet-Subnetz aus der speicherinternen Darstellung des virtuellen Netzwerks entfernt.</span><span class="sxs-lookup"><span data-stu-id="285b9-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="285b9-111">Das Cmdlet Set-AzureRmVirtualNetwork wird dann verwendet, um den geänderten virtuellen Netzwerkzustand auf der Dienstseite zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="285b9-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="285b9-112">Wenn das Set-AzureRmVirtualNetwork-Cmdlet ausgeführt wird, wird der backendSubnet entfernt.</span><span class="sxs-lookup"><span data-stu-id="285b9-112">When the Set-AzureRmVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="285b9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="285b9-113">PARAMETERS</span></span>

### <span data-ttu-id="285b9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="285b9-114">-AsJob</span></span>
<span data-ttu-id="285b9-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="285b9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="285b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285b9-116">-DefaultProfile</span></span>
<span data-ttu-id="285b9-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="285b9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="285b9-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="285b9-118">-VirtualNetwork</span></span>
<span data-ttu-id="285b9-119">Gibt ein **VirtualNetwork** -Objekt an, das den Zielzustand darstellt.</span><span class="sxs-lookup"><span data-stu-id="285b9-119">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="285b9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285b9-120">CommonParameters</span></span>
<span data-ttu-id="285b9-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="285b9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285b9-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="285b9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285b9-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="285b9-123">INPUTS</span></span>

### <span data-ttu-id="285b9-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="285b9-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>
<span data-ttu-id="285b9-125">Parameter: VirtualNetwork (ByValue)</span><span class="sxs-lookup"><span data-stu-id="285b9-125">Parameters: VirtualNetwork (ByValue)</span></span>

## <span data-ttu-id="285b9-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="285b9-126">OUTPUTS</span></span>

### <span data-ttu-id="285b9-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="285b9-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="285b9-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="285b9-128">NOTES</span></span>

## <span data-ttu-id="285b9-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="285b9-129">RELATED LINKS</span></span>

[<span data-ttu-id="285b9-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="285b9-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="285b9-131">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="285b9-131">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="285b9-132">Neu – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="285b9-132">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="285b9-133">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="285b9-133">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


