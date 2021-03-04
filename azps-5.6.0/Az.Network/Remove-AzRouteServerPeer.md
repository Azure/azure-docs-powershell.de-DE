---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
ms.openlocfilehash: 52733af41b5f8d84811f1c1f184181a2d45053e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933771"
---
# <span data-ttu-id="8c664-101">Remove-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="8c664-101">Remove-AzRouteServerPeer</span></span>

## <span data-ttu-id="8c664-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c664-102">SYNOPSIS</span></span>
<span data-ttu-id="8c664-103">Entfernt einen Peer von einem Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="8c664-103">Removes a Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="8c664-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c664-104">SYNTAX</span></span>

### <span data-ttu-id="8c664-105">RouteServerNPeerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8c664-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c664-106">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c664-106">RouteServerNPeerInputObjectParameterSet</span></span>
```
Remove-AzRouteServerPeer -InputObject <PSRouteServerPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c664-107">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c664-107">RouteServerNPeerResourceIdParameterSet</span></span>
```
Remove-AzRouteServerPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c664-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c664-108">DESCRIPTION</span></span>
<span data-ttu-id="8c664-109">Das **Cmdlet Remove-AzRouteServerPeer** entfernt einen RouteServer-Peer von einem Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="8c664-109">The **Remove-AzRouteServerPeer** cmdlet removes a RouteServer Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="8c664-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8c664-110">EXAMPLES</span></span>

### <span data-ttu-id="8c664-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8c664-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServerPeer -PeerName peer -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="8c664-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8c664-112">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Remove-AzRouteServerPeer -ResourceId $RouteServerPeerId
```

### <span data-ttu-id="8c664-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8c664-113">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
Remove-AzRouteServerPeer -InputObject $RouteServerPeer
```
## <span data-ttu-id="8c664-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8c664-114">PARAMETERS</span></span>

### <span data-ttu-id="8c664-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c664-115">-AsJob</span></span>
<span data-ttu-id="8c664-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8c664-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c664-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c664-117">-DefaultProfile</span></span>
<span data-ttu-id="8c664-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c664-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c664-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="8c664-119">-Force</span></span>
<span data-ttu-id="8c664-120">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="8c664-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8c664-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c664-121">-InputObject</span></span>
<span data-ttu-id="8c664-122">Das Peereingabeobjekt des Routenservers.</span><span class="sxs-lookup"><span data-stu-id="8c664-122">The route server peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer
Parameter Sets: RouteServerNPeerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c664-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="8c664-123">-PeerName</span></span>
<span data-ttu-id="8c664-124">Der Name des Routenserver-Peers.</span><span class="sxs-lookup"><span data-stu-id="8c664-124">The name of the route server Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c664-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c664-125">-ResourceGroupName</span></span>
<span data-ttu-id="8c664-126">Der Ressourcengruppenname des Routenservers/Peers.</span><span class="sxs-lookup"><span data-stu-id="8c664-126">The resource group name of the route server/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c664-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c664-127">-ResourceId</span></span>
<span data-ttu-id="8c664-128">Die Peerressourcen-ID des Routenservers.</span><span class="sxs-lookup"><span data-stu-id="8c664-128">The route server peer resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c664-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="8c664-129">-RouteServerName</span></span>
<span data-ttu-id="8c664-130">Der Routenserver, auf dem peer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8c664-130">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c664-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8c664-131">-Confirm</span></span>
<span data-ttu-id="8c664-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c664-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c664-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c664-133">-WhatIf</span></span>
<span data-ttu-id="8c664-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c664-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c664-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c664-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c664-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c664-136">CommonParameters</span></span>
<span data-ttu-id="8c664-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c664-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c664-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c664-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c664-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8c664-139">INPUTS</span></span>

### <span data-ttu-id="8c664-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8c664-140">System.String</span></span>

### <span data-ttu-id="8c664-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="8c664-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="8c664-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8c664-142">OUTPUTS</span></span>

### <span data-ttu-id="8c664-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="8c664-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="8c664-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8c664-144">NOTES</span></span>

## <span data-ttu-id="8c664-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8c664-145">RELATED LINKS</span></span>
