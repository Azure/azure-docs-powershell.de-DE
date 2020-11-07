---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 32e22416a6e624af293ffcc0597203d8b24351a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660756"
---
# <span data-ttu-id="ef548-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef548-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="ef548-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef548-102">SYNOPSIS</span></span>
<span data-ttu-id="ef548-103">Ruft eine ausgehende Regelkonfiguration in einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="ef548-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="ef548-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef548-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef548-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef548-105">DESCRIPTION</span></span>
<span data-ttu-id="ef548-106">Das Cmdlet " **Get-AzLoadBalancerOutboundRuleConfig** " Ruft eine ausgehende Regelkonfiguration oder eine Liste von ausgehenden Regel Konfigurationen in einem Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="ef548-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="ef548-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef548-107">EXAMPLES</span></span>

### <span data-ttu-id="ef548-108">Beispiel 1: Abrufen einer ausgehenden Regelkonfiguration in einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="ef548-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="ef548-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="ef548-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="ef548-110">Der zweite Befehl ruft die ausgehende Regelkonfiguration mit dem Namen "myrule" ab, die diesem Lastenausgleichsmodul zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ef548-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="ef548-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef548-111">PARAMETERS</span></span>

### <span data-ttu-id="ef548-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef548-112">-DefaultProfile</span></span>
<span data-ttu-id="ef548-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef548-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef548-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ef548-114">-LoadBalancer</span></span>
<span data-ttu-id="ef548-115">Der Verweis der Load Balancer-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ef548-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="ef548-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ef548-116">-Name</span></span>
<span data-ttu-id="ef548-117">Der Name der ausgehenden Regel.</span><span class="sxs-lookup"><span data-stu-id="ef548-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="ef548-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef548-118">CommonParameters</span></span>
<span data-ttu-id="ef548-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef548-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef548-120">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef548-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef548-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef548-121">INPUTS</span></span>

### <span data-ttu-id="ef548-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ef548-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ef548-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef548-123">OUTPUTS</span></span>

### <span data-ttu-id="ef548-124">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="ef548-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="ef548-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef548-125">NOTES</span></span>

## <span data-ttu-id="ef548-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef548-126">RELATED LINKS</span></span>

[<span data-ttu-id="ef548-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef548-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="ef548-128">Neu – AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef548-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="ef548-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef548-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="ef548-130">Satz-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef548-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
