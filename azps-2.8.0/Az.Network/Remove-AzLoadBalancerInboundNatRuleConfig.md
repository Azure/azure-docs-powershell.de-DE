---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 2d47a3481772d846a65e3b0bc0d1eb1c62fa5cd5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821363"
---
# <span data-ttu-id="2d2d4-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d2d4-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="2d2d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d2d4-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2d4-103">Entfernt eine eingehende NAT-Regelkonfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="2d2d4-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="2d2d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d2d4-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d2d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d2d4-105">DESCRIPTION</span></span>
<span data-ttu-id="2d2d4-106">Das Cmdlet **Remove-AzLoadBalancerInboundNatRuleConfig** entfernt eine eingehende NAT-Regelkonfiguration (Network Address Translation) aus einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="2d2d4-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="2d2d4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d2d4-107">EXAMPLES</span></span>

### <span data-ttu-id="2d2d4-108">1: Löschen einer eingehenden NAT-Regel aus einem Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="2d2d4-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="2d2d4-109">Der erste Befehl lädt ein bereits vorhandenes Lastenausgleichsmodul mit dem Namen "mylb" und speichert es in der Variablen $Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="2d2d4-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="2d2d4-110">Der zweite Befehl entfernt die eingehende NAT-Regel, die diesem Lastenausgleichsmodul zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2d2d4-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="2d2d4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d2d4-111">PARAMETERS</span></span>

### <span data-ttu-id="2d2d4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d2d4-112">-DefaultProfile</span></span>
<span data-ttu-id="2d2d4-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d2d4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d2d4-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2d2d4-114">-LoadBalancer</span></span>
<span data-ttu-id="2d2d4-115">Gibt das **LoadBalancer** -Objekt an, das die von diesem Cmdlet entfernte eingehende NAT-Regelkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="2d2d4-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2d2d4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2d2d4-116">-Name</span></span>
<span data-ttu-id="2d2d4-117">Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2d2d4-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2d2d4-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d2d4-118">-Confirm</span></span>
<span data-ttu-id="2d2d4-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d2d4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d2d4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d2d4-120">-WhatIf</span></span>
<span data-ttu-id="2d2d4-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d2d4-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d2d4-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d2d4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d2d4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2d4-123">CommonParameters</span></span>
<span data-ttu-id="2d2d4-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d2d4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2d4-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d2d4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2d4-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d2d4-126">INPUTS</span></span>

### <span data-ttu-id="2d2d4-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2d2d4-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2d2d4-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d2d4-128">OUTPUTS</span></span>

### <span data-ttu-id="2d2d4-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2d2d4-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2d2d4-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d2d4-130">NOTES</span></span>

## <span data-ttu-id="2d2d4-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d2d4-131">RELATED LINKS</span></span>

[<span data-ttu-id="2d2d4-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d2d4-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2d2d4-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d2d4-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2d2d4-134">Neu – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d2d4-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2d2d4-135">Satz-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d2d4-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


