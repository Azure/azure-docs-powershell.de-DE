---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 9d5f7960bb8f47a1f0d617cd4ba43db565ae2c79
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156849"
---
# <span data-ttu-id="dea14-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="dea14-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="dea14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dea14-102">SYNOPSIS</span></span>
<span data-ttu-id="dea14-103">Entfernt eine Dienstdelegierung aus dem bereitgestellten Subnetz.</span><span class="sxs-lookup"><span data-stu-id="dea14-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="dea14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dea14-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dea14-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dea14-105">DESCRIPTION</span></span>
<span data-ttu-id="dea14-106">Das **Cmdlet "Remove-AzDelegation"** nimmt ein Subnetz mit Subnetz an und entfernt die benannte Delegierung aus diesem Subnetz.</span><span class="sxs-lookup"><span data-stu-id="dea14-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="dea14-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dea14-107">EXAMPLES</span></span>

### <span data-ttu-id="dea14-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dea14-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="dea14-109">In diesem Beispiel ist die erste Hälfte (die unter _"Delegierung_ zu einem vorhandenen Subnetz hinzufügen" zu finden ist) identisch mit ["Add-AzDelegation".](./Add-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="dea14-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="dea14-110">In der zweiten Hälfte rufen die ersten beiden Cmdlets das subnetz des Interesses ab und aktualisieren die lokale Kopie mit dem, was sich auf dem Server befindet.</span><span class="sxs-lookup"><span data-stu-id="dea14-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="dea14-111">Das dritte Cmdlet entfernt die delegierung, die in der ersten Hälfte erstellt wurde, aus _mySubnet_ und speichert das aktualisierte Subnetz in _$subnet._</span><span class="sxs-lookup"><span data-stu-id="dea14-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="dea14-112">Das letzte Cmdlet aktualisiert den Server mit der entfernten Delegierung.</span><span class="sxs-lookup"><span data-stu-id="dea14-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="dea14-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dea14-113">PARAMETERS</span></span>

### <span data-ttu-id="dea14-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea14-114">-DefaultProfile</span></span>
<span data-ttu-id="dea14-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dea14-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dea14-116">-Name</span><span class="sxs-lookup"><span data-stu-id="dea14-116">-Name</span></span>
<span data-ttu-id="dea14-117">Der Name der Legierung</span><span class="sxs-lookup"><span data-stu-id="dea14-117">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea14-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="dea14-118">-Subnet</span></span>
<span data-ttu-id="dea14-119">Das Subnetz, aus dem die Delegierung entfernt werden soll</span><span class="sxs-lookup"><span data-stu-id="dea14-119">The subnet from which to remove the delegation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dea14-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea14-120">CommonParameters</span></span>
<span data-ttu-id="dea14-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dea14-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea14-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dea14-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea14-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dea14-123">INPUTS</span></span>

### <span data-ttu-id="dea14-124">System.String</span><span class="sxs-lookup"><span data-stu-id="dea14-124">System.String</span></span>

### <span data-ttu-id="dea14-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="dea14-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="dea14-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dea14-126">OUTPUTS</span></span>

### <span data-ttu-id="dea14-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="dea14-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="dea14-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dea14-128">NOTES</span></span>

## <span data-ttu-id="dea14-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dea14-129">RELATED LINKS</span></span>

<span data-ttu-id="dea14-130">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="dea14-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>