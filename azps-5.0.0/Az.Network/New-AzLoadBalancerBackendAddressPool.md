---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178465"
---
# <span data-ttu-id="a8186-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a8186-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="a8186-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8186-102">SYNOPSIS</span></span>
<span data-ttu-id="a8186-103">Erstellt einen Back-End-Adresspool auf einem Loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a8186-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="a8186-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8186-104">SYNTAX</span></span>

### <span data-ttu-id="a8186-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8186-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8186-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8186-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8186-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8186-107">DESCRIPTION</span></span>
<span data-ttu-id="a8186-108">Erstellt einen Back-End-Adresspool auf einem Loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a8186-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="a8186-109">Ermöglicht Angabe ein Array von PSLoadBalancerBackendAddress.</span><span class="sxs-lookup"><span data-stu-id="a8186-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="a8186-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8186-110">EXAMPLES</span></span>

### <span data-ttu-id="a8186-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a8186-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="a8186-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a8186-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="a8186-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a8186-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="a8186-114">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="a8186-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="a8186-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8186-115">PARAMETERS</span></span>

### <span data-ttu-id="a8186-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8186-116">-DefaultProfile</span></span>
<span data-ttu-id="a8186-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8186-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8186-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a8186-118">-LoadBalancer</span></span>
<span data-ttu-id="a8186-119">Die Load Balancer-Ressource.</span><span class="sxs-lookup"><span data-stu-id="a8186-119">The load balancer resource.</span></span>

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

### <span data-ttu-id="a8186-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="a8186-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="a8186-121">Die Back-End-Adressen.</span><span class="sxs-lookup"><span data-stu-id="a8186-121">The backend addresses.</span></span>

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

### <span data-ttu-id="a8186-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="a8186-122">-LoadBalancerName</span></span>
<span data-ttu-id="a8186-123">Der Name des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="a8186-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="a8186-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a8186-124">-Name</span></span>
<span data-ttu-id="a8186-125">Der Name des Back-End-Pools.</span><span class="sxs-lookup"><span data-stu-id="a8186-125">The name of the backend pool.</span></span>

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

### <span data-ttu-id="a8186-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8186-126">-ResourceGroupName</span></span>
<span data-ttu-id="a8186-127">Der Ressourcengruppenname des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="a8186-127">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="a8186-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a8186-128">-Confirm</span></span>
<span data-ttu-id="a8186-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8186-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8186-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8186-130">-WhatIf</span></span>
<span data-ttu-id="a8186-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8186-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8186-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8186-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8186-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8186-133">CommonParameters</span></span>
<span data-ttu-id="a8186-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8186-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8186-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8186-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8186-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8186-136">INPUTS</span></span>

### <span data-ttu-id="a8186-137">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a8186-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a8186-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8186-138">OUTPUTS</span></span>

### <span data-ttu-id="a8186-139">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a8186-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="a8186-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8186-140">NOTES</span></span>

## <span data-ttu-id="a8186-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8186-141">RELATED LINKS</span></span>
