---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1bcaab526ac2fbb82d696db7197bbc8d69c0078f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665306"
---
# <span data-ttu-id="c8399-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8399-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="c8399-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8399-102">SYNOPSIS</span></span>
<span data-ttu-id="c8399-103">Ruft eine ausgehende Regelkonfiguration in einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="c8399-103">Gets an outbound rule configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8399-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8399-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8399-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8399-105">DESCRIPTION</span></span>
<span data-ttu-id="c8399-106">Das Cmdlet " **Get-AzureRmLoadBalancerOutboundRuleConfig** " Ruft eine ausgehende Regelkonfiguration oder eine Liste von ausgehenden Regel Konfigurationen in einem Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="c8399-106">The **Get-AzureRmLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="c8399-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8399-107">EXAMPLES</span></span>

### <span data-ttu-id="c8399-108">Beispiel 1: Abrufen einer ausgehenden Regelkonfiguration in einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="c8399-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="c8399-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="c8399-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="c8399-110">Der zweite Befehl ruft die ausgehende Regelkonfiguration mit dem Namen "myrule" ab, die diesem Lastenausgleichsmodul zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c8399-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="c8399-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8399-111">PARAMETERS</span></span>

### <span data-ttu-id="c8399-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8399-112">-DefaultProfile</span></span>
<span data-ttu-id="c8399-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8399-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8399-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c8399-114">-LoadBalancer</span></span>
<span data-ttu-id="c8399-115">Der Verweis der Load Balancer-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c8399-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="c8399-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c8399-116">-Name</span></span>
<span data-ttu-id="c8399-117">Der Name der ausgehenden Regel.</span><span class="sxs-lookup"><span data-stu-id="c8399-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="c8399-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8399-118">CommonParameters</span></span>
<span data-ttu-id="c8399-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8399-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8399-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8399-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8399-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8399-121">INPUTS</span></span>

### <span data-ttu-id="c8399-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c8399-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c8399-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8399-123">OUTPUTS</span></span>

### <span data-ttu-id="c8399-124">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="c8399-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="c8399-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8399-125">NOTES</span></span>

## <span data-ttu-id="c8399-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8399-126">RELATED LINKS</span></span>
