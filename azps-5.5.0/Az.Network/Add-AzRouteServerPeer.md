---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
ms.openlocfilehash: 70f7573a604ea15c33f1949883503fed2a356e00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159249"
---
# <span data-ttu-id="242a3-101">Add-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="242a3-101">Add-AzRouteServerPeer</span></span>

## <span data-ttu-id="242a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="242a3-102">SYNOPSIS</span></span>
<span data-ttu-id="242a3-103">Hinzufügen eines Peers zu einem Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="242a3-103">Add a peer to an Azure RouteServer</span></span>

## <span data-ttu-id="242a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="242a3-104">SYNTAX</span></span>

### <span data-ttu-id="242a3-105">RouteServerNPeerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="242a3-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="242a3-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="242a3-106">RouteServerNameParameterSet</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="242a3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="242a3-107">DESCRIPTION</span></span>
<span data-ttu-id="242a3-108">Das **Cmdlet "Add-AzRouteServerPeer"** fügt einem Azure RouteServer-Server einen RouteServer-Peer hinzu.</span><span class="sxs-lookup"><span data-stu-id="242a3-108">The **Add-AzRouteServerPeer** cmdlet adds a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="242a3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="242a3-109">EXAMPLES</span></span>

### <span data-ttu-id="242a3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="242a3-110">Example 1</span></span>
```powershell
PS C:\> Add-AzRouteServerPeer -ResourceGroupName $rgname -RouteServerName $routeServerName -PeerName $peerName -PeerIp "192.168.1.5" -PeerAsn "20000"
```

## <span data-ttu-id="242a3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="242a3-111">PARAMETERS</span></span>

### <span data-ttu-id="242a3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="242a3-112">-AsJob</span></span>
<span data-ttu-id="242a3-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="242a3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="242a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="242a3-114">-DefaultProfile</span></span>
<span data-ttu-id="242a3-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="242a3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="242a3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="242a3-116">-Force</span></span>
<span data-ttu-id="242a3-117">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="242a3-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="242a3-118">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="242a3-118">-PeerAsn</span></span>
<span data-ttu-id="242a3-119">ASN des Remoteroutenserver-Peers.</span><span class="sxs-lookup"><span data-stu-id="242a3-119">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="242a3-120">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="242a3-120">-PeerIp</span></span>
<span data-ttu-id="242a3-121">IP des Remoteroutenserver-Peers.</span><span class="sxs-lookup"><span data-stu-id="242a3-121">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="242a3-122">-PeerName</span><span class="sxs-lookup"><span data-stu-id="242a3-122">-PeerName</span></span>
<span data-ttu-id="242a3-123">Der Name des Routenserver-Peers.</span><span class="sxs-lookup"><span data-stu-id="242a3-123">The name of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="242a3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="242a3-124">-ResourceGroupName</span></span>
<span data-ttu-id="242a3-125">Der Ressourcengruppenname des Routeservers/Peers.</span><span class="sxs-lookup"><span data-stu-id="242a3-125">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="242a3-126">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="242a3-126">-RouteServerName</span></span>
<span data-ttu-id="242a3-127">Der Routeserver, auf dem Peer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="242a3-127">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="242a3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="242a3-128">-Confirm</span></span>
<span data-ttu-id="242a3-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="242a3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="242a3-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="242a3-130">-WhatIf</span></span>
<span data-ttu-id="242a3-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="242a3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="242a3-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="242a3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="242a3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="242a3-133">CommonParameters</span></span>
<span data-ttu-id="242a3-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="242a3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="242a3-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="242a3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="242a3-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="242a3-136">INPUTS</span></span>

### <span data-ttu-id="242a3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="242a3-137">System.String</span></span>

### <span data-ttu-id="242a3-138">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="242a3-138">System.UInt32</span></span>

## <span data-ttu-id="242a3-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="242a3-139">OUTPUTS</span></span>

### <span data-ttu-id="242a3-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="242a3-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="242a3-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="242a3-141">NOTES</span></span>

## <span data-ttu-id="242a3-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="242a3-142">RELATED LINKS</span></span>
