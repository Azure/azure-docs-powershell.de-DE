---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: c820d44ed8c3d32feb3f1d63d2b52a487c27f0dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945826"
---
# <span data-ttu-id="4f22b-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4f22b-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="4f22b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f22b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f22b-103">Entfernt eine Subnetzkonfiguration aus einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4f22b-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="4f22b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f22b-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f22b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f22b-105">DESCRIPTION</span></span>
<span data-ttu-id="4f22b-106">Das **Cmdlet Remove-AzVirtualNetworkSubnetConfig** entfernt ein Subnetz aus einem virtuellen Azure-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4f22b-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="4f22b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f22b-107">EXAMPLES</span></span>

### <span data-ttu-id="4f22b-108">1: Entfernen eines Subnetzes aus einem virtuellen Netzwerk und Aktualisieren des virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="4f22b-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
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

<span data-ttu-id="4f22b-109">In diesem Beispiel werden eine Ressourcengruppe und ein virtuelles Netzwerk mit zwei Subnetzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="4f22b-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="4f22b-110">Anschließend wird der Befehl Remove-AzVirtualNetworkSubnetConfig verwendet, um das Back-End-Subnetz aus der Speicherdarstellung des virtuellen Netzwerks zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4f22b-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="4f22b-111">Set-AzVirtualNetwork wird dann aufgerufen, um das virtuelle Netzwerk auf der Serverseite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4f22b-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="4f22b-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4f22b-112">PARAMETERS</span></span>

### <span data-ttu-id="4f22b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f22b-113">-DefaultProfile</span></span>
<span data-ttu-id="4f22b-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f22b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f22b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4f22b-115">-Name</span></span>
<span data-ttu-id="4f22b-116">Gibt den Namen der zu entfernenden Subnetzkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="4f22b-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="4f22b-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f22b-117">-VirtualNetwork</span></span>
<span data-ttu-id="4f22b-118">Gibt das **VirtualNetwork-Objekt** an, das die zu entfernende Subnetzkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="4f22b-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="4f22b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f22b-119">CommonParameters</span></span>
<span data-ttu-id="4f22b-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f22b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f22b-121">Weitere Informationen finden Sie unter [about_CommonParameters] ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f22b-121">For more information, see [about_CommonParameters] (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f22b-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f22b-122">INPUTS</span></span>

### <span data-ttu-id="4f22b-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f22b-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4f22b-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f22b-124">OUTPUTS</span></span>

### <span data-ttu-id="4f22b-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f22b-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4f22b-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4f22b-126">NOTES</span></span>

## <span data-ttu-id="4f22b-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4f22b-127">RELATED LINKS</span></span>

[<span data-ttu-id="4f22b-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4f22b-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4f22b-129">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4f22b-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4f22b-130">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4f22b-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4f22b-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4f22b-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


