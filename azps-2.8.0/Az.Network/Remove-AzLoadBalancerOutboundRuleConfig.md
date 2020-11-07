---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: aff2fccde6fc43b9153d8da421f34a6038688fd7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822879"
---
# <span data-ttu-id="fcd8d-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fcd8d-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="fcd8d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fcd8d-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd8d-103">Entfernt eine ausgehende Regelkonfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="fcd8d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcd8d-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcd8d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcd8d-105">DESCRIPTION</span></span>
<span data-ttu-id="fcd8d-106">Das Cmdlet **Remove-AzLoadBalancerOutboundRuleConfig** entfernt eine ausgehende Regelkonfiguration aus einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="fcd8d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fcd8d-107">EXAMPLES</span></span>

### <span data-ttu-id="fcd8d-108">Beispiel 1: Löschen einer ausgehenden Regel aus einem Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="fcd8d-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="fcd8d-109">Der erste Befehl ruft das Load Balancer ab, das der ausgehenden Regelkonfiguration zugeordnet ist, die Sie entfernen möchten, und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="fcd8d-110">Der zweite Befehl entfernt die zugeordnete ausgehende Regelkonfiguration aus dem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="fcd8d-111">Der dritte Befehl aktualisiert das Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="fcd8d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcd8d-112">PARAMETERS</span></span>

### <span data-ttu-id="fcd8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcd8d-113">-DefaultProfile</span></span>
<span data-ttu-id="fcd8d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcd8d-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fcd8d-115">-LoadBalancer</span></span>
<span data-ttu-id="fcd8d-116">Der Verweis der Load Balancer-Ressource.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="fcd8d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fcd8d-117">-Name</span></span>
<span data-ttu-id="fcd8d-118">Der Name der ausgehenden Regel</span><span class="sxs-lookup"><span data-stu-id="fcd8d-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="fcd8d-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fcd8d-119">-Confirm</span></span>
<span data-ttu-id="fcd8d-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcd8d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcd8d-121">-WhatIf</span></span>
<span data-ttu-id="fcd8d-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcd8d-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcd8d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd8d-124">CommonParameters</span></span>
<span data-ttu-id="fcd8d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd8d-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcd8d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd8d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fcd8d-127">INPUTS</span></span>

### <span data-ttu-id="fcd8d-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fcd8d-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fcd8d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fcd8d-129">OUTPUTS</span></span>

### <span data-ttu-id="fcd8d-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fcd8d-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fcd8d-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="fcd8d-131">NOTES</span></span>

## <span data-ttu-id="fcd8d-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fcd8d-132">RELATED LINKS</span></span>

[<span data-ttu-id="fcd8d-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fcd8d-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="fcd8d-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fcd8d-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="fcd8d-135">Neu – AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fcd8d-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="fcd8d-136">Satz-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fcd8d-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
