---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 9304471b12f33d677f493a3ee6803a1219d9f977
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009142"
---
# <span data-ttu-id="daaf2-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="daaf2-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="daaf2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="daaf2-102">SYNOPSIS</span></span>
<span data-ttu-id="daaf2-103">Ruft eine eingehende NAT-Regelkonfiguration für ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="daaf2-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="daaf2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="daaf2-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daaf2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="daaf2-105">DESCRIPTION</span></span>
<span data-ttu-id="daaf2-106">Das Cmdlet " **Get-AzLoadBalancerInboundNatRuleConfig** " ruft mindestens eine eingehende Netzwerkadressübersetzung (NAT)-Regeln in einem Azure Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="daaf2-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="daaf2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="daaf2-107">EXAMPLES</span></span>

### <span data-ttu-id="daaf2-108">Beispiel 1: Abrufen einer eingehenden NAT-Regelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="daaf2-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="daaf2-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="daaf2-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="daaf2-110">Der zweite Befehl ruft die zugeordnete NAT-Regel namens MyInboundNatRule1 vom Lastenausgleichsmodul in $SLB ab.</span><span class="sxs-lookup"><span data-stu-id="daaf2-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="daaf2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="daaf2-111">PARAMETERS</span></span>

### <span data-ttu-id="daaf2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daaf2-112">-DefaultProfile</span></span>
<span data-ttu-id="daaf2-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="daaf2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daaf2-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="daaf2-114">-LoadBalancer</span></span>
<span data-ttu-id="daaf2-115">Gibt das Load Balancer an, das der eingehenden NAT-Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="daaf2-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="daaf2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="daaf2-116">-Name</span></span>
<span data-ttu-id="daaf2-117">Gibt den Namen der zu erhaltenden eingehenden NAT-Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="daaf2-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="daaf2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daaf2-118">CommonParameters</span></span>
<span data-ttu-id="daaf2-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daaf2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daaf2-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="daaf2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daaf2-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="daaf2-121">INPUTS</span></span>

### <span data-ttu-id="daaf2-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="daaf2-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="daaf2-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="daaf2-123">OUTPUTS</span></span>

### <span data-ttu-id="daaf2-124">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="daaf2-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="daaf2-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="daaf2-125">NOTES</span></span>

## <span data-ttu-id="daaf2-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="daaf2-126">RELATED LINKS</span></span>

[<span data-ttu-id="daaf2-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="daaf2-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="daaf2-128">Neu – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="daaf2-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="daaf2-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="daaf2-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="daaf2-130">Satz-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="daaf2-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


