---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeeradvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
ms.openlocfilehash: 259fb6948abee3a00788e68c8d362196e5c12d51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379783"
---
# <span data-ttu-id="ff71f-101">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="ff71f-101">Get-AzVirtualRouterPeerAdvertisedRoute</span></span>

## <span data-ttu-id="ff71f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff71f-102">SYNOPSIS</span></span>
<span data-ttu-id="ff71f-103">Liste der Routen, die von einem bestimmten virtuellen Router peer angekündigt werden</span><span class="sxs-lookup"><span data-stu-id="ff71f-103">List routes being advertised by specific virtual router peer</span></span>

## <span data-ttu-id="ff71f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff71f-104">SYNTAX</span></span>

### <span data-ttu-id="ff71f-105">VirtualRouterPeerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff71f-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -ResourceGroupName <String> -VirtualRouterName <String>
 -PeerName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff71f-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff71f-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff71f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff71f-107">DESCRIPTION</span></span>
<span data-ttu-id="ff71f-108">Geben Sie einem virtuellen Router-Peer entweder nach Name oder Objekt eine Aufzählung der Routen an, die von einem bestimmten virtuellen Router an den Peer angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="ff71f-108">Given A virtual router peer either by name or by object, enumerate routes being advertised to that peer by a specific virtual router.</span></span>

## <span data-ttu-id="ff71f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ff71f-109">EXAMPLES</span></span>

### <span data-ttu-id="ff71f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ff71f-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerAdvertisedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="ff71f-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ff71f-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerAdvertisedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="ff71f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff71f-112">PARAMETERS</span></span>

### <span data-ttu-id="ff71f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff71f-113">-AsJob</span></span>
<span data-ttu-id="ff71f-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ff71f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff71f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff71f-115">-DefaultProfile</span></span>
<span data-ttu-id="ff71f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff71f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff71f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff71f-117">-InputObject</span></span>
<span data-ttu-id="ff71f-118">Das Eingabeobjekt des virtuellen Router-Peers.</span><span class="sxs-lookup"><span data-stu-id="ff71f-118">The virtual router peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff71f-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="ff71f-119">-PeerName</span></span>
<span data-ttu-id="ff71f-120">Name des Peers des virtuellen Routers</span><span class="sxs-lookup"><span data-stu-id="ff71f-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="ff71f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff71f-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff71f-122">Name der Virtuellen Router-Peer-Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ff71f-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="ff71f-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="ff71f-123">-VirtualRouterName</span></span>
<span data-ttu-id="ff71f-124">Name des virtuellen Routers</span><span class="sxs-lookup"><span data-stu-id="ff71f-124">Virtual router name</span></span>

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

### <span data-ttu-id="ff71f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff71f-125">CommonParameters</span></span>
<span data-ttu-id="ff71f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff71f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff71f-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff71f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff71f-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ff71f-128">INPUTS</span></span>

### <span data-ttu-id="ff71f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ff71f-129">System.String</span></span>

### <span data-ttu-id="ff71f-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="ff71f-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="ff71f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ff71f-131">OUTPUTS</span></span>

### <span data-ttu-id="ff71f-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="ff71f-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="ff71f-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ff71f-133">NOTES</span></span>

## <span data-ttu-id="ff71f-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ff71f-134">RELATED LINKS</span></span>
