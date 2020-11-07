---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 9c50452acd832c7ac7ca0c4bc2827b8f320115b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841128"
---
# <span data-ttu-id="15edb-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15edb-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="15edb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15edb-102">SYNOPSIS</span></span>
<span data-ttu-id="15edb-103">Entfernt eine Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="15edb-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="15edb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15edb-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15edb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15edb-105">DESCRIPTION</span></span>
<span data-ttu-id="15edb-106">Das Cmdlet **Remove-AzLoadBalancerRuleConfig** entfernt eine Regelkonfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="15edb-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="15edb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15edb-107">EXAMPLES</span></span>

### <span data-ttu-id="15edb-108">Beispiel 1: Entfernen einer Regelkonfiguration von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="15edb-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="15edb-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="15edb-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="15edb-110">Der zweite Befehl entfernt die Regelkonfiguration mit dem Namen MyLBruleName aus dem Lastenausgleichsmodul in $LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="15edb-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="15edb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="15edb-111">PARAMETERS</span></span>

### <span data-ttu-id="15edb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15edb-112">-DefaultProfile</span></span>
<span data-ttu-id="15edb-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15edb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15edb-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="15edb-114">-LoadBalancer</span></span>
<span data-ttu-id="15edb-115">Gibt das **LoadBalancer** -Objekt an, das die vom Cmdlet entfernte Regelkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="15edb-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="15edb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="15edb-116">-Name</span></span>
<span data-ttu-id="15edb-117">Gibt den Namen der Load Balancer-Regelkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="15edb-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="15edb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15edb-118">CommonParameters</span></span>
<span data-ttu-id="15edb-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15edb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15edb-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15edb-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15edb-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15edb-121">INPUTS</span></span>

### <span data-ttu-id="15edb-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="15edb-122">PSLoadBalancer</span></span>
<span data-ttu-id="15edb-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="15edb-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="15edb-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15edb-124">OUTPUTS</span></span>

### <span data-ttu-id="15edb-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="15edb-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="15edb-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="15edb-126">NOTES</span></span>

## <span data-ttu-id="15edb-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15edb-127">RELATED LINKS</span></span>

[<span data-ttu-id="15edb-128">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15edb-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="15edb-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="15edb-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="15edb-130">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15edb-130">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="15edb-131">Neu – AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15edb-131">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="15edb-132">Satz-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15edb-132">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


