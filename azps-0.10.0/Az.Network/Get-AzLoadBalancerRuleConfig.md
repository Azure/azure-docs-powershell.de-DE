---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: a5d21e5a34727d0bc13730503d55be6ef604a245
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841608"
---
# <span data-ttu-id="39ea0-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39ea0-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="39ea0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39ea0-102">SYNOPSIS</span></span>
<span data-ttu-id="39ea0-103">Ruft die Regelkonfiguration für ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="39ea0-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="39ea0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39ea0-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39ea0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39ea0-105">DESCRIPTION</span></span>
<span data-ttu-id="39ea0-106">Das Cmdlet " **Get-AzLoadBalancerRuleConfig** " Ruft eine oder mehrere Regel Konfigurationen für ein Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="39ea0-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="39ea0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39ea0-107">EXAMPLES</span></span>

### <span data-ttu-id="39ea0-108">Beispiel 1: Abrufen der Regelkonfiguration eines Load Balancer</span><span class="sxs-lookup"><span data-stu-id="39ea0-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="39ea0-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="39ea0-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="39ea0-110">Der zweite Befehl ruft die zugeordnete Regelkonfiguration mit dem Namen MyLBrulename vom Lastenausgleichsmodul in $SLB ab.</span><span class="sxs-lookup"><span data-stu-id="39ea0-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="39ea0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="39ea0-111">PARAMETERS</span></span>

### <span data-ttu-id="39ea0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ea0-112">-DefaultProfile</span></span>
<span data-ttu-id="39ea0-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39ea0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39ea0-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39ea0-114">-LoadBalancer</span></span>
<span data-ttu-id="39ea0-115">Gibt das Load Balancer an, das der zu erhaltenden Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="39ea0-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="39ea0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="39ea0-116">-Name</span></span>
<span data-ttu-id="39ea0-117">Gibt den Namen der Regelkonfiguration an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="39ea0-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="39ea0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ea0-118">CommonParameters</span></span>
<span data-ttu-id="39ea0-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39ea0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ea0-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39ea0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ea0-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39ea0-121">INPUTS</span></span>

### <span data-ttu-id="39ea0-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39ea0-122">PSLoadBalancer</span></span>
<span data-ttu-id="39ea0-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="39ea0-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="39ea0-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39ea0-124">OUTPUTS</span></span>

### <span data-ttu-id="39ea0-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="39ea0-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="39ea0-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="39ea0-126">NOTES</span></span>

## <span data-ttu-id="39ea0-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39ea0-127">RELATED LINKS</span></span>

[<span data-ttu-id="39ea0-128">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39ea0-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="39ea0-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39ea0-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="39ea0-130">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39ea0-130">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="39ea0-131">Satz-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39ea0-131">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


