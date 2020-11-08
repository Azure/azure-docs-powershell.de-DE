---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: a63f6c2bc57bfc4d1a82861c6b25bd5c8a6e1383
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179057"
---
# <span data-ttu-id="cb8aa-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="cb8aa-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="cb8aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="cb8aa-103">Erstellt ein Peering zwischen zwei virtuellen Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="cb8aa-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="cb8aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb8aa-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb8aa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb8aa-105">DESCRIPTION</span></span>
<span data-ttu-id="cb8aa-106">Das Cmdlet **Add-AzVirtualNetworkPeering** erstellt einen Peering zwischen zwei virtuellen Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="cb8aa-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="cb8aa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb8aa-107">EXAMPLES</span></span>

### <span data-ttu-id="cb8aa-108">Beispiel 1: Erstellen eines Peers zwischen zwei virtuellen Netzwerken in der gleichen Region</span><span class="sxs-lookup"><span data-stu-id="cb8aa-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
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

<span data-ttu-id="cb8aa-109">Beachten Sie, dass ein Peering-Link von vnet1 zu vnet2 und umgekehrt erstellt werden muss, damit Peering funktionieren kann.</span><span class="sxs-lookup"><span data-stu-id="cb8aa-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="cb8aa-110">Beispiel 2: Erstellen eines Peers zwischen zwei virtuellen Netzwerken in verschiedenen Regionen</span><span class="sxs-lookup"><span data-stu-id="cb8aa-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
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

<span data-ttu-id="cb8aa-111">Hier ist "myVnet1" in US West Central mit "myVnet2" in Kanada Central vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="cb8aa-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="cb8aa-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb8aa-112">PARAMETERS</span></span>

### <span data-ttu-id="cb8aa-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="cb8aa-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="cb8aa-114">Gibt an, dass dieses Cmdlet den weitergeleiteten Datenverkehr von den virtuellen Computern im virtuellen Remotenetzwerk zulässt.</span><span class="sxs-lookup"><span data-stu-id="cb8aa-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="cb8aa-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="cb8aa-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="cb8aa-116">Kennzeichnen, damit gatewayLinks im virtuellen Remotenetzwerk-Link zu diesem virtuellen Netzwerk verwendet werden kann</span><span class="sxs-lookup"><span data-stu-id="cb8aa-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="cb8aa-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb8aa-117">-AsJob</span></span>
<span data-ttu-id="cb8aa-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cb8aa-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb8aa-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="cb8aa-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="cb8aa-120">Gibt an, dass dieses Cmdlet die virtuellen Computer im verknüpften virtuellen Netzwerkspeicher blockiert, um auf alle virtuellen Computer im lokalen virtuellen Netzwerkspeicher zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="cb8aa-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="cb8aa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb8aa-121">-DefaultProfile</span></span>
<span data-ttu-id="cb8aa-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb8aa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb8aa-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cb8aa-123">-Name</span></span>
<span data-ttu-id="cb8aa-124">Gibt den Namen des virtuellen Netzwerk-Peering an.</span><span class="sxs-lookup"><span data-stu-id="cb8aa-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="cb8aa-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="cb8aa-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="cb8aa-126">Gibt die ID des virtuellen Remotenetzwerks an.</span><span class="sxs-lookup"><span data-stu-id="cb8aa-126">Specifies the ID of the remote virtual network.</span></span>

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

### <span data-ttu-id="cb8aa-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="cb8aa-127">-UseRemoteGateways</span></span>
<span data-ttu-id="cb8aa-128">Gibt an, dass dieses Cmdlet Remote Gateways in diesem virtuellen Netzwerk zulässt.</span><span class="sxs-lookup"><span data-stu-id="cb8aa-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="cb8aa-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cb8aa-129">-VirtualNetwork</span></span>
<span data-ttu-id="cb8aa-130">Gibt das übergeordnete virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="cb8aa-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="cb8aa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb8aa-131">CommonParameters</span></span>
<span data-ttu-id="cb8aa-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb8aa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb8aa-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb8aa-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb8aa-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb8aa-134">INPUTS</span></span>

### <span data-ttu-id="cb8aa-135">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cb8aa-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="cb8aa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cb8aa-136">System.String</span></span>

## <span data-ttu-id="cb8aa-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb8aa-137">OUTPUTS</span></span>

### <span data-ttu-id="cb8aa-138">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="cb8aa-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="cb8aa-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb8aa-139">NOTES</span></span>

## <span data-ttu-id="cb8aa-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb8aa-140">RELATED LINKS</span></span>

[<span data-ttu-id="cb8aa-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cb8aa-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="cb8aa-142">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="cb8aa-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="cb8aa-143">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="cb8aa-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="cb8aa-144">Satz-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="cb8aa-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
