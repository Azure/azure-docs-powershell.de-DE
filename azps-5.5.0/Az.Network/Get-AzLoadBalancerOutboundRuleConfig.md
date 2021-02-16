---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: b8683d461fe442ec0ad20098766d975b4cd6ae73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161089"
---
# <span data-ttu-id="95de0-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95de0-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="95de0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95de0-102">SYNOPSIS</span></span>
<span data-ttu-id="95de0-103">Ruft eine ausgehende Regelkonfiguration in einem Lastenausgleich ab.</span><span class="sxs-lookup"><span data-stu-id="95de0-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="95de0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95de0-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95de0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95de0-105">DESCRIPTION</span></span>
<span data-ttu-id="95de0-106">Das **Cmdlet "Get-AzLoadBalancerOutboundRuleConfig"** ruft eine ausgehende Regelkonfiguration oder eine Liste der ausgehenden Regelkonfigurationen in einem Lastenausgleich ab.</span><span class="sxs-lookup"><span data-stu-id="95de0-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="95de0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95de0-107">EXAMPLES</span></span>

### <span data-ttu-id="95de0-108">Beispiel 1: Erhalten einer ausgehenden Regelkonfiguration in einem Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="95de0-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="95de0-109">Der erste Befehl ruft den Lastenausgleich namens "MyLoadBalancer" ab und speichert ihn dann im Variablenspeicher $slb.</span><span class="sxs-lookup"><span data-stu-id="95de0-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="95de0-110">Der zweite Befehl ruft die ausgehende Regelkonfiguration namens "MyRule" ab, die diesem Lastenausgleich zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="95de0-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="95de0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95de0-111">PARAMETERS</span></span>

### <span data-ttu-id="95de0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95de0-112">-DefaultProfile</span></span>
<span data-ttu-id="95de0-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95de0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95de0-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95de0-114">-LoadBalancer</span></span>
<span data-ttu-id="95de0-115">Der Verweis auf die Lastensaldoressource.</span><span class="sxs-lookup"><span data-stu-id="95de0-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="95de0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="95de0-116">-Name</span></span>
<span data-ttu-id="95de0-117">Name der ausgehenden Regel.</span><span class="sxs-lookup"><span data-stu-id="95de0-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="95de0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95de0-118">CommonParameters</span></span>
<span data-ttu-id="95de0-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95de0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95de0-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95de0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95de0-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95de0-121">INPUTS</span></span>

### <span data-ttu-id="95de0-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95de0-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="95de0-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95de0-123">OUTPUTS</span></span>

### <span data-ttu-id="95de0-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="95de0-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="95de0-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="95de0-125">NOTES</span></span>

## <span data-ttu-id="95de0-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="95de0-126">RELATED LINKS</span></span>

[<span data-ttu-id="95de0-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95de0-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="95de0-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95de0-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="95de0-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95de0-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="95de0-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95de0-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
