---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 69665b57e1c378b6a5b134228da479096ba45445
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290189"
---
# <span data-ttu-id="bf9ba-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="bf9ba-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="bf9ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf9ba-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9ba-103">Listet die von einem virtuellen Azure-Netzwerkgateway erlernten Routen auf.</span><span class="sxs-lookup"><span data-stu-id="bf9ba-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="bf9ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf9ba-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf9ba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf9ba-105">DESCRIPTION</span></span>
<span data-ttu-id="bf9ba-106">Aufzählen der von einem virtuellen Azure-Netzwerkgateway erlernten Routen aus verschiedenen Quellen.</span><span class="sxs-lookup"><span data-stu-id="bf9ba-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="bf9ba-107">Dies schließt über BGP erlernte Routen sowie statische Routen ein.</span><span class="sxs-lookup"><span data-stu-id="bf9ba-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="bf9ba-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf9ba-108">EXAMPLES</span></span>

### <span data-ttu-id="bf9ba-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf9ba-109">Example 1</span></span>
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

<span data-ttu-id="bf9ba-110">Ruft für das virtuelle Azure-Netzwerkgateway namens "Gatewayname" in der Ressourcengruppe "resourceGroup" Routen ab, die dem Azure-Gateway bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="bf9ba-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="bf9ba-111">In diesem Fall verfügt das virtuelle Azure-Netzwerkgateway über zwei statische Routen (10.1.0.0/16 und 10.0.0.254/32) sowie eine über BGP (10.0.0.0/16) erlernte Route.</span><span class="sxs-lookup"><span data-stu-id="bf9ba-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="bf9ba-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf9ba-112">PARAMETERS</span></span>

### <span data-ttu-id="bf9ba-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf9ba-113">-AsJob</span></span>
<span data-ttu-id="bf9ba-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bf9ba-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf9ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9ba-115">-DefaultProfile</span></span>
<span data-ttu-id="bf9ba-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf9ba-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf9ba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf9ba-117">-ResourceGroupName</span></span>
<span data-ttu-id="bf9ba-118">Name der Ressourcengruppe des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="bf9ba-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="bf9ba-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="bf9ba-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="bf9ba-120">Name des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="bf9ba-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="bf9ba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9ba-121">CommonParameters</span></span>
<span data-ttu-id="bf9ba-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf9ba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9ba-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf9ba-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9ba-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf9ba-124">INPUTS</span></span>

### <span data-ttu-id="bf9ba-125">System.String</span><span class="sxs-lookup"><span data-stu-id="bf9ba-125">System.String</span></span>

## <span data-ttu-id="bf9ba-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf9ba-126">OUTPUTS</span></span>

### <span data-ttu-id="bf9ba-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="bf9ba-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="bf9ba-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bf9ba-128">NOTES</span></span>

## <span data-ttu-id="bf9ba-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bf9ba-129">RELATED LINKS</span></span>
