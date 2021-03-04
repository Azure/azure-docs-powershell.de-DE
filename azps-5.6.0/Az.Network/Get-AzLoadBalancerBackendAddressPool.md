---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 72afb446b41143348b9feaa7e1b465a41d2b9cbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921032"
---
# <span data-ttu-id="95805-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="95805-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="95805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95805-102">SYNOPSIS</span></span>
<span data-ttu-id="95805-103">Get-AzLoadBalancerBackendAddressPool ruft einen oder mehrere Back-End-Adresspools ab, die einem Load Balancer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="95805-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="95805-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95805-104">SYNTAX</span></span>

### <span data-ttu-id="95805-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="95805-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95805-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95805-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95805-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95805-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95805-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95805-108">DESCRIPTION</span></span>
<span data-ttu-id="95805-109">Get-AzLoadBalancerBackendAddressPool ruft einen oder mehrere Back-End-Adresspools ab, die einem Load Balancer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="95805-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="95805-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95805-110">EXAMPLES</span></span>

### <span data-ttu-id="95805-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95805-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="95805-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="95805-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="95805-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="95805-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="95805-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="95805-114">PARAMETERS</span></span>

### <span data-ttu-id="95805-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95805-115">-DefaultProfile</span></span>
<span data-ttu-id="95805-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95805-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95805-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95805-117">-LoadBalancer</span></span>
<span data-ttu-id="95805-118">{{ Fill LoadBalancer Description }}</span><span class="sxs-lookup"><span data-stu-id="95805-118">{{ Fill LoadBalancer Description }}</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95805-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="95805-119">-LoadBalancerName</span></span>
<span data-ttu-id="95805-120">Der Name des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="95805-120">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95805-121">-Name</span><span class="sxs-lookup"><span data-stu-id="95805-121">-Name</span></span>
<span data-ttu-id="95805-122">Der Name des Back-End-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="95805-122">The name of the backend address pool.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95805-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95805-123">-ResourceGroupName</span></span>
<span data-ttu-id="95805-124">Der Ressourcengruppenname des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="95805-124">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95805-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95805-125">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95805-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95805-126">CommonParameters</span></span>
<span data-ttu-id="95805-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95805-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95805-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95805-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95805-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95805-129">INPUTS</span></span>

### <span data-ttu-id="95805-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95805-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="95805-131">System.String</span><span class="sxs-lookup"><span data-stu-id="95805-131">System.String</span></span>

## <span data-ttu-id="95805-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95805-132">OUTPUTS</span></span>

### <span data-ttu-id="95805-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="95805-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="95805-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="95805-134">NOTES</span></span>

## <span data-ttu-id="95805-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="95805-135">RELATED LINKS</span></span>
