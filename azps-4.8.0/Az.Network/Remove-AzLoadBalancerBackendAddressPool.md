---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165186"
---
# <span data-ttu-id="996cf-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="996cf-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="996cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="996cf-102">SYNOPSIS</span></span>
<span data-ttu-id="996cf-103">Entfernt einen Back-End-Pool von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="996cf-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="996cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="996cf-104">SYNTAX</span></span>

### <span data-ttu-id="996cf-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="996cf-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="996cf-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="996cf-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="996cf-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="996cf-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="996cf-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="996cf-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="996cf-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="996cf-109">DESCRIPTION</span></span>
<span data-ttu-id="996cf-110">Entfernt einen Back-End-Pool von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="996cf-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="996cf-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="996cf-111">EXAMPLES</span></span>

### <span data-ttu-id="996cf-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="996cf-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="996cf-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="996cf-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="996cf-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="996cf-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="996cf-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="996cf-115">PARAMETERS</span></span>

### <span data-ttu-id="996cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="996cf-116">-DefaultProfile</span></span>
<span data-ttu-id="996cf-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="996cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="996cf-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="996cf-118">-InputObject</span></span>
<span data-ttu-id="996cf-119">Den zu entfernenden Back-End-Adresspool</span><span class="sxs-lookup"><span data-stu-id="996cf-119">The backend address pool to remove</span></span>

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

### <span data-ttu-id="996cf-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="996cf-120">-LoadBalancer</span></span>
<span data-ttu-id="996cf-121">Die Load Balancer-Ressource.</span><span class="sxs-lookup"><span data-stu-id="996cf-121">The load balancer resource.</span></span>

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

### <span data-ttu-id="996cf-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="996cf-122">-LoadBalancerName</span></span>
<span data-ttu-id="996cf-123">Der Name des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="996cf-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="996cf-124">-Name</span><span class="sxs-lookup"><span data-stu-id="996cf-124">-Name</span></span>
<span data-ttu-id="996cf-125">Der Name des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="996cf-125">The name of the load balancer.</span></span>

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

### <span data-ttu-id="996cf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="996cf-126">-PassThru</span></span>
<span data-ttu-id="996cf-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="996cf-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="996cf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="996cf-128">-ResourceGroupName</span></span>
<span data-ttu-id="996cf-129">Der Ressourcengruppenname des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="996cf-129">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="996cf-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="996cf-130">-ResourceId</span></span>

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

### <span data-ttu-id="996cf-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="996cf-131">-Confirm</span></span>
<span data-ttu-id="996cf-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="996cf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="996cf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="996cf-133">-WhatIf</span></span>
<span data-ttu-id="996cf-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="996cf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="996cf-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="996cf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="996cf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="996cf-136">CommonParameters</span></span>
<span data-ttu-id="996cf-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="996cf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="996cf-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="996cf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="996cf-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="996cf-139">INPUTS</span></span>

### <span data-ttu-id="996cf-140">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="996cf-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="996cf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="996cf-141">System.String</span></span>

## <span data-ttu-id="996cf-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="996cf-142">OUTPUTS</span></span>

### <span data-ttu-id="996cf-143">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="996cf-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="996cf-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="996cf-144">NOTES</span></span>

## <span data-ttu-id="996cf-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="996cf-145">RELATED LINKS</span></span>
