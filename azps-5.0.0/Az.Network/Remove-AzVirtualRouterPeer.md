---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176279"
---
# <span data-ttu-id="3df9a-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="3df9a-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="3df9a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3df9a-102">SYNOPSIS</span></span>
<span data-ttu-id="3df9a-103">Entfernt einen Peer aus einem Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3df9a-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="3df9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3df9a-104">SYNTAX</span></span>

### <span data-ttu-id="3df9a-105">VirtualRouterPeerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3df9a-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3df9a-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3df9a-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3df9a-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3df9a-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3df9a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3df9a-108">DESCRIPTION</span></span>
<span data-ttu-id="3df9a-109">Das Cmdlet " **Remove-AzVirtualRouterPeer** " entfernt einen VirtualRouter-Peer aus einem Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3df9a-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="3df9a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3df9a-110">EXAMPLES</span></span>

### <span data-ttu-id="3df9a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3df9a-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="3df9a-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3df9a-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="3df9a-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3df9a-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="3df9a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3df9a-114">PARAMETERS</span></span>

### <span data-ttu-id="3df9a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3df9a-115">-AsJob</span></span>
<span data-ttu-id="3df9a-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3df9a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3df9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df9a-117">-DefaultProfile</span></span>
<span data-ttu-id="3df9a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3df9a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3df9a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3df9a-119">-Force</span></span>
<span data-ttu-id="3df9a-120">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="3df9a-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3df9a-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3df9a-121">-InputObject</span></span>
<span data-ttu-id="3df9a-122">Das Peer Eingabeobjekt für einen virtuellen Router.</span><span class="sxs-lookup"><span data-stu-id="3df9a-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="3df9a-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="3df9a-123">-PeerName</span></span>
<span data-ttu-id="3df9a-124">Der Name des virtuellen Router-Peers.</span><span class="sxs-lookup"><span data-stu-id="3df9a-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="3df9a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df9a-125">-ResourceGroupName</span></span>
<span data-ttu-id="3df9a-126">Der Name der Ressourcengruppe des virtuellen Routers/Peers.</span><span class="sxs-lookup"><span data-stu-id="3df9a-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="3df9a-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3df9a-127">-ResourceId</span></span>
<span data-ttu-id="3df9a-128">Die Peer Ressourcen-ID des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="3df9a-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="3df9a-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="3df9a-129">-VirtualRouterName</span></span>
<span data-ttu-id="3df9a-130">Der virtuelle Router, auf dem Peer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3df9a-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="3df9a-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3df9a-131">-Confirm</span></span>
<span data-ttu-id="3df9a-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3df9a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3df9a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3df9a-133">-WhatIf</span></span>
<span data-ttu-id="3df9a-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3df9a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3df9a-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3df9a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3df9a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df9a-136">CommonParameters</span></span>
<span data-ttu-id="3df9a-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3df9a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df9a-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3df9a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df9a-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3df9a-139">INPUTS</span></span>

### <span data-ttu-id="3df9a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3df9a-140">System.String</span></span>

### <span data-ttu-id="3df9a-141">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="3df9a-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="3df9a-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3df9a-142">OUTPUTS</span></span>

### <span data-ttu-id="3df9a-143">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3df9a-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="3df9a-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="3df9a-144">NOTES</span></span>

## <span data-ttu-id="3df9a-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3df9a-145">RELATED LINKS</span></span>
