---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 8d7bbf361ee2fc2bf06e1bf3ce6a9bfe1e295338
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847452"
---
# <span data-ttu-id="16f1f-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="16f1f-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="16f1f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="16f1f-103">Aktualisieren eines Peers in einem Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="16f1f-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="16f1f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16f1f-104">SYNTAX</span></span>

### <span data-ttu-id="16f1f-105">VirtualRouterNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="16f1f-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f1f-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="16f1f-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16f1f-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16f1f-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f1f-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16f1f-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16f1f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16f1f-109">DESCRIPTION</span></span>
<span data-ttu-id="16f1f-110">Das Cmdlet **Update-AzVirtualRouterPeer** aktualisiert einen VirtualRouter-Peer auf eine Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="16f1f-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="16f1f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16f1f-111">EXAMPLES</span></span>

### <span data-ttu-id="16f1f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16f1f-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="16f1f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="16f1f-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="16f1f-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="16f1f-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="16f1f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="16f1f-115">PARAMETERS</span></span>

### <span data-ttu-id="16f1f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16f1f-116">-AsJob</span></span>
<span data-ttu-id="16f1f-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="16f1f-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f1f-118">-DefaultProfile</span></span>
<span data-ttu-id="16f1f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16f1f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f1f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="16f1f-120">-Force</span></span>
<span data-ttu-id="16f1f-121">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="16f1f-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f1f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="16f1f-122">-InputObject</span></span>
<span data-ttu-id="16f1f-123">Das Peer Eingabeobjekt für einen virtuellen Router.</span><span class="sxs-lookup"><span data-stu-id="16f1f-123">The virtual router peer input object.</span></span>

```yaml
Type: PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16f1f-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="16f1f-124">-PeerAsn</span></span>
<span data-ttu-id="16f1f-125">Peer-ASN.</span><span class="sxs-lookup"><span data-stu-id="16f1f-125">Peer ASN.</span></span>

```yaml
Type: UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f1f-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="16f1f-126">-PeerIp</span></span>
<span data-ttu-id="16f1f-127">Peer-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="16f1f-127">Peer Ip.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f1f-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="16f1f-128">-PeerName</span></span>
<span data-ttu-id="16f1f-129">Der Name des virtuellen Router-Peers.</span><span class="sxs-lookup"><span data-stu-id="16f1f-129">The name of the virtual router Peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f1f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16f1f-130">-ResourceGroupName</span></span>
<span data-ttu-id="16f1f-131">Der Name der Ressourcengruppe des virtuellen Routers/Peers.</span><span class="sxs-lookup"><span data-stu-id="16f1f-131">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f1f-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="16f1f-132">-ResourceId</span></span>
<span data-ttu-id="16f1f-133">Die Peer Ressourcen-ID des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="16f1f-133">The virtual router peer resource Id.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f1f-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="16f1f-134">-VirtualRouterName</span></span>
<span data-ttu-id="16f1f-135">Der virtuelle Router, auf dem Peer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="16f1f-135">The virtual router where peer exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f1f-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16f1f-136">-Confirm</span></span>
<span data-ttu-id="16f1f-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16f1f-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f1f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16f1f-138">-WhatIf</span></span>
<span data-ttu-id="16f1f-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16f1f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16f1f-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16f1f-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f1f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f1f-141">CommonParameters</span></span>
<span data-ttu-id="16f1f-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16f1f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f1f-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16f1f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f1f-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16f1f-144">INPUTS</span></span>

### <span data-ttu-id="16f1f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="16f1f-145">System.String</span></span>

### <span data-ttu-id="16f1f-146">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="16f1f-146">System.UInt32</span></span>

### <span data-ttu-id="16f1f-147">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="16f1f-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="16f1f-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16f1f-148">OUTPUTS</span></span>

### <span data-ttu-id="16f1f-149">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="16f1f-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="16f1f-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="16f1f-150">NOTES</span></span>

## <span data-ttu-id="16f1f-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16f1f-151">RELATED LINKS</span></span>
