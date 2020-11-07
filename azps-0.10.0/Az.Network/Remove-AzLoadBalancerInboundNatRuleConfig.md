---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: b135f9a54c084eb7bc5dc4562e16c67e316f8736
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841143"
---
# <span data-ttu-id="7327c-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7327c-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="7327c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7327c-102">SYNOPSIS</span></span>
<span data-ttu-id="7327c-103">Entfernt eine eingehende NAT-Regelkonfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="7327c-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="7327c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7327c-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7327c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7327c-105">DESCRIPTION</span></span>
<span data-ttu-id="7327c-106">Das Cmdlet **Remove-AzLoadBalancerInboundNatRuleConfig** entfernt eine eingehende NAT-Regelkonfiguration (Network Address Translation) aus einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="7327c-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="7327c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7327c-107">EXAMPLES</span></span>

### <span data-ttu-id="7327c-108">1: Löschen einer eingehenden NAT-Regel aus einem Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="7327c-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="7327c-109">Der erste Befehl lädt ein bereits vorhandenes Lastenausgleichsmodul mit dem Namen "mylb" und speichert es in der Variablen $Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="7327c-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="7327c-110">Der zweite Befehl entfernt die eingehende NAT-Regel, die diesem Lastenausgleichsmodul zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7327c-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="7327c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7327c-111">PARAMETERS</span></span>

### <span data-ttu-id="7327c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7327c-112">-DefaultProfile</span></span>
<span data-ttu-id="7327c-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7327c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7327c-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7327c-114">-LoadBalancer</span></span>
<span data-ttu-id="7327c-115">Gibt das **LoadBalancer** -Objekt an, das die von diesem Cmdlet entfernte eingehende NAT-Regelkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="7327c-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7327c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7327c-116">-Name</span></span>
<span data-ttu-id="7327c-117">Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7327c-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7327c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7327c-118">CommonParameters</span></span>
<span data-ttu-id="7327c-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7327c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7327c-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7327c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7327c-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7327c-121">INPUTS</span></span>

### <span data-ttu-id="7327c-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7327c-122">PSLoadBalancer</span></span>
<span data-ttu-id="7327c-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7327c-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7327c-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7327c-124">OUTPUTS</span></span>

### <span data-ttu-id="7327c-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7327c-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7327c-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="7327c-126">NOTES</span></span>

## <span data-ttu-id="7327c-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7327c-127">RELATED LINKS</span></span>

[<span data-ttu-id="7327c-128">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7327c-128">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7327c-129">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7327c-129">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7327c-130">Neu – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7327c-130">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7327c-131">Satz-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7327c-131">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


