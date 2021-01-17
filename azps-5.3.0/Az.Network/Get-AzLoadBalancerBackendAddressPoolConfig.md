---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f6acd469c49df7e67e8aa9bf00faf4952a33eb79
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458824"
---
# <span data-ttu-id="2ec0a-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2ec0a-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="2ec0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ec0a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec0a-103">Ruft eine Back-End-Adresspoolkonfiguration für einen Lastenausgleich ab.</span><span class="sxs-lookup"><span data-stu-id="2ec0a-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="2ec0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ec0a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ec0a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ec0a-105">DESCRIPTION</span></span>
<span data-ttu-id="2ec0a-106">Das **Cmdlet "Get-AzLoadBalancerBackendAddressPoolConfig"** ruft einen einzelnen Back-End-Adresspool oder eine Liste von Back-End-Adresspools innerhalb eines Lastenausgleichs ab.</span><span class="sxs-lookup"><span data-stu-id="2ec0a-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="2ec0a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ec0a-107">EXAMPLES</span></span>

### <span data-ttu-id="2ec0a-108">Beispiel 1: Erhalten des Back-End-Adresspools</span><span class="sxs-lookup"><span data-stu-id="2ec0a-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="2ec0a-109">Der erste Befehl ruft einen vorhandenen Lastenausgleich namens "MyLoadBalancer" in der Ressourcengruppe mit dem Namen "MyResourceGroup" ab und speichert ihn dann in der $loadbalancer Variable.</span><span class="sxs-lookup"><span data-stu-id="2ec0a-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="2ec0a-110">Der zweite Befehl ruft die zugehörige Back-End-Adresspool-Konfiguration namens Back-End-Adresspool02 für den Lastenausgleich in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="2ec0a-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="2ec0a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ec0a-111">PARAMETERS</span></span>

### <span data-ttu-id="2ec0a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec0a-112">-DefaultProfile</span></span>
<span data-ttu-id="2ec0a-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ec0a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ec0a-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ec0a-114">-LoadBalancer</span></span>
<span data-ttu-id="2ec0a-115">Gibt den Lastenausgleich an, der dem zu erhaltenden Back-End-Adresspool zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2ec0a-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="2ec0a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2ec0a-116">-Name</span></span>
<span data-ttu-id="2ec0a-117">Gibt den Namen des Lastenausgleichs an, der den zu erhaltenden Back-End-Adresspool enthält.</span><span class="sxs-lookup"><span data-stu-id="2ec0a-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="2ec0a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec0a-118">CommonParameters</span></span>
<span data-ttu-id="2ec0a-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec0a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec0a-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ec0a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec0a-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ec0a-121">INPUTS</span></span>

### <span data-ttu-id="2ec0a-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ec0a-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2ec0a-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ec0a-123">OUTPUTS</span></span>

### <span data-ttu-id="2ec0a-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2ec0a-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="2ec0a-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2ec0a-125">NOTES</span></span>

## <span data-ttu-id="2ec0a-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2ec0a-126">RELATED LINKS</span></span>

[<span data-ttu-id="2ec0a-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2ec0a-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="2ec0a-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ec0a-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="2ec0a-129">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2ec0a-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="2ec0a-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2ec0a-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


