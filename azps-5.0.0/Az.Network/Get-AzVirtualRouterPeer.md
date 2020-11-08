---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 363e9518234551f55bf75fb6c93f8b0b70b495ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177109"
---
# <span data-ttu-id="3caab-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="3caab-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="3caab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3caab-102">SYNOPSIS</span></span>
<span data-ttu-id="3caab-103">Ruft einen VirtualRouter-Peer in einem Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3caab-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="3caab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3caab-104">SYNTAX</span></span>

### <span data-ttu-id="3caab-105">VirtualRouterPeerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3caab-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3caab-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3caab-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3caab-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3caab-107">DESCRIPTION</span></span>
<span data-ttu-id="3caab-108">Das Cmdlet " **Get-AzVirtualRouterPeer** " Ruft einen Peer in einem Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3caab-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="3caab-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3caab-109">EXAMPLES</span></span>

### <span data-ttu-id="3caab-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3caab-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="3caab-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3caab-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="3caab-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3caab-112">PARAMETERS</span></span>

### <span data-ttu-id="3caab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3caab-113">-DefaultProfile</span></span>
<span data-ttu-id="3caab-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3caab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3caab-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="3caab-115">-PeerName</span></span>
<span data-ttu-id="3caab-116">Der Name des virtuellen Router-Peers.</span><span class="sxs-lookup"><span data-stu-id="3caab-116">The name of the virtual router peer.</span></span>

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

### <span data-ttu-id="3caab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3caab-117">-ResourceGroupName</span></span>
<span data-ttu-id="3caab-118">Der Ressourcengruppenname des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="3caab-118">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="3caab-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3caab-119">-ResourceId</span></span>
<span data-ttu-id="3caab-120">Die Quelle des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="3caab-120">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="3caab-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="3caab-121">-VirtualRouterName</span></span>
<span data-ttu-id="3caab-122">Der Name des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="3caab-122">The name of the virtual router.</span></span>

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

### <span data-ttu-id="3caab-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3caab-123">CommonParameters</span></span>
<span data-ttu-id="3caab-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3caab-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3caab-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3caab-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3caab-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3caab-126">INPUTS</span></span>

### <span data-ttu-id="3caab-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3caab-127">System.String</span></span>

## <span data-ttu-id="3caab-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3caab-128">OUTPUTS</span></span>

### <span data-ttu-id="3caab-129">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="3caab-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="3caab-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="3caab-130">NOTES</span></span>

## <span data-ttu-id="3caab-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3caab-131">RELATED LINKS</span></span>
