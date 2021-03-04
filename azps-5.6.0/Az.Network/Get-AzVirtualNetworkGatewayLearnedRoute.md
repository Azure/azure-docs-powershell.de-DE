---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 8dbc1ad62d11ac6b14897c27b11ebdb7f6fb8cc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922843"
---
# <span data-ttu-id="7ce49-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="7ce49-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="7ce49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ce49-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce49-103">Listet routen auf, die von einem virtuellen Azure-Netzwerkgateway gelernt wurden</span><span class="sxs-lookup"><span data-stu-id="7ce49-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="7ce49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ce49-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ce49-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ce49-105">DESCRIPTION</span></span>
<span data-ttu-id="7ce49-106">Enumerates routes learned by a Azure virtual network gateway from various sources.</span><span class="sxs-lookup"><span data-stu-id="7ce49-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="7ce49-107">Dazu gehören Routen, die über BGP gelernt wurden, sowie statische Routen.</span><span class="sxs-lookup"><span data-stu-id="7ce49-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="7ce49-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ce49-108">EXAMPLES</span></span>

### <span data-ttu-id="7ce49-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ce49-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="7ce49-110">Ruft für das azure virtual network gateway named gatewayname in resource group resourceGroup Routen ab, die dem Azure-Gateway bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="7ce49-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="7ce49-111">Das virtuelle Azure-Netzwerkgateway verfügt in diesem Fall über zwei statische Routen (10.1.0.0/16 und 10.0.0.254/32) sowie eine Route, die über BGP (10.0.0.0/16) gelernt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ce49-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="7ce49-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7ce49-112">PARAMETERS</span></span>

### <span data-ttu-id="7ce49-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ce49-113">-AsJob</span></span>
<span data-ttu-id="7ce49-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7ce49-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ce49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce49-115">-DefaultProfile</span></span>
<span data-ttu-id="7ce49-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ce49-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ce49-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ce49-117">-ResourceGroupName</span></span>
<span data-ttu-id="7ce49-118">Name der Ressourcengruppe "Virtuelles Netzwerkgateway"</span><span class="sxs-lookup"><span data-stu-id="7ce49-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="7ce49-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="7ce49-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="7ce49-120">Name des Virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="7ce49-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="7ce49-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce49-121">CommonParameters</span></span>
<span data-ttu-id="7ce49-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ce49-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce49-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ce49-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce49-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ce49-124">INPUTS</span></span>

### <span data-ttu-id="7ce49-125">System.String</span><span class="sxs-lookup"><span data-stu-id="7ce49-125">System.String</span></span>

## <span data-ttu-id="7ce49-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ce49-126">OUTPUTS</span></span>

### <span data-ttu-id="7ce49-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="7ce49-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="7ce49-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7ce49-128">NOTES</span></span>

## <span data-ttu-id="7ce49-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7ce49-129">RELATED LINKS</span></span>
