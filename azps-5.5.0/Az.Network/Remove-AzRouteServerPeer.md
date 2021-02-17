---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
ms.openlocfilehash: d177c0dfa5ff59fde0adfe8ac4e3598ae70127f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169680"
---
# <span data-ttu-id="085d3-101">Remove-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="085d3-101">Remove-AzRouteServerPeer</span></span>

## <span data-ttu-id="085d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="085d3-102">SYNOPSIS</span></span>
<span data-ttu-id="085d3-103">Entfernt einen Peer aus einem Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="085d3-103">Removes a Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="085d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="085d3-104">SYNTAX</span></span>

### <span data-ttu-id="085d3-105">RouteServerNPeerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="085d3-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="085d3-106">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="085d3-106">RouteServerNPeerInputObjectParameterSet</span></span>
```
Remove-AzRouteServerPeer -InputObject <PSRouteServerPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="085d3-107">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="085d3-107">RouteServerNPeerResourceIdParameterSet</span></span>
```
Remove-AzRouteServerPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="085d3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="085d3-108">DESCRIPTION</span></span>
<span data-ttu-id="085d3-109">Das **Cmdlet "Remove-AzRouteServerPeer"** entfernt einen RouteServer Peer aus einem Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="085d3-109">The **Remove-AzRouteServerPeer** cmdlet removes a RouteServer Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="085d3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="085d3-110">EXAMPLES</span></span>

### <span data-ttu-id="085d3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="085d3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServerPeer -PeerName peer -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="085d3-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="085d3-112">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Remove-AzRouteServerPeer -ResourceId $RouteServerPeerId
```

### <span data-ttu-id="085d3-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="085d3-113">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
Remove-AzRouteServerPeer -InputObject $RouteServerPeer
```
## <span data-ttu-id="085d3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="085d3-114">PARAMETERS</span></span>

### <span data-ttu-id="085d3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="085d3-115">-AsJob</span></span>
<span data-ttu-id="085d3-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="085d3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="085d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="085d3-117">-DefaultProfile</span></span>
<span data-ttu-id="085d3-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="085d3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="085d3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="085d3-119">-Force</span></span>
<span data-ttu-id="085d3-120">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="085d3-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="085d3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="085d3-121">-InputObject</span></span>
<span data-ttu-id="085d3-122">Das Eingabeobjekt für den Routenserver-Peer.</span><span class="sxs-lookup"><span data-stu-id="085d3-122">The route server peer input object.</span></span>

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

### <span data-ttu-id="085d3-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="085d3-123">-PeerName</span></span>
<span data-ttu-id="085d3-124">Der Name des Routenserver-Peers.</span><span class="sxs-lookup"><span data-stu-id="085d3-124">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="085d3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="085d3-125">-ResourceGroupName</span></span>
<span data-ttu-id="085d3-126">Der Ressourcengruppenname des Routeservers/Peers.</span><span class="sxs-lookup"><span data-stu-id="085d3-126">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="085d3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="085d3-127">-ResourceId</span></span>
<span data-ttu-id="085d3-128">Die Peerressourcen-ID des Routeservers.</span><span class="sxs-lookup"><span data-stu-id="085d3-128">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="085d3-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="085d3-129">-RouteServerName</span></span>
<span data-ttu-id="085d3-130">Der Routeserver, auf dem Peer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="085d3-130">The route server where peer exists.</span></span>

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

### <span data-ttu-id="085d3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="085d3-131">-Confirm</span></span>
<span data-ttu-id="085d3-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="085d3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="085d3-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="085d3-133">-WhatIf</span></span>
<span data-ttu-id="085d3-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="085d3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="085d3-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="085d3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="085d3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="085d3-136">CommonParameters</span></span>
<span data-ttu-id="085d3-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="085d3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="085d3-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="085d3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="085d3-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="085d3-139">INPUTS</span></span>

### <span data-ttu-id="085d3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="085d3-140">System.String</span></span>

### <span data-ttu-id="085d3-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="085d3-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="085d3-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="085d3-142">OUTPUTS</span></span>

### <span data-ttu-id="085d3-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="085d3-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="085d3-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="085d3-144">NOTES</span></span>

## <span data-ttu-id="085d3-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="085d3-145">RELATED LINKS</span></span>
