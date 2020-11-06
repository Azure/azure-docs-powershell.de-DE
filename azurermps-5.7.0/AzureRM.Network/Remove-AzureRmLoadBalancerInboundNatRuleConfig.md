---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6dcd7c51a43387139de85a3a9f0c17c0b19cfe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497533"
---
# <span data-ttu-id="60964-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60964-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="60964-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60964-102">SYNOPSIS</span></span>
<span data-ttu-id="60964-103">Entfernt eine eingehende NAT-Regelkonfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="60964-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60964-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60964-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60964-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60964-105">DESCRIPTION</span></span>
<span data-ttu-id="60964-106">Das Cmdlet **Remove-AzureRmLoadBalancerInboundNatRuleConfig** entfernt eine eingehende NAT-Regelkonfiguration (Network Address Translation) aus einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="60964-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="60964-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60964-107">EXAMPLES</span></span>

### <span data-ttu-id="60964-108">1: Löschen einer eingehenden NAT-Regel aus einem Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="60964-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="60964-109">Der erste Befehl lädt ein bereits vorhandenes Lastenausgleichsmodul mit dem Namen "mylb" und speichert es in der Variablen $Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="60964-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="60964-110">Der zweite Befehl entfernt die eingehende NAT-Regel, die diesem Lastenausgleichsmodul zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="60964-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="60964-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="60964-111">PARAMETERS</span></span>

### <span data-ttu-id="60964-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60964-112">-DefaultProfile</span></span>
<span data-ttu-id="60964-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60964-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60964-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="60964-114">-LoadBalancer</span></span>
<span data-ttu-id="60964-115">Gibt das **LoadBalancer** -Objekt an, das die von diesem Cmdlet entfernte eingehende NAT-Regelkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="60964-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="60964-116">-Name</span><span class="sxs-lookup"><span data-stu-id="60964-116">-Name</span></span>
<span data-ttu-id="60964-117">Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="60964-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="60964-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60964-118">CommonParameters</span></span>
<span data-ttu-id="60964-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60964-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60964-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60964-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60964-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60964-121">INPUTS</span></span>

### <span data-ttu-id="60964-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="60964-122">PSLoadBalancer</span></span>
<span data-ttu-id="60964-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="60964-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="60964-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60964-124">OUTPUTS</span></span>

### <span data-ttu-id="60964-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="60964-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="60964-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="60964-126">NOTES</span></span>

## <span data-ttu-id="60964-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60964-127">RELATED LINKS</span></span>

[<span data-ttu-id="60964-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60964-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="60964-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60964-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="60964-130">Neu – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60964-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="60964-131">Satz-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60964-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


