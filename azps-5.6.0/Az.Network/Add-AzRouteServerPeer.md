---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
ms.openlocfilehash: 430292ba3a387a0b2a0285b26c147c375f114398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932504"
---
# <span data-ttu-id="f0a92-101">Add-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="f0a92-101">Add-AzRouteServerPeer</span></span>

## <span data-ttu-id="f0a92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0a92-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a92-103">Hinzufügen eines Peers zu einem Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="f0a92-103">Add a peer to an Azure RouteServer</span></span>

## <span data-ttu-id="f0a92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0a92-104">SYNTAX</span></span>

### <span data-ttu-id="f0a92-105">RouteServerNPeerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0a92-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0a92-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0a92-106">RouteServerNameParameterSet</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0a92-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0a92-107">DESCRIPTION</span></span>
<span data-ttu-id="f0a92-108">Das **Add-AzRouteServerPeer-Cmdlet** fügt einem Azure RouteServer einen RouteServer-Peer hinzu.</span><span class="sxs-lookup"><span data-stu-id="f0a92-108">The **Add-AzRouteServerPeer** cmdlet adds a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="f0a92-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0a92-109">EXAMPLES</span></span>

### <span data-ttu-id="f0a92-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f0a92-110">Example 1</span></span>
```powershell
PS C:\> Add-AzRouteServerPeer -ResourceGroupName $rgname -RouteServerName $routeServerName -PeerName $peerName -PeerIp "192.168.1.5" -PeerAsn "20000"
```

## <span data-ttu-id="f0a92-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f0a92-111">PARAMETERS</span></span>

### <span data-ttu-id="f0a92-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0a92-112">-AsJob</span></span>
<span data-ttu-id="f0a92-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f0a92-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0a92-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a92-114">-DefaultProfile</span></span>
<span data-ttu-id="f0a92-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0a92-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0a92-116">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="f0a92-116">-Force</span></span>
<span data-ttu-id="f0a92-117">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="f0a92-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f0a92-118">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="f0a92-118">-PeerAsn</span></span>
<span data-ttu-id="f0a92-119">ASN des Remoteroutenserver-Peers.</span><span class="sxs-lookup"><span data-stu-id="f0a92-119">ASN of remote route server peer.</span></span>

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

### <span data-ttu-id="f0a92-120">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="f0a92-120">-PeerIp</span></span>
<span data-ttu-id="f0a92-121">Ip des Remoteroutenserver-Peers.</span><span class="sxs-lookup"><span data-stu-id="f0a92-121">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="f0a92-122">-PeerName</span><span class="sxs-lookup"><span data-stu-id="f0a92-122">-PeerName</span></span>
<span data-ttu-id="f0a92-123">Der Name des Routenserver-Peers.</span><span class="sxs-lookup"><span data-stu-id="f0a92-123">The name of the route server peer.</span></span>

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

### <span data-ttu-id="f0a92-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0a92-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0a92-125">Der Ressourcengruppenname des Routenservers/Peers.</span><span class="sxs-lookup"><span data-stu-id="f0a92-125">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="f0a92-126">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="f0a92-126">-RouteServerName</span></span>
<span data-ttu-id="f0a92-127">Der Routenserver, auf dem peer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f0a92-127">The route server where peer exists.</span></span>

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

### <span data-ttu-id="f0a92-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0a92-128">-Confirm</span></span>
<span data-ttu-id="f0a92-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0a92-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0a92-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0a92-130">-WhatIf</span></span>
<span data-ttu-id="f0a92-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0a92-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0a92-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0a92-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0a92-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a92-133">CommonParameters</span></span>
<span data-ttu-id="f0a92-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0a92-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a92-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0a92-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a92-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0a92-136">INPUTS</span></span>

### <span data-ttu-id="f0a92-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f0a92-137">System.String</span></span>

### <span data-ttu-id="f0a92-138">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="f0a92-138">System.UInt32</span></span>

## <span data-ttu-id="f0a92-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0a92-139">OUTPUTS</span></span>

### <span data-ttu-id="f0a92-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="f0a92-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="f0a92-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f0a92-141">NOTES</span></span>

## <span data-ttu-id="f0a92-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f0a92-142">RELATED LINKS</span></span>
