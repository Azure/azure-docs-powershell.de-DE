---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 5652615cf8072e4a448f2fe6c6d4b3fd784cc330
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941603"
---
# <span data-ttu-id="99f3a-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99f3a-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="99f3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="99f3a-103">Entfernt eine ausgehende Regelkonfiguration aus einem Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="99f3a-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="99f3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99f3a-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99f3a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="99f3a-106">Das **Cmdlet Remove-AzLoadBalancerOutboundRuleConfig** entfernt eine ausgehende Regelkonfiguration aus einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="99f3a-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="99f3a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99f3a-107">EXAMPLES</span></span>

### <span data-ttu-id="99f3a-108">Beispiel 1: Löschen einer ausgehenden Regel aus einem Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="99f3a-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="99f3a-109">Der erste Befehl ruft den Load Balancer ab, der der ausgehenden Regelkonfiguration zugeordnet ist, die Sie entfernen möchten, und speichert ihn dann in der $slb Variablen.</span><span class="sxs-lookup"><span data-stu-id="99f3a-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="99f3a-110">Mit dem zweiten Befehl wird die zugeordnete ausgehende Regelkonfiguration aus dem Load Balancer entfernt.</span><span class="sxs-lookup"><span data-stu-id="99f3a-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="99f3a-111">Der dritte Befehl aktualisiert den Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="99f3a-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="99f3a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="99f3a-112">PARAMETERS</span></span>

### <span data-ttu-id="99f3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f3a-113">-DefaultProfile</span></span>
<span data-ttu-id="99f3a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99f3a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99f3a-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99f3a-115">-LoadBalancer</span></span>
<span data-ttu-id="99f3a-116">Der Verweis auf die Load Balancer-Ressource.</span><span class="sxs-lookup"><span data-stu-id="99f3a-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="99f3a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="99f3a-117">-Name</span></span>
<span data-ttu-id="99f3a-118">Der Name der ausgehenden Regel</span><span class="sxs-lookup"><span data-stu-id="99f3a-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="99f3a-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="99f3a-119">-Confirm</span></span>
<span data-ttu-id="99f3a-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="99f3a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99f3a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f3a-121">-WhatIf</span></span>
<span data-ttu-id="99f3a-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99f3a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99f3a-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99f3a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99f3a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f3a-124">CommonParameters</span></span>
<span data-ttu-id="99f3a-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f3a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f3a-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f3a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f3a-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99f3a-127">INPUTS</span></span>

### <span data-ttu-id="99f3a-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99f3a-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="99f3a-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99f3a-129">OUTPUTS</span></span>

### <span data-ttu-id="99f3a-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99f3a-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="99f3a-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="99f3a-131">NOTES</span></span>

## <span data-ttu-id="99f3a-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="99f3a-132">RELATED LINKS</span></span>

[<span data-ttu-id="99f3a-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99f3a-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="99f3a-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99f3a-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="99f3a-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99f3a-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="99f3a-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99f3a-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
