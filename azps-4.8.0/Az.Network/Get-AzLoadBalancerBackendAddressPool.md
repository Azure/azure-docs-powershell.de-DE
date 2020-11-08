---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 5d1c561af678086671927d3782a1fafbd9de503b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174341"
---
# <span data-ttu-id="b7132-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b7132-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="b7132-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7132-102">SYNOPSIS</span></span>
<span data-ttu-id="b7132-103">Get-AzLoadBalancerBackendAddressPool ruft einen oder mehrere Back-End-Adresspools ab, die einem Lastenausgleichsmodul zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b7132-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="b7132-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7132-104">SYNTAX</span></span>

### <span data-ttu-id="b7132-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7132-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7132-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7132-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7132-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7132-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7132-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7132-108">DESCRIPTION</span></span>
<span data-ttu-id="b7132-109">Get-AzLoadBalancerBackendAddressPool ruft einen oder mehrere Back-End-Adresspools ab, die einem Lastenausgleichsmodul zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b7132-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="b7132-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7132-110">EXAMPLES</span></span>

### <span data-ttu-id="b7132-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b7132-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="b7132-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b7132-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="b7132-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b7132-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="b7132-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7132-114">PARAMETERS</span></span>

### <span data-ttu-id="b7132-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7132-115">-DefaultProfile</span></span>
<span data-ttu-id="b7132-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7132-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7132-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7132-117">-LoadBalancer</span></span>
<span data-ttu-id="b7132-118">{{Fill LoadBalancer Description}}</span><span class="sxs-lookup"><span data-stu-id="b7132-118">{{ Fill LoadBalancer Description }}</span></span>

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

### <span data-ttu-id="b7132-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="b7132-119">-LoadBalancerName</span></span>
<span data-ttu-id="b7132-120">Der Name des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="b7132-120">The name of the load balancer.</span></span>

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

### <span data-ttu-id="b7132-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b7132-121">-Name</span></span>
<span data-ttu-id="b7132-122">Der Name des Back-End-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="b7132-122">The name of the backend address pool.</span></span>

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

### <span data-ttu-id="b7132-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7132-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7132-124">Der Ressourcengruppenname des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="b7132-124">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="b7132-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b7132-125">-ResourceId</span></span>

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

### <span data-ttu-id="b7132-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7132-126">CommonParameters</span></span>
<span data-ttu-id="b7132-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7132-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7132-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7132-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7132-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7132-129">INPUTS</span></span>

### <span data-ttu-id="b7132-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7132-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b7132-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b7132-131">System.String</span></span>

## <span data-ttu-id="b7132-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7132-132">OUTPUTS</span></span>

### <span data-ttu-id="b7132-133">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b7132-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="b7132-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7132-134">NOTES</span></span>

## <span data-ttu-id="b7132-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7132-135">RELATED LINKS</span></span>
