---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7d90ffff788239996f7b79f7e56493611db86e04
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300587"
---
# <span data-ttu-id="616a1-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="616a1-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="616a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="616a1-102">SYNOPSIS</span></span>
<span data-ttu-id="616a1-103">Entfernt eine Subnetzkonfiguration aus einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="616a1-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="616a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="616a1-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="616a1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="616a1-105">DESCRIPTION</span></span>
<span data-ttu-id="616a1-106">Das **Cmdlet "Remove-AzVirtualNetworkSubnetConfig"** entfernt ein Subnetz aus einem virtuellen Azure-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="616a1-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="616a1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="616a1-107">EXAMPLES</span></span>

### <span data-ttu-id="616a1-108">1: Entfernen eines Subnetzes aus einem virtuellen Netzwerk und Aktualisieren des virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="616a1-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="616a1-109">In diesem Beispiel werden eine Ressourcengruppe und ein virtuelles Netzwerk mit zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="616a1-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="616a1-110">Anschließend wird der Befehl Remove-AzVirtualNetworkSubnetConfig verwendet, um das Back-End-Subnetz aus der Speicherdarstellung des virtuellen Netzwerks zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="616a1-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="616a1-111">Set-AzVirtualNetwork wird dann aufgerufen, um das virtuelle Netzwerk auf serverseitig zu ändern.</span><span class="sxs-lookup"><span data-stu-id="616a1-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="616a1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="616a1-112">PARAMETERS</span></span>

### <span data-ttu-id="616a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="616a1-113">-DefaultProfile</span></span>
<span data-ttu-id="616a1-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="616a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="616a1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="616a1-115">-Name</span></span>
<span data-ttu-id="616a1-116">Gibt den Namen der zu entfernenden Subnetzkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="616a1-116">Specifies the name of the subnet configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="616a1-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="616a1-117">-VirtualNetwork</span></span>
<span data-ttu-id="616a1-118">Gibt das **VirtualNetwork-Objekt** an, das die zu entfernende Subnetzkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="616a1-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="616a1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="616a1-119">CommonParameters</span></span>
<span data-ttu-id="616a1-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="616a1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="616a1-121">Weitere Informationen finden Sie unter [about_CommonParameters] ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="616a1-121">For more information, see [about_CommonParameters] (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="616a1-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="616a1-122">INPUTS</span></span>

### <span data-ttu-id="616a1-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="616a1-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="616a1-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="616a1-124">OUTPUTS</span></span>

### <span data-ttu-id="616a1-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="616a1-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="616a1-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="616a1-126">NOTES</span></span>

## <span data-ttu-id="616a1-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="616a1-127">RELATED LINKS</span></span>

[<span data-ttu-id="616a1-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="616a1-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="616a1-129">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="616a1-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="616a1-130">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="616a1-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="616a1-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="616a1-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


