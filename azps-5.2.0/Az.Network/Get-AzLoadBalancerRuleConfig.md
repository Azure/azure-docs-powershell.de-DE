---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299856"
---
# <span data-ttu-id="e94ed-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e94ed-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="e94ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e94ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e94ed-103">Ruft die Regelkonfiguration für einen Lastenausgleich ab.</span><span class="sxs-lookup"><span data-stu-id="e94ed-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="e94ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e94ed-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e94ed-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e94ed-105">DESCRIPTION</span></span>
<span data-ttu-id="e94ed-106">Das **Cmdlet "Get-AzLoadBalancerRuleConfig"** ruft eine oder mehrere Regelkonfigurationen für einen Lastenausgleich ab.</span><span class="sxs-lookup"><span data-stu-id="e94ed-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="e94ed-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e94ed-107">EXAMPLES</span></span>

### <span data-ttu-id="e94ed-108">Beispiel 1: Regelkonfiguration eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="e94ed-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="e94ed-109">Der erste Befehl ruft den Lastenausgleich namens "MyLoadBalancer" ab und speichert ihn dann im Variablenspeicher $slb.</span><span class="sxs-lookup"><span data-stu-id="e94ed-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="e94ed-110">Der zweite Befehl ruft die zugeordnete Regelkonfiguration namens "MyLBrulename" aus dem Lastenausgleich in $slb.</span><span class="sxs-lookup"><span data-stu-id="e94ed-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="e94ed-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e94ed-111">PARAMETERS</span></span>

### <span data-ttu-id="e94ed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e94ed-112">-DefaultProfile</span></span>
<span data-ttu-id="e94ed-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e94ed-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e94ed-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e94ed-114">-LoadBalancer</span></span>
<span data-ttu-id="e94ed-115">Gibt den Lastenausgleich an, der der Regelkonfiguration zugeordnet ist, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="e94ed-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="e94ed-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e94ed-116">-Name</span></span>
<span data-ttu-id="e94ed-117">Gibt den Namen der regelkonfiguration an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="e94ed-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="e94ed-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94ed-118">CommonParameters</span></span>
<span data-ttu-id="e94ed-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e94ed-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94ed-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e94ed-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94ed-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e94ed-121">INPUTS</span></span>

### <span data-ttu-id="e94ed-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e94ed-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e94ed-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e94ed-123">OUTPUTS</span></span>

### <span data-ttu-id="e94ed-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="e94ed-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="e94ed-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e94ed-125">NOTES</span></span>

## <span data-ttu-id="e94ed-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e94ed-126">RELATED LINKS</span></span>

[<span data-ttu-id="e94ed-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e94ed-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="e94ed-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e94ed-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e94ed-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e94ed-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="e94ed-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e94ed-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


