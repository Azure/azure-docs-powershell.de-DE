---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 87647d504d47bf3f53b775d68b42ab617485f73d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932475"
---
# <span data-ttu-id="904c9-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="904c9-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="904c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="904c9-102">SYNOPSIS</span></span>
<span data-ttu-id="904c9-103">Hinzufügen eines Peers zu einem Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="904c9-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="904c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="904c9-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="904c9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="904c9-105">DESCRIPTION</span></span>
<span data-ttu-id="904c9-106">Das **Add-AzVirtualRouterPeer-Cmdlet** fügt einem Azure VirtualRouter einen VirtualRouter-Peer hinzu.</span><span class="sxs-lookup"><span data-stu-id="904c9-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="904c9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="904c9-107">EXAMPLES</span></span>

### <span data-ttu-id="904c9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="904c9-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="904c9-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="904c9-109">PARAMETERS</span></span>

### <span data-ttu-id="904c9-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="904c9-110">-AsJob</span></span>
<span data-ttu-id="904c9-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="904c9-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="904c9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="904c9-112">-DefaultProfile</span></span>
<span data-ttu-id="904c9-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="904c9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="904c9-114">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="904c9-114">-Force</span></span>
<span data-ttu-id="904c9-115">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="904c9-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="904c9-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="904c9-116">-PeerAsn</span></span>
<span data-ttu-id="904c9-117">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="904c9-117">Peer ASN.</span></span>

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

### <span data-ttu-id="904c9-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="904c9-118">-PeerIp</span></span>
<span data-ttu-id="904c9-119">Peer Ip.</span><span class="sxs-lookup"><span data-stu-id="904c9-119">Peer Ip.</span></span>

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

### <span data-ttu-id="904c9-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="904c9-120">-PeerName</span></span>
<span data-ttu-id="904c9-121">Der Name des peer virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="904c9-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="904c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="904c9-122">-ResourceGroupName</span></span>
<span data-ttu-id="904c9-123">Der Ressourcengruppenname des virtuellen Routers/Peers.</span><span class="sxs-lookup"><span data-stu-id="904c9-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="904c9-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="904c9-124">-VirtualRouterName</span></span>
<span data-ttu-id="904c9-125">Der virtuelle Router, in dem Peer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="904c9-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="904c9-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="904c9-126">-Confirm</span></span>
<span data-ttu-id="904c9-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="904c9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="904c9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="904c9-128">-WhatIf</span></span>
<span data-ttu-id="904c9-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="904c9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="904c9-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="904c9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="904c9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="904c9-131">CommonParameters</span></span>
<span data-ttu-id="904c9-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="904c9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="904c9-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="904c9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="904c9-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="904c9-134">INPUTS</span></span>

### <span data-ttu-id="904c9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="904c9-135">System.String</span></span>

### <span data-ttu-id="904c9-136">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="904c9-136">System.UInt32</span></span>

## <span data-ttu-id="904c9-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="904c9-137">OUTPUTS</span></span>

### <span data-ttu-id="904c9-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="904c9-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="904c9-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="904c9-139">NOTES</span></span>

## <span data-ttu-id="904c9-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="904c9-140">RELATED LINKS</span></span>
