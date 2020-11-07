---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: bcf26466c87a98d6a44486c5314c3541a7192a47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824048"
---
# <span data-ttu-id="20c3a-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="20c3a-101">Get-AzPeering</span></span>

## <span data-ttu-id="20c3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="20c3a-103">Ruft die Peering-Ressourcen für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="20c3a-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="20c3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20c3a-104">SYNTAX</span></span>

### <span data-ttu-id="20c3a-105">BySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="20c3a-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20c3a-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="20c3a-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20c3a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="20c3a-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20c3a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20c3a-108">DESCRIPTION</span></span>
<span data-ttu-id="20c3a-109">Ruft die Peerings aus einem Abonnement, einer Ressourcengruppe oder dem Namen ab.</span><span class="sxs-lookup"><span data-stu-id="20c3a-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="20c3a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20c3a-110">EXAMPLES</span></span>

### <span data-ttu-id="20c3a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20c3a-111">Example 1</span></span>
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

<span data-ttu-id="20c3a-112">Ruft alle Ressourcen für das Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="20c3a-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="20c3a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="20c3a-113">Example 2</span></span>
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

<span data-ttu-id="20c3a-114">Ruft das Exchange-Peering mit dem Namen `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="20c3a-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="20c3a-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="20c3a-115">Example 2</span></span>
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

<span data-ttu-id="20c3a-116">Ruft den Exchange-Peering `myExchangePeering1` -Namen ab, der auf der Ressourcen-ID basiert.</span><span class="sxs-lookup"><span data-stu-id="20c3a-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="20c3a-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="20c3a-117">PARAMETERS</span></span>

### <span data-ttu-id="20c3a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c3a-118">-DefaultProfile</span></span>
<span data-ttu-id="20c3a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20c3a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20c3a-120">-Art</span><span class="sxs-lookup"><span data-stu-id="20c3a-120">-Kind</span></span>
<span data-ttu-id="20c3a-121">Zeigt alle Peering-Ressourcen nach Art.</span><span class="sxs-lookup"><span data-stu-id="20c3a-121">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="20c3a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="20c3a-122">-Name</span></span>
<span data-ttu-id="20c3a-123">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="20c3a-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="20c3a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c3a-124">-ResourceGroupName</span></span>
<span data-ttu-id="20c3a-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="20c3a-125">The resource group name.</span></span>

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

### <span data-ttu-id="20c3a-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="20c3a-126">-ResourceId</span></span>
<span data-ttu-id="20c3a-127">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="20c3a-127">The resource id string name.</span></span>

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

### <span data-ttu-id="20c3a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c3a-128">CommonParameters</span></span>
<span data-ttu-id="20c3a-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c3a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c3a-130">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20c3a-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c3a-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20c3a-131">INPUTS</span></span>

### <span data-ttu-id="20c3a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="20c3a-132">System.String</span></span>

## <span data-ttu-id="20c3a-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20c3a-133">OUTPUTS</span></span>

### <span data-ttu-id="20c3a-134">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="20c3a-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="20c3a-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="20c3a-135">NOTES</span></span>

## <span data-ttu-id="20c3a-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20c3a-136">RELATED LINKS</span></span>
