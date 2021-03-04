---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 2cafba2d579a37db45f12c5e3dd1746f799bfe21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921016"
---
# <span data-ttu-id="75f30-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="75f30-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="75f30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75f30-102">SYNOPSIS</span></span>
<span data-ttu-id="75f30-103">Ruft eine Front-End-IP-Konfiguration in einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="75f30-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="75f30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75f30-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75f30-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75f30-105">DESCRIPTION</span></span>
<span data-ttu-id="75f30-106">Das **Get-AzLoadBalancerFrontendIpConfig-Cmdlet** ruft eine Front-End-IP-Konfiguration oder eine Liste der Front-End-IP-Konfigurationen in einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="75f30-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="75f30-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="75f30-107">EXAMPLES</span></span>

### <span data-ttu-id="75f30-108">Beispiel 1: Erhalten einer Front-End-IP-Konfiguration in einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="75f30-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="75f30-109">Der erste Befehl ruft den Load Balancer mit dem Namen MyLoadBalancer ab und speichert ihn dann in der Variablen $slb.</span><span class="sxs-lookup"><span data-stu-id="75f30-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="75f30-110">Der zweite Befehl ruft die front-end-IP-Konfiguration ab, die diesem Load Balancer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="75f30-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="75f30-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="75f30-111">PARAMETERS</span></span>

### <span data-ttu-id="75f30-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f30-112">-DefaultProfile</span></span>
<span data-ttu-id="75f30-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75f30-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75f30-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75f30-114">-LoadBalancer</span></span>
<span data-ttu-id="75f30-115">Gibt den Load Balancer an, der der Front-End-IP-Konfiguration zugeordnet ist, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="75f30-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="75f30-116">-Name</span><span class="sxs-lookup"><span data-stu-id="75f30-116">-Name</span></span>
<span data-ttu-id="75f30-117">Gibt den Namen des Load Balancers an, der die zu erhaltende Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="75f30-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="75f30-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f30-118">CommonParameters</span></span>
<span data-ttu-id="75f30-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f30-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f30-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75f30-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f30-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="75f30-121">INPUTS</span></span>

### <span data-ttu-id="75f30-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75f30-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="75f30-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="75f30-123">OUTPUTS</span></span>

### <span data-ttu-id="75f30-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="75f30-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="75f30-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="75f30-125">NOTES</span></span>

## <span data-ttu-id="75f30-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="75f30-126">RELATED LINKS</span></span>

[<span data-ttu-id="75f30-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="75f30-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="75f30-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75f30-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="75f30-129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="75f30-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="75f30-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="75f30-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="75f30-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="75f30-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


