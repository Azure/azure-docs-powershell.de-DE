---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: cbb560b04219b0a77c9158afe3b76b1b9461cdb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926587"
---
# <span data-ttu-id="e40c1-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="e40c1-101">Get-AzDelegation</span></span>

## <span data-ttu-id="e40c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e40c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e40c1-103">Holen Sie sich eine Delegation (oder alle Delegation) in einem bestimmten Subnetz.</span><span class="sxs-lookup"><span data-stu-id="e40c1-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="e40c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e40c1-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e40c1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e40c1-105">DESCRIPTION</span></span>
<span data-ttu-id="e40c1-106">Das **Get-AzDelegation-Cmdlet** ruft die benannte Delegierung aus einem Subnetz ab.</span><span class="sxs-lookup"><span data-stu-id="e40c1-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="e40c1-107">Wenn keine Delegierung benannt ist, gibt sie alle Delegationen im bereitgestellten Subnetz zurück.</span><span class="sxs-lookup"><span data-stu-id="e40c1-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="e40c1-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e40c1-108">EXAMPLES</span></span>

### <span data-ttu-id="e40c1-109">1: Abrufen einer bestimmten Delegierung</span><span class="sxs-lookup"><span data-stu-id="e40c1-109">1: Retrieving a specific delegation</span></span>
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

<span data-ttu-id="e40c1-110">In der ersten Zeile wird das von Interesse seinde Subnetz abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e40c1-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="e40c1-111">In der zweiten Zeile werden die Delegierungsinformationen für die Delegation mit dem Namen "myDelegation" gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e40c1-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="e40c1-112">2: Abrufen aller Subnetzdelegationen</span><span class="sxs-lookup"><span data-stu-id="e40c1-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="e40c1-113">In der ersten Zeile wird das von Interesse seinde Subnetz abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e40c1-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="e40c1-114">In der zweiten Zeile wird eine Liste aller Delegationen auf _mySubnet_ in der $delegations gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e40c1-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="e40c1-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e40c1-115">PARAMETERS</span></span>

### <span data-ttu-id="e40c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e40c1-116">-DefaultProfile</span></span>
<span data-ttu-id="e40c1-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e40c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e40c1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e40c1-118">-Name</span></span>
<span data-ttu-id="e40c1-119">Der Name der Delegierung</span><span class="sxs-lookup"><span data-stu-id="e40c1-119">The name of the delegation</span></span>

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

### <span data-ttu-id="e40c1-120">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="e40c1-120">-Subnet</span></span>
<span data-ttu-id="e40c1-121">Das Subnetz</span><span class="sxs-lookup"><span data-stu-id="e40c1-121">The subnet</span></span>

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

### <span data-ttu-id="e40c1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e40c1-122">CommonParameters</span></span>
<span data-ttu-id="e40c1-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e40c1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e40c1-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e40c1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e40c1-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e40c1-125">INPUTS</span></span>

### <span data-ttu-id="e40c1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e40c1-126">System.String</span></span>

### <span data-ttu-id="e40c1-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="e40c1-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="e40c1-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e40c1-128">OUTPUTS</span></span>

### <span data-ttu-id="e40c1-129">Microsoft.Azure.Commands.Network.Models.PSDElegation</span><span class="sxs-lookup"><span data-stu-id="e40c1-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="e40c1-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e40c1-130">NOTES</span></span>

## <span data-ttu-id="e40c1-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e40c1-131">RELATED LINKS</span></span>

<span data-ttu-id="e40c1-132">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="e40c1-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>
