---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: 463b9cf07bbb04273e1653f4d84805de3802b616
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481125"
---
# <span data-ttu-id="59f80-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59f80-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="59f80-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59f80-102">SYNOPSIS</span></span>
<span data-ttu-id="59f80-103">Legt den Zielstatus für ein Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="59f80-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59f80-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59f80-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59f80-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59f80-105">DESCRIPTION</span></span>
<span data-ttu-id="59f80-106">Das Cmdlet " **Set-AzureRmLoadBalancer** " legt den Zielstatus für ein Azure Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="59f80-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="59f80-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59f80-107">EXAMPLES</span></span>

### <span data-ttu-id="59f80-108">Beispiel 1: Ändern eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="59f80-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="59f80-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen NRPLB ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="59f80-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="59f80-110">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzureRmLoadBalancerInboundNatRuleConfig zu übergeben, wodurch eine eingehende NAT-Regel mit dem Namen "Neuregelung" hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="59f80-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="59f80-111">Der dritte Befehl übergibt das Load Balancer an **AzureRmLoadBalancer** , das die Konfiguration des Lastenausgleichsmoduls aktualisiert und speichert.</span><span class="sxs-lookup"><span data-stu-id="59f80-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="59f80-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="59f80-112">PARAMETERS</span></span>

### <span data-ttu-id="59f80-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59f80-113">-AsJob</span></span>
<span data-ttu-id="59f80-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="59f80-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59f80-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f80-115">-DefaultProfile</span></span>
<span data-ttu-id="59f80-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59f80-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59f80-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59f80-117">-LoadBalancer</span></span>
<span data-ttu-id="59f80-118">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="59f80-118">Specifies a load balancer.</span></span>
<span data-ttu-id="59f80-119">Mit diesem Cmdlet wird der Zielstatus für das Load Balancer festgelegt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="59f80-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="59f80-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f80-120">CommonParameters</span></span>
<span data-ttu-id="59f80-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59f80-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f80-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f80-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f80-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59f80-123">INPUTS</span></span>

### <span data-ttu-id="59f80-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59f80-124">PSLoadBalancer</span></span>
<span data-ttu-id="59f80-125">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="59f80-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="59f80-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59f80-126">OUTPUTS</span></span>

### <span data-ttu-id="59f80-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59f80-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="59f80-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="59f80-128">NOTES</span></span>

## <span data-ttu-id="59f80-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59f80-129">RELATED LINKS</span></span>

[<span data-ttu-id="59f80-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59f80-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="59f80-131">Neu – AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59f80-131">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="59f80-132">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59f80-132">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


