---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 6e12cc4bb296a1c523547aebc44c6992dd2b687e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940131"
---
# <span data-ttu-id="29c02-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="29c02-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="29c02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29c02-102">SYNOPSIS</span></span>
<span data-ttu-id="29c02-103">Entfernt einen Back-End-Pool aus einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="29c02-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="29c02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29c02-104">SYNTAX</span></span>

### <span data-ttu-id="29c02-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="29c02-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c02-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29c02-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29c02-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29c02-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c02-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29c02-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29c02-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29c02-109">DESCRIPTION</span></span>
<span data-ttu-id="29c02-110">Entfernt einen Back-End-Pool aus einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="29c02-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="29c02-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29c02-111">EXAMPLES</span></span>

### <span data-ttu-id="29c02-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29c02-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="29c02-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="29c02-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="29c02-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="29c02-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="29c02-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="29c02-115">PARAMETERS</span></span>

### <span data-ttu-id="29c02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c02-116">-DefaultProfile</span></span>
<span data-ttu-id="29c02-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29c02-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29c02-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29c02-118">-InputObject</span></span>
<span data-ttu-id="29c02-119">Der zu entfernende Back-End-Adresspool</span><span class="sxs-lookup"><span data-stu-id="29c02-119">The backend address pool to remove</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c02-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="29c02-120">-LoadBalancer</span></span>
<span data-ttu-id="29c02-121">Die Load Balancer-Ressource.</span><span class="sxs-lookup"><span data-stu-id="29c02-121">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29c02-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="29c02-122">-LoadBalancerName</span></span>
<span data-ttu-id="29c02-123">Der Name des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="29c02-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="29c02-124">-Name</span><span class="sxs-lookup"><span data-stu-id="29c02-124">-Name</span></span>
<span data-ttu-id="29c02-125">Der Name des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="29c02-125">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c02-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29c02-126">-PassThru</span></span>
<span data-ttu-id="29c02-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="29c02-127">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c02-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c02-128">-ResourceGroupName</span></span>
<span data-ttu-id="29c02-129">Der Ressourcengruppenname des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="29c02-129">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c02-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29c02-130">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29c02-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29c02-131">-Confirm</span></span>
<span data-ttu-id="29c02-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29c02-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29c02-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29c02-133">-WhatIf</span></span>
<span data-ttu-id="29c02-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29c02-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29c02-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29c02-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29c02-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c02-136">CommonParameters</span></span>
<span data-ttu-id="29c02-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c02-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c02-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29c02-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c02-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29c02-139">INPUTS</span></span>

### <span data-ttu-id="29c02-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="29c02-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="29c02-141">System.String</span><span class="sxs-lookup"><span data-stu-id="29c02-141">System.String</span></span>

## <span data-ttu-id="29c02-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29c02-142">OUTPUTS</span></span>

### <span data-ttu-id="29c02-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="29c02-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="29c02-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="29c02-144">NOTES</span></span>

## <span data-ttu-id="29c02-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="29c02-145">RELATED LINKS</span></span>
