---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 43c3b4d17d024eaae06c7d7f891dfd2ea3e08aa9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946007"
---
# <span data-ttu-id="c09b4-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c09b4-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="c09b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c09b4-102">SYNOPSIS</span></span>
<span data-ttu-id="c09b4-103">Ruft eine Testkonfiguration für einen Lastenausgleich ab.</span><span class="sxs-lookup"><span data-stu-id="c09b4-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="c09b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c09b4-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c09b4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c09b4-105">DESCRIPTION</span></span>
<span data-ttu-id="c09b4-106">Das **Get-AzLoadBalancerProbeConfig-Cmdlet** ruft eine oder mehrere Prüfpunktkonfigurationen für einen Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="c09b4-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="c09b4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c09b4-107">EXAMPLES</span></span>

### <span data-ttu-id="c09b4-108">Beispiel 1: So wird die Sondenkonfiguration eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="c09b4-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="c09b4-109">Der erste Befehl ruft den Load Balancer mit dem Namen MyLoadBalancer ab und speichert ihn dann in der Variablen $slb.</span><span class="sxs-lookup"><span data-stu-id="c09b4-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="c09b4-110">Der zweite Befehl ruft die zugehörige Sondenkonfiguration mit dem Namen MyProbe aus dem Load Balancer in $slb.</span><span class="sxs-lookup"><span data-stu-id="c09b4-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="c09b4-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c09b4-111">PARAMETERS</span></span>

### <span data-ttu-id="c09b4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c09b4-112">-DefaultProfile</span></span>
<span data-ttu-id="c09b4-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c09b4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c09b4-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c09b4-114">-LoadBalancer</span></span>
<span data-ttu-id="c09b4-115">Gibt den Load Balancer an, der der Sondenkonfiguration zugeordnet ist, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="c09b4-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c09b4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c09b4-116">-Name</span></span>
<span data-ttu-id="c09b4-117">Gibt den Namen der zu erhaltenden Sondenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="c09b4-117">Specifies the name of the probe configuration to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c09b4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c09b4-118">CommonParameters</span></span>
<span data-ttu-id="c09b4-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c09b4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c09b4-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c09b4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c09b4-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c09b4-121">INPUTS</span></span>

### <span data-ttu-id="c09b4-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c09b4-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c09b4-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c09b4-123">OUTPUTS</span></span>

### <span data-ttu-id="c09b4-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="c09b4-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="c09b4-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c09b4-125">NOTES</span></span>

## <span data-ttu-id="c09b4-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c09b4-126">RELATED LINKS</span></span>

[<span data-ttu-id="c09b4-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c09b4-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="c09b4-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c09b4-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c09b4-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c09b4-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="c09b4-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c09b4-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="c09b4-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c09b4-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


