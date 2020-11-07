---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: 1bf784a94d3f4a03c380f114064fa3f1e399e379
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850780"
---
# <span data-ttu-id="8d906-101">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8d906-101">Add-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="8d906-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d906-102">SYNOPSIS</span></span>
<span data-ttu-id="8d906-103">Erstellt ein Peering zwischen zwei virtuellen Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="8d906-103">Creates a peering between two virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d906-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d906-104">SYNTAX</span></span>

```
Add-AzureRmVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d906-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d906-105">DESCRIPTION</span></span>
<span data-ttu-id="8d906-106">Das Cmdlet **Add-AzureRmVirtualNetworkPeering** erstellt einen Peering zwischen zwei virtuellen Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="8d906-106">The **Add-AzureRmVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="8d906-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d906-107">EXAMPLES</span></span>

### <span data-ttu-id="8d906-108">Beispiel 1: Erstellen eines Peers zwischen zwei virtuellen Netzwerken in der gleichen Region</span><span class="sxs-lookup"><span data-stu-id="8d906-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="8d906-109">Beachten Sie, dass ein Peering-Link von vnet1 zu vnet2 und umgekehrt erstellt werden muss, damit Peering funktionieren kann.</span><span class="sxs-lookup"><span data-stu-id="8d906-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="8d906-110">Beispiel 2: Erstellen eines Peers zwischen zwei virtuellen Netzwerken in verschiedenen Regionen</span><span class="sxs-lookup"><span data-stu-id="8d906-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="8d906-111">Hier ist "myVnet1" in US West Central mit "myVnet2" in Kanada Central vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="8d906-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="8d906-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d906-112">PARAMETERS</span></span>

### <span data-ttu-id="8d906-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="8d906-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="8d906-114">Gibt an, dass dieses Cmdlet den weitergeleiteten Datenverkehr von den virtuellen Computern im virtuellen Remotenetzwerk zulässt.</span><span class="sxs-lookup"><span data-stu-id="8d906-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="8d906-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="8d906-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="8d906-116">Kennzeichnen, damit gatewayLinks im virtuellen Remotenetzwerk-Link zu diesem virtuellen Netzwerk verwendet werden kann</span><span class="sxs-lookup"><span data-stu-id="8d906-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d906-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d906-117">-AsJob</span></span>
<span data-ttu-id="8d906-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8d906-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d906-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="8d906-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="8d906-120">Gibt an, dass dieses Cmdlet die virtuellen Computer im verknüpften virtuellen Netzwerkspeicher blockiert, um auf alle virtuellen Computer im lokalen virtuellen Netzwerkspeicher zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="8d906-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="8d906-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d906-121">-DefaultProfile</span></span>
<span data-ttu-id="8d906-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d906-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d906-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8d906-123">-Name</span></span>
<span data-ttu-id="8d906-124">Gibt den Namen des virtuellen Netzwerk-Peering an.</span><span class="sxs-lookup"><span data-stu-id="8d906-124">Specifies the name of the virtual network peering.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d906-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8d906-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="8d906-126">Gibt die ID des virtuellen Remotenetzwerks an.</span><span class="sxs-lookup"><span data-stu-id="8d906-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d906-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="8d906-127">-UseRemoteGateways</span></span>
<span data-ttu-id="8d906-128">Gibt an, dass dieses Cmdlet Remote Gateways in diesem virtuellen Netzwerk zulässt.</span><span class="sxs-lookup"><span data-stu-id="8d906-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="8d906-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8d906-129">-VirtualNetwork</span></span>
<span data-ttu-id="8d906-130">Gibt das übergeordnete virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="8d906-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="8d906-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d906-131">CommonParameters</span></span>
<span data-ttu-id="8d906-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d906-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d906-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d906-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d906-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d906-134">INPUTS</span></span>

### <span data-ttu-id="8d906-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8d906-135">String</span></span>
<span data-ttu-id="8d906-136">Der Parameter "RemoteVirtualNetworkId" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8d906-136">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="8d906-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8d906-137">PSVirtualNetwork</span></span>
<span data-ttu-id="8d906-138">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8d906-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="8d906-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d906-139">OUTPUTS</span></span>

### <span data-ttu-id="8d906-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8d906-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="8d906-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d906-141">NOTES</span></span>

## <span data-ttu-id="8d906-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d906-142">RELATED LINKS</span></span>

[<span data-ttu-id="8d906-143">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8d906-143">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="8d906-144">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8d906-144">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="8d906-145">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8d906-145">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="8d906-146">Satz-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8d906-146">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


