---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 3a11b6435c263b5460258a63adb9b72d7ac9f02c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505474"
---
# <span data-ttu-id="0ff7b-101">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff7b-101">Get-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="0ff7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ff7b-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff7b-103">Ruft die Regelkonfiguration für ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-103">Gets the rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ff7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ff7b-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ff7b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ff7b-105">DESCRIPTION</span></span>
<span data-ttu-id="0ff7b-106">Das Cmdlet " **Get-AzureRmLoadBalancerRuleConfig** " Ruft eine oder mehrere Regel Konfigurationen für ein Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-106">The **Get-AzureRmLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="0ff7b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ff7b-107">EXAMPLES</span></span>

### <span data-ttu-id="0ff7b-108">Beispiel 1: Abrufen der Regelkonfiguration eines Load Balancer</span><span class="sxs-lookup"><span data-stu-id="0ff7b-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="0ff7b-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="0ff7b-110">Der zweite Befehl ruft die zugeordnete Regelkonfiguration mit dem Namen MyLBrulename vom Lastenausgleichsmodul in $SLB ab.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="0ff7b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ff7b-111">PARAMETERS</span></span>

### <span data-ttu-id="0ff7b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff7b-112">-DefaultProfile</span></span>
<span data-ttu-id="0ff7b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ff7b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0ff7b-114">-LoadBalancer</span></span>
<span data-ttu-id="0ff7b-115">Gibt das Load Balancer an, das der zu erhaltenden Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="0ff7b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0ff7b-116">-Name</span></span>
<span data-ttu-id="0ff7b-117">Gibt den Namen der Regelkonfiguration an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="0ff7b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff7b-118">CommonParameters</span></span>
<span data-ttu-id="0ff7b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff7b-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ff7b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff7b-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ff7b-121">INPUTS</span></span>

### <span data-ttu-id="0ff7b-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0ff7b-122">PSLoadBalancer</span></span>
<span data-ttu-id="0ff7b-123">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="0ff7b-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ff7b-124">OUTPUTS</span></span>

### <span data-ttu-id="0ff7b-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="0ff7b-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="0ff7b-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ff7b-126">NOTES</span></span>

## <span data-ttu-id="0ff7b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ff7b-127">RELATED LINKS</span></span>

[<span data-ttu-id="0ff7b-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff7b-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="0ff7b-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0ff7b-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="0ff7b-130">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff7b-130">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="0ff7b-131">Satz-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff7b-131">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


