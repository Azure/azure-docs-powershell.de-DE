---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: bbe047def99ef2300c2002a2e8d5beedef26fd4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660159"
---
# <span data-ttu-id="69e41-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="69e41-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="69e41-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69e41-102">SYNOPSIS</span></span>
<span data-ttu-id="69e41-103">Konfiguriert einen virtuellen Netzwerk-Peering.</span><span class="sxs-lookup"><span data-stu-id="69e41-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="69e41-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69e41-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69e41-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69e41-105">DESCRIPTION</span></span>
<span data-ttu-id="69e41-106">Das Cmdlet " **Satz-AzVirtualNetworkPeering** " konfiguriert ein Peering für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="69e41-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="69e41-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69e41-107">EXAMPLES</span></span>

### <span data-ttu-id="69e41-108">Beispiel 1: Ändern der Konfiguration des weitergeleiteten Datenverkehrs eines virtuellen Netzwerk Peerings</span><span class="sxs-lookup"><span data-stu-id="69e41-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="69e41-109">Beispiel 2: Ändern des Zugriffs auf virtuelle Netzwerke eines virtuellen Netzwerk Peerings</span><span class="sxs-lookup"><span data-stu-id="69e41-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="69e41-110">Beispiel 3: Ändern der Eigenschaften Konfiguration des Gateway-Transits eines virtuellen Netzwerk Peerings</span><span class="sxs-lookup"><span data-stu-id="69e41-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="69e41-111">Beispiel 4: Verwenden von Remote Gateways im virtuellen Netzwerk-Peering</span><span class="sxs-lookup"><span data-stu-id="69e41-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

<span data-ttu-id="69e41-112">Wenn Sie diese Eigenschaft in $true ändern, kann das VNet-Gateway Ihres Peers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69e41-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="69e41-113">Der Peer-VNet muss jedoch über ein Gateway konfiguriert sein, und **AllowGatewayTransit** muss über einen Wert von $true verfügen.</span><span class="sxs-lookup"><span data-stu-id="69e41-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="69e41-114">Diese Eigenschaft kann nicht verwendet werden, wenn ein Gateway bereits konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="69e41-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="69e41-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="69e41-115">PARAMETERS</span></span>

### <span data-ttu-id="69e41-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69e41-116">-AsJob</span></span>
<span data-ttu-id="69e41-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="69e41-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69e41-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e41-118">-DefaultProfile</span></span>
<span data-ttu-id="69e41-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69e41-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69e41-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="69e41-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="69e41-121">Gibt den virtuellen Netzwerk-Peering an.</span><span class="sxs-lookup"><span data-stu-id="69e41-121">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="69e41-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e41-122">CommonParameters</span></span>
<span data-ttu-id="69e41-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69e41-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e41-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69e41-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e41-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69e41-125">INPUTS</span></span>

### <span data-ttu-id="69e41-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="69e41-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="69e41-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69e41-127">OUTPUTS</span></span>

### <span data-ttu-id="69e41-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="69e41-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="69e41-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="69e41-129">NOTES</span></span>

## <span data-ttu-id="69e41-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69e41-130">RELATED LINKS</span></span>

[<span data-ttu-id="69e41-131">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="69e41-131">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="69e41-132">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="69e41-132">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="69e41-133">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="69e41-133">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)
