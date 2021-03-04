---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: a337446238807f3a6408d0c9b68034e4a245eb48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921019"
---
# <span data-ttu-id="9dd3b-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9dd3b-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="9dd3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dd3b-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd3b-103">Ruft eine Back-End-Adresspoolkonfiguration für einen Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="9dd3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9dd3b-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dd3b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9dd3b-105">DESCRIPTION</span></span>
<span data-ttu-id="9dd3b-106">Das **Get-AzLoadBalancerBackendAddressPoolConfig-Cmdlet** ruft einen einzelnen Back-End-Adresspool oder eine Liste der Back-End-Adresspools in einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="9dd3b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9dd3b-107">EXAMPLES</span></span>

### <span data-ttu-id="9dd3b-108">Beispiel 1: Erhalten des Back-End-Adresspools</span><span class="sxs-lookup"><span data-stu-id="9dd3b-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="9dd3b-109">Der erste Befehl ruft einen vorhandenen Load Balancer mit dem Namen MyLoadBalancer in der Ressourcengruppe mit dem Namen MyResourceGroup ab und speichert ihn dann in der $loadbalancer Variablen.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="9dd3b-110">Der zweite Befehl ruft die zugeordnete Back-End-Adresspoolkonfiguration mit dem Namen Back-EndAddressPool02 für den Load Balancer in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="9dd3b-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9dd3b-111">PARAMETERS</span></span>

### <span data-ttu-id="9dd3b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd3b-112">-DefaultProfile</span></span>
<span data-ttu-id="9dd3b-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dd3b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9dd3b-114">-LoadBalancer</span></span>
<span data-ttu-id="9dd3b-115">Gibt den Load Balancer an, der dem zu erhaltenden Back-End-Adresspool zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="9dd3b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9dd3b-116">-Name</span></span>
<span data-ttu-id="9dd3b-117">Gibt den Namen des Load Balancers an, der den zu erhaltenden Back-End-Adresspool enthält.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="9dd3b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd3b-118">CommonParameters</span></span>
<span data-ttu-id="9dd3b-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd3b-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dd3b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd3b-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9dd3b-121">INPUTS</span></span>

### <span data-ttu-id="9dd3b-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9dd3b-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9dd3b-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9dd3b-123">OUTPUTS</span></span>

### <span data-ttu-id="9dd3b-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9dd3b-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="9dd3b-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9dd3b-125">NOTES</span></span>

## <span data-ttu-id="9dd3b-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9dd3b-126">RELATED LINKS</span></span>

[<span data-ttu-id="9dd3b-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9dd3b-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="9dd3b-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9dd3b-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="9dd3b-129">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9dd3b-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="9dd3b-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9dd3b-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


