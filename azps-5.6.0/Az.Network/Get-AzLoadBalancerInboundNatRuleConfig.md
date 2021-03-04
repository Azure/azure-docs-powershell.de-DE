---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 816c94281c246762dac41f2e69e080dfec70565d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919896"
---
# <span data-ttu-id="c9eb0-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9eb0-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="c9eb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="c9eb0-103">Ruft eine eingehende NAT-Regelkonfiguration für einen Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="c9eb0-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="c9eb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9eb0-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9eb0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9eb0-105">DESCRIPTION</span></span>
<span data-ttu-id="c9eb0-106">Das **Get-AzLoadBalancerInboundNatRuleConfig-Cmdlet** ruft eine oder mehrere NAT-Regeln (Inbound Network Address Translation) in einem Azure Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="c9eb0-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="c9eb0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c9eb0-107">EXAMPLES</span></span>

### <span data-ttu-id="c9eb0-108">Beispiel 1: Erhalten einer eingehenden NAT-Regelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="c9eb0-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="c9eb0-109">Der erste Befehl ruft den Load Balancer mit dem Namen MyLoadBalancer ab und speichert ihn in der Variablen $slb.</span><span class="sxs-lookup"><span data-stu-id="c9eb0-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="c9eb0-110">Der zweite Befehl ruft die zugeordnete NAT-Regel mit dem Namen MyInboundNatRule1 aus dem Load Balancer in $slb.</span><span class="sxs-lookup"><span data-stu-id="c9eb0-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="c9eb0-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c9eb0-111">PARAMETERS</span></span>

### <span data-ttu-id="c9eb0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9eb0-112">-DefaultProfile</span></span>
<span data-ttu-id="c9eb0-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9eb0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9eb0-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9eb0-114">-LoadBalancer</span></span>
<span data-ttu-id="c9eb0-115">Gibt den Load Balancer an, der der eingehenden NAT-Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c9eb0-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="c9eb0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c9eb0-116">-Name</span></span>
<span data-ttu-id="c9eb0-117">Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="c9eb0-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="c9eb0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9eb0-118">CommonParameters</span></span>
<span data-ttu-id="c9eb0-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9eb0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9eb0-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9eb0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9eb0-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c9eb0-121">INPUTS</span></span>

### <span data-ttu-id="c9eb0-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9eb0-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c9eb0-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c9eb0-123">OUTPUTS</span></span>

### <span data-ttu-id="c9eb0-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="c9eb0-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="c9eb0-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c9eb0-125">NOTES</span></span>

## <span data-ttu-id="c9eb0-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c9eb0-126">RELATED LINKS</span></span>

[<span data-ttu-id="c9eb0-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9eb0-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c9eb0-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9eb0-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c9eb0-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9eb0-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c9eb0-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9eb0-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


