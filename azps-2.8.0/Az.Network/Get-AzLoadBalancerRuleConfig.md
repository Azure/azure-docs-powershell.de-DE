---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d2cd1a2f8601cfb0a0a0a58818c1b63c1c41a12c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821808"
---
# <span data-ttu-id="059ac-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="059ac-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="059ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="059ac-102">SYNOPSIS</span></span>
<span data-ttu-id="059ac-103">Ruft die Regelkonfiguration für ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="059ac-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="059ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="059ac-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="059ac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="059ac-105">DESCRIPTION</span></span>
<span data-ttu-id="059ac-106">Das Cmdlet " **Get-AzLoadBalancerRuleConfig** " Ruft eine oder mehrere Regel Konfigurationen für ein Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="059ac-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="059ac-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="059ac-107">EXAMPLES</span></span>

### <span data-ttu-id="059ac-108">Beispiel 1: Abrufen der Regelkonfiguration eines Load Balancer</span><span class="sxs-lookup"><span data-stu-id="059ac-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="059ac-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="059ac-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="059ac-110">Der zweite Befehl ruft die zugeordnete Regelkonfiguration mit dem Namen MyLBrulename vom Lastenausgleichsmodul in $SLB ab.</span><span class="sxs-lookup"><span data-stu-id="059ac-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="059ac-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="059ac-111">PARAMETERS</span></span>

### <span data-ttu-id="059ac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059ac-112">-DefaultProfile</span></span>
<span data-ttu-id="059ac-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="059ac-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="059ac-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="059ac-114">-LoadBalancer</span></span>
<span data-ttu-id="059ac-115">Gibt das Load Balancer an, das der zu erhaltenden Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="059ac-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="059ac-116">-Name</span><span class="sxs-lookup"><span data-stu-id="059ac-116">-Name</span></span>
<span data-ttu-id="059ac-117">Gibt den Namen der Regelkonfiguration an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="059ac-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="059ac-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059ac-118">CommonParameters</span></span>
<span data-ttu-id="059ac-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="059ac-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059ac-120">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="059ac-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059ac-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="059ac-121">INPUTS</span></span>

### <span data-ttu-id="059ac-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="059ac-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="059ac-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="059ac-123">OUTPUTS</span></span>

### <span data-ttu-id="059ac-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="059ac-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="059ac-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="059ac-125">NOTES</span></span>

## <span data-ttu-id="059ac-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="059ac-126">RELATED LINKS</span></span>

[<span data-ttu-id="059ac-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="059ac-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="059ac-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="059ac-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="059ac-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="059ac-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="059ac-130">Satz-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="059ac-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


