---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: 2af05b60498fc83b74c00701794dba7f1b59e6a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850635"
---
# <span data-ttu-id="4014e-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4014e-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="4014e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4014e-102">SYNOPSIS</span></span>
<span data-ttu-id="4014e-103">Entfernt eine eingehende NAT-Regelkonfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="4014e-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4014e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4014e-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4014e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4014e-105">DESCRIPTION</span></span>
<span data-ttu-id="4014e-106">Das Cmdlet **Remove-AzureRmLoadBalancerInboundNatRuleConfig** entfernt eine eingehende NAT-Regelkonfiguration (Network Address Translation) aus einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="4014e-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="4014e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4014e-107">EXAMPLES</span></span>

### <span data-ttu-id="4014e-108">1: Löschen einer eingehenden NAT-Regel aus einem Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="4014e-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="4014e-109">Der erste Befehl lädt ein bereits vorhandenes Lastenausgleichsmodul mit dem Namen "mylb" und speichert es in der Variablen $Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="4014e-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="4014e-110">Der zweite Befehl entfernt die eingehende NAT-Regel, die diesem Lastenausgleichsmodul zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4014e-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="4014e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4014e-111">PARAMETERS</span></span>

### <span data-ttu-id="4014e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4014e-112">-DefaultProfile</span></span>
<span data-ttu-id="4014e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4014e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4014e-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4014e-114">-LoadBalancer</span></span>
<span data-ttu-id="4014e-115">Gibt das **LoadBalancer** -Objekt an, das die von diesem Cmdlet entfernte eingehende NAT-Regelkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="4014e-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4014e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4014e-116">-Name</span></span>
<span data-ttu-id="4014e-117">Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4014e-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4014e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4014e-118">CommonParameters</span></span>
<span data-ttu-id="4014e-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4014e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4014e-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4014e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4014e-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4014e-121">INPUTS</span></span>

### <span data-ttu-id="4014e-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4014e-122">PSLoadBalancer</span></span>
<span data-ttu-id="4014e-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4014e-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4014e-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4014e-124">OUTPUTS</span></span>

### <span data-ttu-id="4014e-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4014e-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4014e-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="4014e-126">NOTES</span></span>

## <span data-ttu-id="4014e-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4014e-127">RELATED LINKS</span></span>

[<span data-ttu-id="4014e-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4014e-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4014e-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4014e-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4014e-130">Neu – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4014e-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4014e-131">Satz-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4014e-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


