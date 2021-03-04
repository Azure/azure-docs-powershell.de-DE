---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: 511ff37071767c9e28164fcf93e985eb773297f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930976"
---
# <span data-ttu-id="aace9-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="aace9-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="aace9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aace9-102">SYNOPSIS</span></span>
<span data-ttu-id="aace9-103">Erstellt ein Peering zwischen zwei virtuellen Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="aace9-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="aace9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aace9-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aace9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aace9-105">DESCRIPTION</span></span>
<span data-ttu-id="aace9-106">Das **Add-AzVirtualNetworkPeering-Cmdlet** erstellt ein Peering zwischen zwei virtuellen Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="aace9-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="aace9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aace9-107">EXAMPLES</span></span>

### <span data-ttu-id="aace9-108">Beispiel 1: Erstellen eines Peerings zwischen zwei virtuellen Netzwerken in derselben Region</span><span class="sxs-lookup"><span data-stu-id="aace9-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="aace9-109">Beachten Sie, dass ein Peeringlink von vnet1 zu vnet2 und umgekehrt erstellt werden muss, damit Peering funktioniert.</span><span class="sxs-lookup"><span data-stu-id="aace9-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="aace9-110">Beispiel 2: Erstellen eines Peerings zwischen zwei virtuellen Netzwerken in verschiedenen Regionen</span><span class="sxs-lookup"><span data-stu-id="aace9-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location canadacentral

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="aace9-111">Hier wird "myVnet1" in US West Central mit "myVnet2" in Canada Central ge peered.</span><span class="sxs-lookup"><span data-stu-id="aace9-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="aace9-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aace9-112">PARAMETERS</span></span>

### <span data-ttu-id="aace9-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="aace9-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="aace9-114">Gibt an, dass dieses Cmdlet den weitergeleiteten Datenverkehr von den virtuellen Computern im virtuellen Remotenetzwerk zulässt.</span><span class="sxs-lookup"><span data-stu-id="aace9-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="aace9-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="aace9-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="aace9-116">Kennzeichnen, um die Verwendung von GatewayLinks in der Verknüpfung des virtuellen Remotenetzwerks zu diesem virtuellen Netzwerk zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="aace9-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="aace9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aace9-117">-AsJob</span></span>
<span data-ttu-id="aace9-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="aace9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aace9-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="aace9-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="aace9-120">Gibt an, dass dieses Cmdlet die virtuellen Computer im verknüpften virtuellen Netzwerkbereich blockiert, um auf alle virtuellen Computer im lokalen virtuellen Netzwerkbereich zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="aace9-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="aace9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aace9-121">-DefaultProfile</span></span>
<span data-ttu-id="aace9-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aace9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aace9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="aace9-123">-Name</span></span>
<span data-ttu-id="aace9-124">Gibt den Namen des Peerings für virtuelle Netzwerke an.</span><span class="sxs-lookup"><span data-stu-id="aace9-124">Specifies the name of the virtual network peering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aace9-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="aace9-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="aace9-126">Gibt die ID des virtuellen Remotenetzwerks an.</span><span class="sxs-lookup"><span data-stu-id="aace9-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aace9-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="aace9-127">-UseRemoteGateways</span></span>
<span data-ttu-id="aace9-128">Gibt an, dass dieses Cmdlet Remotegateways in diesem virtuellen Netzwerk zulässt.</span><span class="sxs-lookup"><span data-stu-id="aace9-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="aace9-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aace9-129">-VirtualNetwork</span></span>
<span data-ttu-id="aace9-130">Gibt das übergeordnete virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="aace9-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="aace9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aace9-131">CommonParameters</span></span>
<span data-ttu-id="aace9-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aace9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aace9-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aace9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aace9-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aace9-134">INPUTS</span></span>

### <span data-ttu-id="aace9-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aace9-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="aace9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="aace9-136">System.String</span></span>

## <span data-ttu-id="aace9-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aace9-137">OUTPUTS</span></span>

### <span data-ttu-id="aace9-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="aace9-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="aace9-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aace9-139">NOTES</span></span>

## <span data-ttu-id="aace9-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aace9-140">RELATED LINKS</span></span>

[<span data-ttu-id="aace9-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aace9-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="aace9-142">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="aace9-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="aace9-143">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="aace9-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="aace9-144">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="aace9-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
