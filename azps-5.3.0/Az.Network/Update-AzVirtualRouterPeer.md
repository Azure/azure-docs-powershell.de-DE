---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 242a3985d75e0a741c5e2175c098139b448f3e70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473354"
---
# <span data-ttu-id="01c40-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="01c40-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="01c40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01c40-102">SYNOPSIS</span></span>
<span data-ttu-id="01c40-103">Aktualisieren eines Peers in Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="01c40-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="01c40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01c40-104">SYNTAX</span></span>

### <span data-ttu-id="01c40-105">VirtualRouterNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="01c40-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01c40-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="01c40-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01c40-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01c40-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01c40-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01c40-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01c40-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01c40-109">DESCRIPTION</span></span>
<span data-ttu-id="01c40-110">Das **Cmdlet "Update-AzVirtualRouterPeer"** aktualisiert einen VirtualRouter Peer auf ein Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="01c40-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="01c40-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01c40-111">EXAMPLES</span></span>

### <span data-ttu-id="01c40-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01c40-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="01c40-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="01c40-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="01c40-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="01c40-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="01c40-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01c40-115">PARAMETERS</span></span>

### <span data-ttu-id="01c40-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01c40-116">-AsJob</span></span>
<span data-ttu-id="01c40-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="01c40-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01c40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c40-118">-DefaultProfile</span></span>
<span data-ttu-id="01c40-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01c40-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01c40-120">-Force</span><span class="sxs-lookup"><span data-stu-id="01c40-120">-Force</span></span>
<span data-ttu-id="01c40-121">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="01c40-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="01c40-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01c40-122">-InputObject</span></span>
<span data-ttu-id="01c40-123">Das Eingabeobjekt des virtuellen Router-Peers.</span><span class="sxs-lookup"><span data-stu-id="01c40-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="01c40-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="01c40-124">-PeerAsn</span></span>
<span data-ttu-id="01c40-125">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="01c40-125">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c40-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="01c40-126">-PeerIp</span></span>
<span data-ttu-id="01c40-127">Peer Ip.</span><span class="sxs-lookup"><span data-stu-id="01c40-127">Peer Ip.</span></span>

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

### <span data-ttu-id="01c40-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="01c40-128">-PeerName</span></span>
<span data-ttu-id="01c40-129">Der Name des Peers des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="01c40-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="01c40-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c40-130">-ResourceGroupName</span></span>
<span data-ttu-id="01c40-131">Der Ressourcengruppenname des virtuellen Routers/Peers.</span><span class="sxs-lookup"><span data-stu-id="01c40-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="01c40-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01c40-132">-ResourceId</span></span>
<span data-ttu-id="01c40-133">Die Id der Peerressource des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="01c40-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="01c40-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="01c40-134">-VirtualRouterName</span></span>
<span data-ttu-id="01c40-135">Der virtuelle Router, auf dem Peer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="01c40-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="01c40-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01c40-136">-Confirm</span></span>
<span data-ttu-id="01c40-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01c40-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c40-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="01c40-138">-WhatIf</span></span>
<span data-ttu-id="01c40-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01c40-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01c40-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01c40-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c40-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c40-141">CommonParameters</span></span>
<span data-ttu-id="01c40-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01c40-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c40-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01c40-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c40-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01c40-144">INPUTS</span></span>

### <span data-ttu-id="01c40-145">System.String</span><span class="sxs-lookup"><span data-stu-id="01c40-145">System.String</span></span>

### <span data-ttu-id="01c40-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="01c40-146">System.UInt32</span></span>

### <span data-ttu-id="01c40-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="01c40-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="01c40-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01c40-148">OUTPUTS</span></span>

### <span data-ttu-id="01c40-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="01c40-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="01c40-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="01c40-150">NOTES</span></span>

## <span data-ttu-id="01c40-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="01c40-151">RELATED LINKS</span></span>
