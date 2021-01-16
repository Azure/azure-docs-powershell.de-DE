---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 049b99ee0d019ae7f845e5e7578d9982e41a7a4b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367365"
---
# <span data-ttu-id="4db5d-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4db5d-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="4db5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4db5d-102">SYNOPSIS</span></span>
<span data-ttu-id="4db5d-103">Aktualisiert einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="4db5d-103">Updates a load balancer.</span></span>

## <span data-ttu-id="4db5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4db5d-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4db5d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4db5d-105">DESCRIPTION</span></span>
<span data-ttu-id="4db5d-106">Das **Cmdlet Set-AzLoadBalancer** aktualisiert einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="4db5d-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="4db5d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4db5d-107">EXAMPLES</span></span>

### <span data-ttu-id="4db5d-108">Beispiel 1: Ändern eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="4db5d-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="4db5d-109">Der erste Befehl ruft den Lastenausgleich namens NRPLB ab und speichert ihn dann in der $slb Variable.</span><span class="sxs-lookup"><span data-stu-id="4db5d-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="4db5d-110">Der zweite Befehl verwendet den Pipelineoperator, um den Lastenausgleich in $slb an Add-AzLoadBalancerInboundNatRuleConfig zu übergeben, wodurch eine eingehende NAT-Regel namens "NewRule" hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="4db5d-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="4db5d-111">Der dritte Befehl übergibt den Lastenausgleich an **Set-AzLoadBalancer, wodurch** die Lastenausgleichskonfiguration aktualisiert und gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="4db5d-111">The third command passes the load balancer to **Set-AzLoadBalancer**, which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="4db5d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4db5d-112">PARAMETERS</span></span>

### <span data-ttu-id="4db5d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4db5d-113">-AsJob</span></span>
<span data-ttu-id="4db5d-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4db5d-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db5d-115">-DefaultProfile</span></span>
<span data-ttu-id="4db5d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4db5d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4db5d-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4db5d-117">-LoadBalancer</span></span>
<span data-ttu-id="4db5d-118">Gibt ein Lastenausgleichsobjekt an, das den Zustand darstellt, auf den der Lastenausgleich festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4db5d-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4db5d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4db5d-119">-Confirm</span></span>
<span data-ttu-id="4db5d-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4db5d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4db5d-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4db5d-121">-WhatIf</span></span>
<span data-ttu-id="4db5d-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4db5d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4db5d-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4db5d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4db5d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db5d-124">CommonParameters</span></span>
<span data-ttu-id="4db5d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4db5d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db5d-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4db5d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db5d-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4db5d-127">INPUTS</span></span>

### <span data-ttu-id="4db5d-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4db5d-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4db5d-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4db5d-129">OUTPUTS</span></span>

### <span data-ttu-id="4db5d-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4db5d-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4db5d-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4db5d-131">NOTES</span></span>

## <span data-ttu-id="4db5d-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4db5d-132">RELATED LINKS</span></span>

[<span data-ttu-id="4db5d-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4db5d-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4db5d-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4db5d-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="4db5d-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4db5d-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


