---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 17af7cc61ec3d254133dd0563e8ea09fc0e3043f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843643"
---
# <span data-ttu-id="c4753-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c4753-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="c4753-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4753-102">SYNOPSIS</span></span>
<span data-ttu-id="c4753-103">Legt den Zielstatus für ein Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="c4753-103">Sets the goal state for a load balancer.</span></span>

## <span data-ttu-id="c4753-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4753-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4753-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4753-105">DESCRIPTION</span></span>
<span data-ttu-id="c4753-106">Das Cmdlet " **Set-AzLoadBalancer** " legt den Zielstatus für ein Azure Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="c4753-106">The **Set-AzLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="c4753-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4753-107">EXAMPLES</span></span>

### <span data-ttu-id="c4753-108">Beispiel 1: Ändern eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="c4753-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="c4753-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen NRPLB ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c4753-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="c4753-110">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzLoadBalancerInboundNatRuleConfig zu übergeben, wodurch eine eingehende NAT-Regel mit dem Namen "Neuregelung" hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c4753-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="c4753-111">Der dritte Befehl übergibt das Load Balancer an **AzLoadBalancer** , das die Konfiguration des Lastenausgleichsmoduls aktualisiert und speichert.</span><span class="sxs-lookup"><span data-stu-id="c4753-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="c4753-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4753-112">PARAMETERS</span></span>

### <span data-ttu-id="c4753-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4753-113">-AsJob</span></span>
<span data-ttu-id="c4753-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c4753-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4753-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4753-115">-DefaultProfile</span></span>
<span data-ttu-id="c4753-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4753-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4753-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c4753-117">-LoadBalancer</span></span>
<span data-ttu-id="c4753-118">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="c4753-118">Specifies a load balancer.</span></span>
<span data-ttu-id="c4753-119">Mit diesem Cmdlet wird der Zielstatus für das Load Balancer festgelegt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c4753-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4753-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4753-120">CommonParameters</span></span>
<span data-ttu-id="c4753-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4753-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4753-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4753-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4753-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4753-123">INPUTS</span></span>

### <span data-ttu-id="c4753-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c4753-124">PSLoadBalancer</span></span>
<span data-ttu-id="c4753-125">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c4753-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c4753-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4753-126">OUTPUTS</span></span>

### <span data-ttu-id="c4753-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c4753-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c4753-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4753-128">NOTES</span></span>

## <span data-ttu-id="c4753-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4753-129">RELATED LINKS</span></span>

[<span data-ttu-id="c4753-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c4753-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c4753-131">Neu – AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c4753-131">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="c4753-132">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c4753-132">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


