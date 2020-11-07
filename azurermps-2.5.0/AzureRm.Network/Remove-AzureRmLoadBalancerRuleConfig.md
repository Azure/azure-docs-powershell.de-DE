---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: bb0821265f87f959523009a9277dc884498e0e0c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850343"
---
# <span data-ttu-id="16e5e-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16e5e-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="16e5e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="16e5e-103">Entfernt eine Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="16e5e-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16e5e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16e5e-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16e5e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16e5e-105">DESCRIPTION</span></span>
<span data-ttu-id="16e5e-106">Das Cmdlet **Remove-AzureRmLoadBalancerRuleConfig** entfernt eine Regelkonfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="16e5e-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="16e5e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16e5e-107">EXAMPLES</span></span>

### <span data-ttu-id="16e5e-108">Beispiel 1: Entfernen einer Regelkonfiguration von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="16e5e-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="16e5e-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="16e5e-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="16e5e-110">Der zweite Befehl entfernt die Regelkonfiguration mit dem Namen MyLBruleName aus dem Lastenausgleichsmodul in $LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="16e5e-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="16e5e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="16e5e-111">PARAMETERS</span></span>

### <span data-ttu-id="16e5e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e5e-112">-DefaultProfile</span></span>
<span data-ttu-id="16e5e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16e5e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16e5e-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="16e5e-114">-LoadBalancer</span></span>
<span data-ttu-id="16e5e-115">Gibt das **LoadBalancer** -Objekt an, das die vom Cmdlet entfernte Regelkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="16e5e-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="16e5e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="16e5e-116">-Name</span></span>
<span data-ttu-id="16e5e-117">Gibt den Namen der Load Balancer-Regelkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="16e5e-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="16e5e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e5e-118">CommonParameters</span></span>
<span data-ttu-id="16e5e-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e5e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e5e-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e5e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e5e-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16e5e-121">INPUTS</span></span>

### <span data-ttu-id="16e5e-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="16e5e-122">PSLoadBalancer</span></span>
<span data-ttu-id="16e5e-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="16e5e-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="16e5e-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16e5e-124">OUTPUTS</span></span>

### <span data-ttu-id="16e5e-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="16e5e-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="16e5e-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="16e5e-126">NOTES</span></span>

## <span data-ttu-id="16e5e-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16e5e-127">RELATED LINKS</span></span>

[<span data-ttu-id="16e5e-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16e5e-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="16e5e-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="16e5e-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="16e5e-130">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16e5e-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="16e5e-131">Neu – AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16e5e-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="16e5e-132">Satz-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16e5e-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


