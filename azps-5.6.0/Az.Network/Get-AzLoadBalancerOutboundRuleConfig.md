---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: fc3b34e2fb9f91684aee2427d4271e6fab08843f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946006"
---
# <span data-ttu-id="61377-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="61377-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="61377-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61377-102">SYNOPSIS</span></span>
<span data-ttu-id="61377-103">Ruft eine ausgehende Regelkonfiguration in einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="61377-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="61377-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61377-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61377-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61377-105">DESCRIPTION</span></span>
<span data-ttu-id="61377-106">Das **Get-AzLoadBalancerOutboundRuleConfig-Cmdlet** ruft eine ausgehende Regelkonfiguration oder eine Liste ausgehender Regelkonfigurationen in einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="61377-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="61377-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="61377-107">EXAMPLES</span></span>

### <span data-ttu-id="61377-108">Beispiel 1: Erhalten einer ausgehenden Regelkonfiguration in einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="61377-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="61377-109">Der erste Befehl ruft den Load Balancer mit dem Namen MyLoadBalancer ab und speichert ihn dann in der Variablen $slb.</span><span class="sxs-lookup"><span data-stu-id="61377-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="61377-110">Der zweite Befehl ruft die ausgehende Regelkonfiguration mit dem Namen MyRule ab, die diesem Lastenausgleich zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="61377-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="61377-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="61377-111">PARAMETERS</span></span>

### <span data-ttu-id="61377-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61377-112">-DefaultProfile</span></span>
<span data-ttu-id="61377-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61377-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61377-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="61377-114">-LoadBalancer</span></span>
<span data-ttu-id="61377-115">Der Verweis auf die Load Balancer-Ressource.</span><span class="sxs-lookup"><span data-stu-id="61377-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="61377-116">-Name</span><span class="sxs-lookup"><span data-stu-id="61377-116">-Name</span></span>
<span data-ttu-id="61377-117">Name der ausgehenden Regel.</span><span class="sxs-lookup"><span data-stu-id="61377-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="61377-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61377-118">CommonParameters</span></span>
<span data-ttu-id="61377-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61377-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61377-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61377-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61377-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="61377-121">INPUTS</span></span>

### <span data-ttu-id="61377-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="61377-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="61377-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="61377-123">OUTPUTS</span></span>

### <span data-ttu-id="61377-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="61377-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="61377-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="61377-125">NOTES</span></span>

## <span data-ttu-id="61377-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="61377-126">RELATED LINKS</span></span>

[<span data-ttu-id="61377-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="61377-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="61377-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="61377-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="61377-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="61377-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="61377-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="61377-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
