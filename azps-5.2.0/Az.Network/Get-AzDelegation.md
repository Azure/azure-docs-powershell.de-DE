---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: f32b06e9b162a4d142d6d6fff9b7cdca34e0b30b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289348"
---
# <span data-ttu-id="3a590-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="3a590-101">Get-AzDelegation</span></span>

## <span data-ttu-id="3a590-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a590-102">SYNOPSIS</span></span>
<span data-ttu-id="3a590-103">Erhalten Sie eine Delegierung (oder alle Deren) in einem bestimmten Subnetz.</span><span class="sxs-lookup"><span data-stu-id="3a590-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="3a590-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a590-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a590-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a590-105">DESCRIPTION</span></span>
<span data-ttu-id="3a590-106">Das **Cmdlet "Get-AzDelegation"** ruft die benannte Delegierung aus einem Subnetz ab.</span><span class="sxs-lookup"><span data-stu-id="3a590-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="3a590-107">Wenn keine Delegierung benannt ist, gibt sie alle Daten im bereitgestellten Subnetz zurück.</span><span class="sxs-lookup"><span data-stu-id="3a590-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="3a590-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a590-108">EXAMPLES</span></span>

### <span data-ttu-id="3a590-109">1: Abrufen einer bestimmten Delegierung</span><span class="sxs-lookup"><span data-stu-id="3a590-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="3a590-110">Die erste Zeile ruft das Interessennetz ab.</span><span class="sxs-lookup"><span data-stu-id="3a590-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="3a590-111">Die zweite Zeile enthält die Delegierungsinformationen für die Delegierung namens "myDelegation".</span><span class="sxs-lookup"><span data-stu-id="3a590-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="3a590-112">2: Abrufen aller Subnetze</span><span class="sxs-lookup"><span data-stu-id="3a590-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="3a590-113">Die erste Zeile ruft das Interessennetz ab.</span><span class="sxs-lookup"><span data-stu-id="3a590-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="3a590-114">In der zweiten Zeile wird eine Liste aller auf _mySubnet_ vorhandenen Daten in der $delegations gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3a590-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="3a590-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a590-115">PARAMETERS</span></span>

### <span data-ttu-id="3a590-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a590-116">-DefaultProfile</span></span>
<span data-ttu-id="3a590-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a590-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a590-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3a590-118">-Name</span></span>
<span data-ttu-id="3a590-119">Der Name der Legierung</span><span class="sxs-lookup"><span data-stu-id="3a590-119">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a590-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="3a590-120">-Subnet</span></span>
<span data-ttu-id="3a590-121">Das Subnetz</span><span class="sxs-lookup"><span data-stu-id="3a590-121">The subnet</span></span>

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

### <span data-ttu-id="3a590-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a590-122">CommonParameters</span></span>
<span data-ttu-id="3a590-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a590-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a590-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a590-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a590-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a590-125">INPUTS</span></span>

### <span data-ttu-id="3a590-126">System.String</span><span class="sxs-lookup"><span data-stu-id="3a590-126">System.String</span></span>

### <span data-ttu-id="3a590-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="3a590-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="3a590-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a590-128">OUTPUTS</span></span>

### <span data-ttu-id="3a590-129">Microsoft.Azure.Commands.Network.Models.PSDElegation</span><span class="sxs-lookup"><span data-stu-id="3a590-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="3a590-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3a590-130">NOTES</span></span>

## <span data-ttu-id="3a590-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3a590-131">RELATED LINKS</span></span>

<span data-ttu-id="3a590-132">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="3a590-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>
