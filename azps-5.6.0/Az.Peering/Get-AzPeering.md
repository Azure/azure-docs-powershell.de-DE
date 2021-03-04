---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: e2827d08d813608dbf3f6f40bc15603d5a5a0d99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937787"
---
# <span data-ttu-id="a04dc-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a04dc-101">Get-AzPeering</span></span>

## <span data-ttu-id="a04dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a04dc-102">SYNOPSIS</span></span>
<span data-ttu-id="a04dc-103">Ruft die Peeringressourcen für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a04dc-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="a04dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a04dc-104">SYNTAX</span></span>

### <span data-ttu-id="a04dc-105">BySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="a04dc-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a04dc-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="a04dc-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a04dc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a04dc-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a04dc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a04dc-108">DESCRIPTION</span></span>
<span data-ttu-id="a04dc-109">Ruft die Peerings aus einem Abonnement, einer Ressourcengruppe oder nach Namen ab.</span><span class="sxs-lookup"><span data-stu-id="a04dc-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="a04dc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a04dc-110">EXAMPLES</span></span>

### <span data-ttu-id="a04dc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a04dc-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeering

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}

Name                 : ContosoSeattlePeering
Sku                  : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringSku
Kind                 : Direct
Connections          : {99999}
UseForPeeringService : False
PeerAsn              : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSSubResource
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions/resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="a04dc-112">Ruft alle Ressourcen für das Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a04dc-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="a04dc-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a04dc-113">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceGroupName test -Name myExchangePeering1

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="a04dc-114">Ruft das Exchange-Peering mit dem Namen ab. `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="a04dc-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="a04dc-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a04dc-115">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceId $resourceId

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="a04dc-116">Ruft das Exchange-Peering basierend `myExchangePeering1` auf der Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="a04dc-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="a04dc-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a04dc-117">PARAMETERS</span></span>

### <span data-ttu-id="a04dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a04dc-118">-DefaultProfile</span></span>
<span data-ttu-id="a04dc-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a04dc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a04dc-120">-Kind</span><span class="sxs-lookup"><span data-stu-id="a04dc-120">-Kind</span></span>
<span data-ttu-id="a04dc-121">Zeigt alle Peeringressourcen nach Art an.</span><span class="sxs-lookup"><span data-stu-id="a04dc-121">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a04dc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a04dc-122">-Name</span></span>
<span data-ttu-id="a04dc-123">Der eindeutige Name des PSPeerings.</span><span class="sxs-lookup"><span data-stu-id="a04dc-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a04dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a04dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="a04dc-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a04dc-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a04dc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a04dc-126">-ResourceId</span></span>
<span data-ttu-id="a04dc-127">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a04dc-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a04dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a04dc-128">CommonParameters</span></span>
<span data-ttu-id="a04dc-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a04dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a04dc-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a04dc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a04dc-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a04dc-131">INPUTS</span></span>

### <span data-ttu-id="a04dc-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a04dc-132">System.String</span></span>

## <span data-ttu-id="a04dc-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a04dc-133">OUTPUTS</span></span>

### <span data-ttu-id="a04dc-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="a04dc-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a04dc-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a04dc-135">NOTES</span></span>

## <span data-ttu-id="a04dc-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a04dc-136">RELATED LINKS</span></span>
