---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 9304471b12f33d677f493a3ee6803a1219d9f977
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358880"
---
# <span data-ttu-id="dced9-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dced9-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="dced9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dced9-102">SYNOPSIS</span></span>
<span data-ttu-id="dced9-103">Ruft eine eingehende NAT-Regelkonfiguration für einen Lastenausgleich ab.</span><span class="sxs-lookup"><span data-stu-id="dced9-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="dced9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dced9-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dced9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dced9-105">DESCRIPTION</span></span>
<span data-ttu-id="dced9-106">Das **Cmdlet "Get-AzLoadBalancerInboundNatRuleConfig"** ruft eine oder mehrere REGELN für die eingehende Netzwerkadressenübersetzung (Nat) in einem Azure Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="dced9-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="dced9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dced9-107">EXAMPLES</span></span>

### <span data-ttu-id="dced9-108">Beispiel 1: Erhalten einer eingehenden NAT-Regelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="dced9-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="dced9-109">Der erste Befehl ruft den Lastenausgleich namens "MyLoadBalancer" ab und speichert ihn in der Variablen $slb.</span><span class="sxs-lookup"><span data-stu-id="dced9-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="dced9-110">Der zweite Befehl ruft die zugeordnete NAT-Regel namens "MyInboundNatRule1" aus dem Lastenausgleich in $slb.</span><span class="sxs-lookup"><span data-stu-id="dced9-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="dced9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dced9-111">PARAMETERS</span></span>

### <span data-ttu-id="dced9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dced9-112">-DefaultProfile</span></span>
<span data-ttu-id="dced9-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dced9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dced9-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dced9-114">-LoadBalancer</span></span>
<span data-ttu-id="dced9-115">Gibt den Lastenausgleich an, der der Konfiguration der eingehenden NAT-Regel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="dced9-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="dced9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="dced9-116">-Name</span></span>
<span data-ttu-id="dced9-117">Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="dced9-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="dced9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dced9-118">CommonParameters</span></span>
<span data-ttu-id="dced9-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dced9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dced9-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dced9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dced9-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dced9-121">INPUTS</span></span>

### <span data-ttu-id="dced9-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dced9-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dced9-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dced9-123">OUTPUTS</span></span>

### <span data-ttu-id="dced9-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="dced9-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="dced9-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dced9-125">NOTES</span></span>

## <span data-ttu-id="dced9-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dced9-126">RELATED LINKS</span></span>

[<span data-ttu-id="dced9-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dced9-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="dced9-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dced9-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="dced9-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dced9-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="dced9-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dced9-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


