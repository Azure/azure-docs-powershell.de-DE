---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: d16e0579224907885a2239aa0669ae865ed19dd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822724"
---
# <span data-ttu-id="f5127-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5127-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="f5127-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5127-102">SYNOPSIS</span></span>
<span data-ttu-id="f5127-103">Aktualisiert ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="f5127-103">Updates a load balancer.</span></span>

## <span data-ttu-id="f5127-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5127-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5127-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5127-105">DESCRIPTION</span></span>
<span data-ttu-id="f5127-106">Das Cmdlet " **Satz-AzLoadBalancer** " aktualisiert ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="f5127-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="f5127-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5127-107">EXAMPLES</span></span>

### <span data-ttu-id="f5127-108">Beispiel 1: Ändern eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="f5127-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="f5127-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen NRPLB ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f5127-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="f5127-110">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzLoadBalancerInboundNatRuleConfig zu übergeben, wodurch eine eingehende NAT-Regel mit dem Namen "Neuregelung" hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f5127-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="f5127-111">Der dritte Befehl übergibt das Load Balancer an **AzLoadBalancer** , das die Konfiguration des Lastenausgleichsmoduls aktualisiert und speichert.</span><span class="sxs-lookup"><span data-stu-id="f5127-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="f5127-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5127-112">PARAMETERS</span></span>

### <span data-ttu-id="f5127-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5127-113">-AsJob</span></span>
<span data-ttu-id="f5127-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f5127-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5127-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5127-115">-DefaultProfile</span></span>
<span data-ttu-id="f5127-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5127-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5127-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5127-117">-LoadBalancer</span></span>
<span data-ttu-id="f5127-118">Gibt ein Load Balancer-Objekt an, das den Zustand darstellt, in dem das Load Balancer festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5127-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

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

### <span data-ttu-id="f5127-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5127-119">-Confirm</span></span>
<span data-ttu-id="f5127-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5127-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5127-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5127-121">-WhatIf</span></span>
<span data-ttu-id="f5127-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5127-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5127-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5127-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5127-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5127-124">CommonParameters</span></span>
<span data-ttu-id="f5127-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5127-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5127-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5127-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5127-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5127-127">INPUTS</span></span>

### <span data-ttu-id="f5127-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5127-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f5127-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5127-129">OUTPUTS</span></span>

### <span data-ttu-id="f5127-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5127-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f5127-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5127-131">NOTES</span></span>

## <span data-ttu-id="f5127-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5127-132">RELATED LINKS</span></span>

[<span data-ttu-id="f5127-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5127-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f5127-134">Neu – AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5127-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="f5127-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5127-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


