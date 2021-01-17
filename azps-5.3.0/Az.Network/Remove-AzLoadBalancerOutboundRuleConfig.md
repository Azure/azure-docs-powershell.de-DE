---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 824675d331d37c93e6bcf3bb3d5da0fa8cbde78b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468899"
---
# <span data-ttu-id="2f186-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f186-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="2f186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f186-102">SYNOPSIS</span></span>
<span data-ttu-id="2f186-103">Entfernt eine ausgehende Regelkonfiguration aus einem Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="2f186-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="2f186-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f186-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f186-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f186-105">DESCRIPTION</span></span>
<span data-ttu-id="2f186-106">Das **Cmdlet "Remove-AzLoadBalancerOutboundRuleConfig"** entfernt eine ausgehende Regelkonfiguration aus einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="2f186-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="2f186-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2f186-107">EXAMPLES</span></span>

### <span data-ttu-id="2f186-108">Beispiel 1: Löschen einer ausgehenden Regel aus einem Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="2f186-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="2f186-109">Der erste Befehl ruft den Lastenausgleich ab, der der ausgehenden Regelkonfiguration zugeordnet ist, die Sie entfernen möchten, und speichert ihn dann in der $slb Variable.</span><span class="sxs-lookup"><span data-stu-id="2f186-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="2f186-110">Der zweite Befehl entfernt die zugehörige ausgehende Regelkonfiguration aus dem Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="2f186-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="2f186-111">Der dritte Befehl aktualisiert den Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="2f186-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="2f186-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f186-112">PARAMETERS</span></span>

### <span data-ttu-id="2f186-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f186-113">-DefaultProfile</span></span>
<span data-ttu-id="2f186-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f186-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f186-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f186-115">-LoadBalancer</span></span>
<span data-ttu-id="2f186-116">Der Verweis auf die Lastensaldoressource.</span><span class="sxs-lookup"><span data-stu-id="2f186-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="2f186-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2f186-117">-Name</span></span>
<span data-ttu-id="2f186-118">Der Name der ausgehenden Regel</span><span class="sxs-lookup"><span data-stu-id="2f186-118">The Name of outbound rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f186-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f186-119">-Confirm</span></span>
<span data-ttu-id="2f186-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f186-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f186-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2f186-121">-WhatIf</span></span>
<span data-ttu-id="2f186-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f186-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f186-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f186-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f186-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f186-124">CommonParameters</span></span>
<span data-ttu-id="2f186-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f186-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f186-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f186-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f186-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2f186-127">INPUTS</span></span>

### <span data-ttu-id="2f186-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f186-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2f186-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2f186-129">OUTPUTS</span></span>

### <span data-ttu-id="2f186-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f186-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2f186-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2f186-131">NOTES</span></span>

## <span data-ttu-id="2f186-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2f186-132">RELATED LINKS</span></span>

[<span data-ttu-id="2f186-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f186-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="2f186-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f186-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="2f186-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f186-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="2f186-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f186-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
