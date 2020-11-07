---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: fbfa70146a5eb70d118e6cd1859f968c576d8a0f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850728"
---
# <span data-ttu-id="ee177-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ee177-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="ee177-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee177-102">SYNOPSIS</span></span>
<span data-ttu-id="ee177-103">Ruft eine eingehende NAT-Regelkonfiguration für ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="ee177-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee177-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee177-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee177-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee177-105">DESCRIPTION</span></span>
<span data-ttu-id="ee177-106">Das Cmdlet " **Get-AzureRmLoadBalancerInboundNatRuleConfig** " ruft mindestens eine eingehende Netzwerkadressübersetzung (NAT)-Regeln in einem Azure Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="ee177-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="ee177-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee177-107">EXAMPLES</span></span>

### <span data-ttu-id="ee177-108">Beispiel 1: Abrufen einer eingehenden NAT-Regelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ee177-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="ee177-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="ee177-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="ee177-110">Der zweite Befehl ruft die zugeordnete NAT-Regel namens MyInboundNatRule1 vom Lastenausgleichsmodul in $SLB ab.</span><span class="sxs-lookup"><span data-stu-id="ee177-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="ee177-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee177-111">PARAMETERS</span></span>

### <span data-ttu-id="ee177-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee177-112">-DefaultProfile</span></span>
<span data-ttu-id="ee177-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ee177-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee177-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ee177-114">-LoadBalancer</span></span>
<span data-ttu-id="ee177-115">Gibt das Load Balancer an, das der eingehenden NAT-Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ee177-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="ee177-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ee177-116">-Name</span></span>
<span data-ttu-id="ee177-117">Gibt den Namen der zu erhaltenden eingehenden NAT-Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="ee177-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee177-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee177-118">CommonParameters</span></span>
<span data-ttu-id="ee177-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee177-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee177-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee177-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee177-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee177-121">INPUTS</span></span>

### <span data-ttu-id="ee177-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ee177-122">PSLoadBalancer</span></span>
<span data-ttu-id="ee177-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ee177-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ee177-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee177-124">OUTPUTS</span></span>

### <span data-ttu-id="ee177-125">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="ee177-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="ee177-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee177-126">NOTES</span></span>

## <span data-ttu-id="ee177-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee177-127">RELATED LINKS</span></span>

[<span data-ttu-id="ee177-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ee177-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="ee177-129">Neu – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ee177-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ee177-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ee177-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ee177-131">Satz-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ee177-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


