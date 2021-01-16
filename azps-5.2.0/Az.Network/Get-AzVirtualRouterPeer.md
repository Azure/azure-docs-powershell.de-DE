---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 363e9518234551f55bf75fb6c93f8b0b70b495ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306256"
---
# <span data-ttu-id="639e4-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="639e4-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="639e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="639e4-102">SYNOPSIS</span></span>
<span data-ttu-id="639e4-103">Ruft einen VirtualRouter-Peer in einem Azure VirtualRouter ab.</span><span class="sxs-lookup"><span data-stu-id="639e4-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="639e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="639e4-104">SYNTAX</span></span>

### <span data-ttu-id="639e4-105">VirtualRouterPeerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="639e4-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="639e4-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="639e4-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="639e4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="639e4-107">DESCRIPTION</span></span>
<span data-ttu-id="639e4-108">Das **Cmdlet "Get-AzVirtualRouterPeer"** ruft einen Peer in einem Azure VirtualRouter ab.</span><span class="sxs-lookup"><span data-stu-id="639e4-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="639e4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="639e4-109">EXAMPLES</span></span>

### <span data-ttu-id="639e4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="639e4-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="639e4-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="639e4-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="639e4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="639e4-112">PARAMETERS</span></span>

### <span data-ttu-id="639e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="639e4-113">-DefaultProfile</span></span>
<span data-ttu-id="639e4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="639e4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="639e4-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="639e4-115">-PeerName</span></span>
<span data-ttu-id="639e4-116">Der Name des virtuellen Router-Peers.</span><span class="sxs-lookup"><span data-stu-id="639e4-116">The name of the virtual router peer.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="639e4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="639e4-117">-ResourceGroupName</span></span>
<span data-ttu-id="639e4-118">Der Ressourcengruppenname des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="639e4-118">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="639e4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="639e4-119">-ResourceId</span></span>
<span data-ttu-id="639e4-120">ResourceId des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="639e4-120">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="639e4-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="639e4-121">-VirtualRouterName</span></span>
<span data-ttu-id="639e4-122">Der Name des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="639e4-122">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="639e4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="639e4-123">CommonParameters</span></span>
<span data-ttu-id="639e4-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="639e4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="639e4-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="639e4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="639e4-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="639e4-126">INPUTS</span></span>

### <span data-ttu-id="639e4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="639e4-127">System.String</span></span>

## <span data-ttu-id="639e4-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="639e4-128">OUTPUTS</span></span>

### <span data-ttu-id="639e4-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="639e4-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="639e4-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="639e4-130">NOTES</span></span>

## <span data-ttu-id="639e4-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="639e4-131">RELATED LINKS</span></span>
