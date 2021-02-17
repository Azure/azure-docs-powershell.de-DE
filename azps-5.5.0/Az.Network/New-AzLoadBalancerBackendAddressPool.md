---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146884"
---
# <span data-ttu-id="cef26-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cef26-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="cef26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cef26-102">SYNOPSIS</span></span>
<span data-ttu-id="cef26-103">Erstellt einen Back-End-Adresspool für ein Lastenausgleichs-Konto.</span><span class="sxs-lookup"><span data-stu-id="cef26-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="cef26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cef26-104">SYNTAX</span></span>

### <span data-ttu-id="cef26-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cef26-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef26-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cef26-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef26-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cef26-107">DESCRIPTION</span></span>
<span data-ttu-id="cef26-108">Erstellt einen Back-End-Adresspool für ein Lastenausgleichs-Konto.</span><span class="sxs-lookup"><span data-stu-id="cef26-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="cef26-109">Ermöglicht die Spezifikation eines Arrays von PSLoadBalancerBackendAddress.</span><span class="sxs-lookup"><span data-stu-id="cef26-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="cef26-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cef26-110">EXAMPLES</span></span>

### <span data-ttu-id="cef26-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cef26-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="cef26-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cef26-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="cef26-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="cef26-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="cef26-114">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="cef26-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="cef26-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cef26-115">PARAMETERS</span></span>

### <span data-ttu-id="cef26-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef26-116">-DefaultProfile</span></span>
<span data-ttu-id="cef26-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cef26-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cef26-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cef26-118">-LoadBalancer</span></span>
<span data-ttu-id="cef26-119">Die Lastenausgleichsressource.</span><span class="sxs-lookup"><span data-stu-id="cef26-119">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cef26-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="cef26-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="cef26-121">Die Back-End-Adressen.</span><span class="sxs-lookup"><span data-stu-id="cef26-121">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef26-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="cef26-122">-LoadBalancerName</span></span>
<span data-ttu-id="cef26-123">Der Name des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="cef26-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef26-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cef26-124">-Name</span></span>
<span data-ttu-id="cef26-125">Der Name des Back-End-Pools.</span><span class="sxs-lookup"><span data-stu-id="cef26-125">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef26-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef26-126">-ResourceGroupName</span></span>
<span data-ttu-id="cef26-127">Der Ressourcengruppenname des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="cef26-127">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef26-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cef26-128">-Confirm</span></span>
<span data-ttu-id="cef26-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cef26-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef26-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cef26-130">-WhatIf</span></span>
<span data-ttu-id="cef26-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cef26-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef26-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cef26-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef26-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef26-133">CommonParameters</span></span>
<span data-ttu-id="cef26-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef26-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef26-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cef26-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef26-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cef26-136">INPUTS</span></span>

### <span data-ttu-id="cef26-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cef26-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cef26-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cef26-138">OUTPUTS</span></span>

### <span data-ttu-id="cef26-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cef26-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="cef26-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cef26-140">NOTES</span></span>

## <span data-ttu-id="cef26-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cef26-141">RELATED LINKS</span></span>
