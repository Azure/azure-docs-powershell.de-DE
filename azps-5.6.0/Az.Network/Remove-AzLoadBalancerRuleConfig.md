---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 053f86f0b29346c98f60a3160a8e1f2a51ab0e14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941595"
---
# <span data-ttu-id="d457f-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d457f-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="d457f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d457f-102">SYNOPSIS</span></span>
<span data-ttu-id="d457f-103">Entfernt eine Regelkonfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="d457f-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="d457f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d457f-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d457f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d457f-105">DESCRIPTION</span></span>
<span data-ttu-id="d457f-106">Das **Cmdlet Remove-AzLoadBalancerRuleConfig** entfernt eine Regelkonfiguration für einen Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="d457f-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="d457f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d457f-107">EXAMPLES</span></span>

### <span data-ttu-id="d457f-108">Beispiel 1: Entfernen einer Regelkonfiguration aus einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="d457f-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="d457f-109">Der erste Befehl ruft den Load Balancer mit dem Namen MyLoadBalancer ab und speichert ihn dann in $loadbalancer Variablen.</span><span class="sxs-lookup"><span data-stu-id="d457f-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="d457f-110">Mit dem zweiten Befehl wird die Regelkonfiguration mit dem Namen "MyLBruleName" aus dem Load Balancer in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="d457f-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="d457f-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d457f-111">PARAMETERS</span></span>

### <span data-ttu-id="d457f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d457f-112">-DefaultProfile</span></span>
<span data-ttu-id="d457f-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d457f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d457f-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d457f-114">-LoadBalancer</span></span>
<span data-ttu-id="d457f-115">Gibt das **LoadBalancer-Objekt** an, das die Regelkonfiguration enthält, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d457f-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d457f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d457f-116">-Name</span></span>
<span data-ttu-id="d457f-117">Gibt den Namen der Load Balancer-Regelkonfiguration an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d457f-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d457f-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d457f-118">-Confirm</span></span>
<span data-ttu-id="d457f-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d457f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d457f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d457f-120">-WhatIf</span></span>
<span data-ttu-id="d457f-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d457f-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d457f-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d457f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d457f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d457f-123">CommonParameters</span></span>
<span data-ttu-id="d457f-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d457f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d457f-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d457f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d457f-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d457f-126">INPUTS</span></span>

### <span data-ttu-id="d457f-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d457f-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d457f-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d457f-128">OUTPUTS</span></span>

### <span data-ttu-id="d457f-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d457f-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d457f-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d457f-130">NOTES</span></span>

## <span data-ttu-id="d457f-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d457f-131">RELATED LINKS</span></span>

[<span data-ttu-id="d457f-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d457f-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d457f-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d457f-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d457f-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d457f-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d457f-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d457f-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d457f-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d457f-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


