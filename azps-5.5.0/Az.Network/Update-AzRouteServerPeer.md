---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
ms.openlocfilehash: 79d907a5ac1b75bdc65d6ea79ffc6c9dea911479
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160532"
---
# <span data-ttu-id="2115c-101">Update-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="2115c-101">Update-AzRouteServerPeer</span></span>

## <span data-ttu-id="2115c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2115c-102">SYNOPSIS</span></span>
<span data-ttu-id="2115c-103">Aktualisieren eines Peers in einem Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="2115c-103">Update a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="2115c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2115c-104">SYNTAX</span></span>

### <span data-ttu-id="2115c-105">RouteServerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2115c-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2115c-106">RouteServerNPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2115c-106">RouteServerNPeerNameParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2115c-107">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2115c-107">RouteServerNPeerInputObjectParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -InputObject <PSRouteServerPeer>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2115c-108">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2115c-108">RouteServerNPeerResourceIdParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -ResourceId <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2115c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2115c-109">DESCRIPTION</span></span>
<span data-ttu-id="2115c-110">Das **Cmdlet "Update-AzRouteServerPeer"** aktualisiert einen RouteServer-Peer auf einen Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="2115c-110">The **Update-AzRouteServerPeer** cmdlet updates a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="2115c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2115c-111">EXAMPLES</span></span>

### <span data-ttu-id="2115c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2115c-112">Example 1</span></span>
```powershell
PS C:\> Update-AzRouteServerPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="2115c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2115c-113">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/csr'
Update-AzRouteServerPeer -ResourceId $routeServerPeerId  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="2115c-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2115c-114">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServer -RouteServerName routeServer -PeerName csr
Update-AzRouteServerPeer -ResourceGroupName routeServerRG -InputObject $routeServerPeer  -RouteServerName routeServer
```

## <span data-ttu-id="2115c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2115c-115">PARAMETERS</span></span>

### <span data-ttu-id="2115c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2115c-116">-AsJob</span></span>
<span data-ttu-id="2115c-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2115c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2115c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2115c-118">-DefaultProfile</span></span>
<span data-ttu-id="2115c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2115c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2115c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2115c-120">-Force</span></span>
<span data-ttu-id="2115c-121">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="2115c-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2115c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2115c-122">-InputObject</span></span>
<span data-ttu-id="2115c-123">Das Eingabeobjekt für den Routenserver-Peer.</span><span class="sxs-lookup"><span data-stu-id="2115c-123">The route server peer input object.</span></span>

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

### <span data-ttu-id="2115c-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="2115c-124">-PeerAsn</span></span>
<span data-ttu-id="2115c-125">ASN des Remoteroutenserver-Peers.</span><span class="sxs-lookup"><span data-stu-id="2115c-125">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2115c-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="2115c-126">-PeerIp</span></span>
<span data-ttu-id="2115c-127">IP des Remoteroutenserver-Peers.</span><span class="sxs-lookup"><span data-stu-id="2115c-127">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="2115c-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="2115c-128">-PeerName</span></span>
<span data-ttu-id="2115c-129">Der Name des Routenserver-Peers.</span><span class="sxs-lookup"><span data-stu-id="2115c-129">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="2115c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2115c-130">-ResourceGroupName</span></span>
<span data-ttu-id="2115c-131">Der Ressourcengruppenname des Routeservers/Peers.</span><span class="sxs-lookup"><span data-stu-id="2115c-131">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="2115c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2115c-132">-ResourceId</span></span>
<span data-ttu-id="2115c-133">Die Peerressourcen-ID des Routeservers.</span><span class="sxs-lookup"><span data-stu-id="2115c-133">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="2115c-134">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="2115c-134">-RouteServerName</span></span>
<span data-ttu-id="2115c-135">Der Routeserver, auf dem Peer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2115c-135">The route server where peer exists.</span></span>

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

### <span data-ttu-id="2115c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2115c-136">-Confirm</span></span>
<span data-ttu-id="2115c-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2115c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2115c-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2115c-138">-WhatIf</span></span>
<span data-ttu-id="2115c-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2115c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2115c-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2115c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2115c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2115c-141">CommonParameters</span></span>
<span data-ttu-id="2115c-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2115c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2115c-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2115c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2115c-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2115c-144">INPUTS</span></span>

### <span data-ttu-id="2115c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="2115c-145">System.String</span></span>

### <span data-ttu-id="2115c-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="2115c-146">System.UInt32</span></span>

### <span data-ttu-id="2115c-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="2115c-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="2115c-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2115c-148">OUTPUTS</span></span>

### <span data-ttu-id="2115c-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="2115c-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="2115c-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2115c-150">NOTES</span></span>

## <span data-ttu-id="2115c-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2115c-151">RELATED LINKS</span></span>
