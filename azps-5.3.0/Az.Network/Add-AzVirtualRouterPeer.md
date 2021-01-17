---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 2cb7bc759847af456286bfc611904922a26dc443
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467412"
---
# <span data-ttu-id="e5572-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="e5572-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="e5572-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5572-102">SYNOPSIS</span></span>
<span data-ttu-id="e5572-103">Hinzufügen eines Peers zu Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e5572-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="e5572-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5572-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5572-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5572-105">DESCRIPTION</span></span>
<span data-ttu-id="e5572-106">Das **Cmdlet "Add-AzVirtualRouterPeer"** fügt einem Azure VirtualRouter-Konto einen VirtualRouter-Peer hinzu.</span><span class="sxs-lookup"><span data-stu-id="e5572-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="e5572-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e5572-107">EXAMPLES</span></span>

### <span data-ttu-id="e5572-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5572-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="e5572-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5572-109">PARAMETERS</span></span>

### <span data-ttu-id="e5572-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5572-110">-AsJob</span></span>
<span data-ttu-id="e5572-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e5572-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5572-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5572-112">-DefaultProfile</span></span>
<span data-ttu-id="e5572-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5572-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5572-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e5572-114">-Force</span></span>
<span data-ttu-id="e5572-115">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="e5572-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e5572-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="e5572-116">-PeerAsn</span></span>
<span data-ttu-id="e5572-117">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="e5572-117">Peer ASN.</span></span>

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

### <span data-ttu-id="e5572-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="e5572-118">-PeerIp</span></span>
<span data-ttu-id="e5572-119">Peer Ip.</span><span class="sxs-lookup"><span data-stu-id="e5572-119">Peer Ip.</span></span>

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

### <span data-ttu-id="e5572-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="e5572-120">-PeerName</span></span>
<span data-ttu-id="e5572-121">Der Name des Peers des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="e5572-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="e5572-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5572-122">-ResourceGroupName</span></span>
<span data-ttu-id="e5572-123">Der Ressourcengruppenname des virtuellen Routers/Peers.</span><span class="sxs-lookup"><span data-stu-id="e5572-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="e5572-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="e5572-124">-VirtualRouterName</span></span>
<span data-ttu-id="e5572-125">Der virtuelle Router, auf dem Peer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e5572-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="e5572-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5572-126">-Confirm</span></span>
<span data-ttu-id="e5572-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5572-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5572-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e5572-128">-WhatIf</span></span>
<span data-ttu-id="e5572-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5572-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5572-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5572-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5572-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5572-131">CommonParameters</span></span>
<span data-ttu-id="e5572-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5572-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5572-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5572-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5572-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e5572-134">INPUTS</span></span>

### <span data-ttu-id="e5572-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e5572-135">System.String</span></span>

### <span data-ttu-id="e5572-136">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="e5572-136">System.UInt32</span></span>

## <span data-ttu-id="e5572-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e5572-137">OUTPUTS</span></span>

### <span data-ttu-id="e5572-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e5572-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="e5572-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e5572-139">NOTES</span></span>

## <span data-ttu-id="e5572-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e5572-140">RELATED LINKS</span></span>
