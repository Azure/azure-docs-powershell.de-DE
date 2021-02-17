---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: 421358a9241fe41549898547c62404f6ba1162e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158825"
---
# <span data-ttu-id="eed6a-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="eed6a-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="eed6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eed6a-102">SYNOPSIS</span></span>
<span data-ttu-id="eed6a-103">Konfiguriert ein virtuelles Netzwerk-Peering.</span><span class="sxs-lookup"><span data-stu-id="eed6a-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="eed6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eed6a-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eed6a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eed6a-105">DESCRIPTION</span></span>
<span data-ttu-id="eed6a-106">Das **Cmdlet "Set-AzVirtualNetworkPeering"** konfiguriert ein virtuelles Netzwerkpeering.</span><span class="sxs-lookup"><span data-stu-id="eed6a-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="eed6a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eed6a-107">EXAMPLES</span></span>

### <span data-ttu-id="eed6a-108">Beispiel 1: Ändern der Konfiguration eines weitergeleiteten Datenverkehrs eines virtuellen Netzwerk-Peerings</span><span class="sxs-lookup"><span data-stu-id="eed6a-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="eed6a-109">Beispiel 2: Ändern des virtuellen Netzwerkzugriffs eines virtuellen Netzwerk peerings</span><span class="sxs-lookup"><span data-stu-id="eed6a-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="eed6a-110">Beispiel 3: Ändern der Konfiguration einer Gatewaydurchfahrtseigenschaft für ein virtuelles Netzwerk-Peering</span><span class="sxs-lookup"><span data-stu-id="eed6a-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="eed6a-111">Beispiel 4: Verwenden von Remotegateways in Peering für virtuelle Netzwerke</span><span class="sxs-lookup"><span data-stu-id="eed6a-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

<span data-ttu-id="eed6a-112">Wenn Sie diese Eigenschaft in $True ändern, kann das VNetgateway Ihres Peers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eed6a-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="eed6a-113">Für das Peer-VNet muss jedoch ein Gateway konfiguriert sein, und **AllowGatewayTransit** muss einen Wert von $True.</span><span class="sxs-lookup"><span data-stu-id="eed6a-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="eed6a-114">Diese Eigenschaft kann nicht verwendet werden, wenn ein Gateway bereits konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="eed6a-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="eed6a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eed6a-115">PARAMETERS</span></span>

### <span data-ttu-id="eed6a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eed6a-116">-AsJob</span></span>
<span data-ttu-id="eed6a-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="eed6a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eed6a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed6a-118">-DefaultProfile</span></span>
<span data-ttu-id="eed6a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eed6a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eed6a-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="eed6a-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="eed6a-121">Gibt das virtuelle Netzwerk peering an.</span><span class="sxs-lookup"><span data-stu-id="eed6a-121">Specifies the virtual network peering.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eed6a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed6a-122">CommonParameters</span></span>
<span data-ttu-id="eed6a-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eed6a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed6a-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eed6a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed6a-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eed6a-125">INPUTS</span></span>

### <span data-ttu-id="eed6a-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="eed6a-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="eed6a-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eed6a-127">OUTPUTS</span></span>

### <span data-ttu-id="eed6a-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="eed6a-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="eed6a-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eed6a-129">NOTES</span></span>

## <span data-ttu-id="eed6a-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eed6a-130">RELATED LINKS</span></span>

[<span data-ttu-id="eed6a-131">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="eed6a-131">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="eed6a-132">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="eed6a-132">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="eed6a-133">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="eed6a-133">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)
