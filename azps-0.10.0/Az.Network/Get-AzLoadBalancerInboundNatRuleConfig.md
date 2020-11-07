---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6b866dc04975c2cde17509182e21936a2d6c9363
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841616"
---
# <span data-ttu-id="b207e-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b207e-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="b207e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b207e-102">SYNOPSIS</span></span>
<span data-ttu-id="b207e-103">Ruft eine eingehende NAT-Regelkonfiguration für ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="b207e-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="b207e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b207e-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b207e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b207e-105">DESCRIPTION</span></span>
<span data-ttu-id="b207e-106">Das Cmdlet " **Get-AzLoadBalancerInboundNatRuleConfig** " ruft mindestens eine eingehende Netzwerkadressübersetzung (NAT)-Regeln in einem Azure Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="b207e-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="b207e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b207e-107">EXAMPLES</span></span>

### <span data-ttu-id="b207e-108">Beispiel 1: Abrufen einer eingehenden NAT-Regelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="b207e-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="b207e-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="b207e-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="b207e-110">Der zweite Befehl ruft die zugeordnete NAT-Regel namens MyInboundNatRule1 vom Lastenausgleichsmodul in $SLB ab.</span><span class="sxs-lookup"><span data-stu-id="b207e-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="b207e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b207e-111">PARAMETERS</span></span>

### <span data-ttu-id="b207e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b207e-112">-DefaultProfile</span></span>
<span data-ttu-id="b207e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b207e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b207e-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b207e-114">-LoadBalancer</span></span>
<span data-ttu-id="b207e-115">Gibt das Load Balancer an, das der eingehenden NAT-Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b207e-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="b207e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b207e-116">-Name</span></span>
<span data-ttu-id="b207e-117">Gibt den Namen der zu erhaltenden eingehenden NAT-Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="b207e-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="b207e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b207e-118">CommonParameters</span></span>
<span data-ttu-id="b207e-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b207e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b207e-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b207e-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b207e-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b207e-121">INPUTS</span></span>

### <span data-ttu-id="b207e-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b207e-122">PSLoadBalancer</span></span>
<span data-ttu-id="b207e-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b207e-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b207e-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b207e-124">OUTPUTS</span></span>

### <span data-ttu-id="b207e-125">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="b207e-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="b207e-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="b207e-126">NOTES</span></span>

## <span data-ttu-id="b207e-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b207e-127">RELATED LINKS</span></span>

[<span data-ttu-id="b207e-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b207e-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b207e-129">Neu – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b207e-129">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b207e-130">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b207e-130">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b207e-131">Satz-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b207e-131">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


