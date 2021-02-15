---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172473"
---
# <span data-ttu-id="4becd-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="4becd-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="4becd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4becd-102">SYNOPSIS</span></span>
<span data-ttu-id="4becd-103">Entfernt einen Peer aus Einem Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="4becd-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="4becd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4becd-104">SYNTAX</span></span>

### <span data-ttu-id="4becd-105">VirtualRouterPeerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4becd-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4becd-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4becd-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4becd-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4becd-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4becd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4becd-108">DESCRIPTION</span></span>
<span data-ttu-id="4becd-109">Das **Cmdlet "Remove-AzVirtualRouterPeer"** entfernt einen VirtualRouter-Peer aus einem Azure VirtualRouter-</span><span class="sxs-lookup"><span data-stu-id="4becd-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="4becd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4becd-110">EXAMPLES</span></span>

### <span data-ttu-id="4becd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4becd-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="4becd-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4becd-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="4becd-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4becd-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="4becd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4becd-114">PARAMETERS</span></span>

### <span data-ttu-id="4becd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4becd-115">-AsJob</span></span>
<span data-ttu-id="4becd-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4becd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4becd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4becd-117">-DefaultProfile</span></span>
<span data-ttu-id="4becd-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4becd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4becd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4becd-119">-Force</span></span>
<span data-ttu-id="4becd-120">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="4becd-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4becd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4becd-121">-InputObject</span></span>
<span data-ttu-id="4becd-122">Das Eingabeobjekt des virtuellen Router-Peers.</span><span class="sxs-lookup"><span data-stu-id="4becd-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="4becd-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="4becd-123">-PeerName</span></span>
<span data-ttu-id="4becd-124">Der Name des Peers des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="4becd-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="4becd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4becd-125">-ResourceGroupName</span></span>
<span data-ttu-id="4becd-126">Der Ressourcengruppenname des virtuellen Routers/Peers.</span><span class="sxs-lookup"><span data-stu-id="4becd-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="4becd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4becd-127">-ResourceId</span></span>
<span data-ttu-id="4becd-128">Die Id der Peerressource des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="4becd-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="4becd-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="4becd-129">-VirtualRouterName</span></span>
<span data-ttu-id="4becd-130">Der virtuelle Router, auf dem Peer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4becd-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="4becd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4becd-131">-Confirm</span></span>
<span data-ttu-id="4becd-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4becd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4becd-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4becd-133">-WhatIf</span></span>
<span data-ttu-id="4becd-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4becd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4becd-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4becd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4becd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4becd-136">CommonParameters</span></span>
<span data-ttu-id="4becd-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4becd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4becd-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4becd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4becd-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4becd-139">INPUTS</span></span>

### <span data-ttu-id="4becd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4becd-140">System.String</span></span>

### <span data-ttu-id="4becd-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="4becd-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="4becd-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4becd-142">OUTPUTS</span></span>

### <span data-ttu-id="4becd-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="4becd-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="4becd-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4becd-144">NOTES</span></span>

## <span data-ttu-id="4becd-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4becd-145">RELATED LINKS</span></span>
