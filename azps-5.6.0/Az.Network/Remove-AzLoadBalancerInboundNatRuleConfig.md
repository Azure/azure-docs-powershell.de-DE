---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: b32f36e55df3c00ee7539c082f863be563b874b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941600"
---
# <span data-ttu-id="d5ae8-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d5ae8-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="d5ae8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ae8-103">Entfernt eine eingehende NAT-Regelkonfiguration aus einem Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="d5ae8-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="d5ae8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5ae8-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5ae8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5ae8-105">DESCRIPTION</span></span>
<span data-ttu-id="d5ae8-106">Das **Cmdlet Remove-AzLoadBalancerInboundNatRuleConfig** entfernt eine Nat-Regelkonfiguration (Inbound Network Address Translation) aus einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="d5ae8-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="d5ae8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5ae8-107">EXAMPLES</span></span>

### <span data-ttu-id="d5ae8-108">1: Löschen einer eingehenden NAT-Regel aus einem Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="d5ae8-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="d5ae8-109">Der erste Befehl lädt einen bereits vorhandenen Load Balancer mit dem Namen "mylb" und speichert ihn in der variablen $load Balancer.</span><span class="sxs-lookup"><span data-stu-id="d5ae8-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="d5ae8-110">Mit dem zweiten Befehl wird die eingehende NAT-Regel entfernt, die diesem Lastenausgleich zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d5ae8-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="d5ae8-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d5ae8-111">PARAMETERS</span></span>

### <span data-ttu-id="d5ae8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ae8-112">-DefaultProfile</span></span>
<span data-ttu-id="d5ae8-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5ae8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5ae8-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d5ae8-114">-LoadBalancer</span></span>
<span data-ttu-id="d5ae8-115">Gibt das **LoadBalancer-Objekt** an, das die eingehende NAT-Regelkonfiguration enthält, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d5ae8-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d5ae8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d5ae8-116">-Name</span></span>
<span data-ttu-id="d5ae8-117">Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d5ae8-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d5ae8-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5ae8-118">-Confirm</span></span>
<span data-ttu-id="d5ae8-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5ae8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5ae8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5ae8-120">-WhatIf</span></span>
<span data-ttu-id="d5ae8-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5ae8-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5ae8-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5ae8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5ae8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ae8-123">CommonParameters</span></span>
<span data-ttu-id="d5ae8-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5ae8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ae8-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5ae8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ae8-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5ae8-126">INPUTS</span></span>

### <span data-ttu-id="d5ae8-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d5ae8-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d5ae8-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5ae8-128">OUTPUTS</span></span>

### <span data-ttu-id="d5ae8-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d5ae8-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d5ae8-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d5ae8-130">NOTES</span></span>

## <span data-ttu-id="d5ae8-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d5ae8-131">RELATED LINKS</span></span>

[<span data-ttu-id="d5ae8-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d5ae8-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d5ae8-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d5ae8-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d5ae8-134">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d5ae8-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d5ae8-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d5ae8-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


