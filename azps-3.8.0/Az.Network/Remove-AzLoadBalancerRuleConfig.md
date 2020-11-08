---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ba865b5059e69ae9fb89936a45e432ddff7fb9a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004233"
---
# <span data-ttu-id="a6054-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6054-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="a6054-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6054-102">SYNOPSIS</span></span>
<span data-ttu-id="a6054-103">Entfernt eine Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="a6054-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a6054-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6054-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6054-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6054-105">DESCRIPTION</span></span>
<span data-ttu-id="a6054-106">Das Cmdlet **Remove-AzLoadBalancerRuleConfig** entfernt eine Regelkonfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="a6054-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a6054-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6054-107">EXAMPLES</span></span>

### <span data-ttu-id="a6054-108">Beispiel 1: Entfernen einer Regelkonfiguration von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="a6054-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a6054-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a6054-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="a6054-110">Der zweite Befehl entfernt die Regelkonfiguration mit dem Namen MyLBruleName aus dem Lastenausgleichsmodul in $LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="a6054-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a6054-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6054-111">PARAMETERS</span></span>

### <span data-ttu-id="a6054-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6054-112">-DefaultProfile</span></span>
<span data-ttu-id="a6054-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6054-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6054-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6054-114">-LoadBalancer</span></span>
<span data-ttu-id="a6054-115">Gibt das **LoadBalancer** -Objekt an, das die vom Cmdlet entfernte Regelkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="a6054-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a6054-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a6054-116">-Name</span></span>
<span data-ttu-id="a6054-117">Gibt den Namen der Load Balancer-Regelkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="a6054-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a6054-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6054-118">-Confirm</span></span>
<span data-ttu-id="a6054-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6054-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6054-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6054-120">-WhatIf</span></span>
<span data-ttu-id="a6054-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6054-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6054-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6054-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6054-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6054-123">CommonParameters</span></span>
<span data-ttu-id="a6054-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6054-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6054-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6054-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6054-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6054-126">INPUTS</span></span>

### <span data-ttu-id="a6054-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6054-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a6054-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6054-128">OUTPUTS</span></span>

### <span data-ttu-id="a6054-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6054-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a6054-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6054-130">NOTES</span></span>

## <span data-ttu-id="a6054-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6054-131">RELATED LINKS</span></span>

[<span data-ttu-id="a6054-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6054-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a6054-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6054-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a6054-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6054-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a6054-135">Neu – AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6054-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a6054-136">Satz-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6054-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


