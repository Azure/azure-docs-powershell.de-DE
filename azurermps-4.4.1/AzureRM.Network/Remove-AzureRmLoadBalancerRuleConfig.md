---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 38f6223fdf1dc230dbd34310b7eda2ab45e2d4b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662259"
---
# <span data-ttu-id="26998-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26998-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="26998-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26998-102">SYNOPSIS</span></span>
<span data-ttu-id="26998-103">Entfernt eine Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="26998-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26998-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26998-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26998-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26998-105">DESCRIPTION</span></span>
<span data-ttu-id="26998-106">Das Cmdlet **Remove-AzureRmLoadBalancerRuleConfig** entfernt eine Regelkonfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="26998-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="26998-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26998-107">EXAMPLES</span></span>

### <span data-ttu-id="26998-108">Beispiel 1: Entfernen einer Regelkonfiguration von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="26998-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="26998-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="26998-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="26998-110">Der zweite Befehl entfernt die Regelkonfiguration mit dem Namen MyLBruleName aus dem Lastenausgleichsmodul in $LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="26998-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="26998-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="26998-111">PARAMETERS</span></span>

### <span data-ttu-id="26998-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26998-112">-LoadBalancer</span></span>
<span data-ttu-id="26998-113">Gibt das **LoadBalancer** -Objekt an, das die vom Cmdlet entfernte Regelkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="26998-113">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26998-114">-Name</span><span class="sxs-lookup"><span data-stu-id="26998-114">-Name</span></span>
<span data-ttu-id="26998-115">Gibt den Namen der Load Balancer-Regelkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="26998-115">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="26998-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26998-116">-DefaultProfile</span></span>
<span data-ttu-id="26998-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26998-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26998-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26998-118">CommonParameters</span></span>
<span data-ttu-id="26998-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26998-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26998-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26998-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26998-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26998-121">INPUTS</span></span>

### <span data-ttu-id="26998-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26998-122">PSLoadBalancer</span></span>
<span data-ttu-id="26998-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="26998-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="26998-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26998-124">OUTPUTS</span></span>

### <span data-ttu-id="26998-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26998-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="26998-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="26998-126">NOTES</span></span>

## <span data-ttu-id="26998-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26998-127">RELATED LINKS</span></span>

[<span data-ttu-id="26998-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26998-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="26998-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26998-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="26998-130">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26998-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="26998-131">Neu – AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26998-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="26998-132">Satz-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26998-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


