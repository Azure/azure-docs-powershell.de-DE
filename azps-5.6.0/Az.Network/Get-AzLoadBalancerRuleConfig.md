---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d5782ea85a97df723967d73cf2716d837477f01d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945995"
---
# <span data-ttu-id="4cf43-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4cf43-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="4cf43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cf43-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf43-103">Ruft die Regelkonfiguration für einen Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="4cf43-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="4cf43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cf43-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cf43-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cf43-105">DESCRIPTION</span></span>
<span data-ttu-id="4cf43-106">Das **Get-AzLoadBalancerRuleConfig-Cmdlet** ruft eine oder mehrere Regelkonfigurationen für einen Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="4cf43-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="4cf43-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4cf43-107">EXAMPLES</span></span>

### <span data-ttu-id="4cf43-108">Beispiel 1: Erhalten der Regelkonfiguration eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="4cf43-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="4cf43-109">Der erste Befehl ruft den Load Balancer mit dem Namen MyLoadBalancer ab und speichert ihn dann in der Variablen $slb.</span><span class="sxs-lookup"><span data-stu-id="4cf43-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="4cf43-110">Der zweite Befehl ruft die zugeordnete Regelkonfiguration mit dem Namen MyLBrulename aus dem Load Balancer in $slb.</span><span class="sxs-lookup"><span data-stu-id="4cf43-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="4cf43-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4cf43-111">PARAMETERS</span></span>

### <span data-ttu-id="4cf43-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf43-112">-DefaultProfile</span></span>
<span data-ttu-id="4cf43-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4cf43-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cf43-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cf43-114">-LoadBalancer</span></span>
<span data-ttu-id="4cf43-115">Gibt den Load Balancer an, der der Regelkonfiguration zugeordnet ist, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="4cf43-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="4cf43-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4cf43-116">-Name</span></span>
<span data-ttu-id="4cf43-117">Gibt den Namen der zu erhaltenden Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="4cf43-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="4cf43-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf43-118">CommonParameters</span></span>
<span data-ttu-id="4cf43-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf43-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf43-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cf43-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf43-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4cf43-121">INPUTS</span></span>

### <span data-ttu-id="4cf43-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cf43-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4cf43-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4cf43-123">OUTPUTS</span></span>

### <span data-ttu-id="4cf43-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="4cf43-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="4cf43-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4cf43-125">NOTES</span></span>

## <span data-ttu-id="4cf43-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4cf43-126">RELATED LINKS</span></span>

[<span data-ttu-id="4cf43-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4cf43-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4cf43-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cf43-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4cf43-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4cf43-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4cf43-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4cf43-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


