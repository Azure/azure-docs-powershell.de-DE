---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 034e33b1c465f106c1edfa8647fe34233575b801
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306323"
---
# <span data-ttu-id="cbef6-101">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cbef6-101">Set-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="cbef6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbef6-102">SYNOPSIS</span></span>
<span data-ttu-id="cbef6-103">Aktualisiert den Back-End-Pool bei einem Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="cbef6-103">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="cbef6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbef6-104">SYNTAX</span></span>

### <span data-ttu-id="cbef6-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbef6-105">SetByNameParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbef6-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbef6-106">SetByParentObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -Name <String> -LoadBalancer <PSLoadBalancer>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbef6-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbef6-107">SetByInputObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -InputObject <PSBackendAddressPool> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbef6-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbef6-108">SetByResourceIdParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>
 -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbef6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cbef6-109">DESCRIPTION</span></span>
<span data-ttu-id="cbef6-110">Aktualisiert den Back-End-Pool bei einem Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="cbef6-110">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="cbef6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cbef6-111">EXAMPLES</span></span>

### <span data-ttu-id="cbef6-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cbef6-112">Example 1</span></span>
```powershell
###Set by name and modified input object
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip3 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.7" -Name "TestVNetRef3" -VirtualNetworkId $virtualNetwork.id
PS C:\> $ips = @($ip1, $ip2)
PS C:\> $b2 = Get-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool1
PS C:\> $b2.LoadBalancerBackendAddresses.Add($ip3)

PS C:\> Set-AzLoadBalancerBackendAddressPool -InputObject $b2
```
### <span data-ttu-id="cbef6-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cbef6-113">Example 2</span></span>
```powershell
###Set by specific backend from piped loadbalancer and set two IP's
PS C:\> $lb | Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress $ips -Name $backendPool1
```

### <span data-ttu-id="cbef6-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="cbef6-114">Example 3</span></span>
```powershell
### #set by ResourceId
PS C:\> Set-AzLoadBalancerBackendAddressPool -ResourceId b2.Id -LoadBalancerBackendAddress $b2.LoadBalancerBackendAddresses
```

## <span data-ttu-id="cbef6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbef6-115">PARAMETERS</span></span>

### <span data-ttu-id="cbef6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbef6-116">-DefaultProfile</span></span>
<span data-ttu-id="cbef6-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cbef6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbef6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cbef6-118">-Force</span></span>
<span data-ttu-id="cbef6-119">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="cbef6-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cbef6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbef6-120">-InputObject</span></span>
<span data-ttu-id="cbef6-121">Der festgelegte Back-End-Adresspool</span><span class="sxs-lookup"><span data-stu-id="cbef6-121">The backend address pool to set</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbef6-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cbef6-122">-LoadBalancer</span></span>
<span data-ttu-id="cbef6-123">Die Lastenausgleichsressource.</span><span class="sxs-lookup"><span data-stu-id="cbef6-123">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbef6-124">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="cbef6-124">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="cbef6-125">Die Back-End-Adressen.</span><span class="sxs-lookup"><span data-stu-id="cbef6-125">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbef6-126">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="cbef6-126">-LoadBalancerName</span></span>
<span data-ttu-id="cbef6-127">Der Name des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="cbef6-127">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbef6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="cbef6-128">-Name</span></span>
<span data-ttu-id="cbef6-129">Der Name des Back-End-Pools.</span><span class="sxs-lookup"><span data-stu-id="cbef6-129">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbef6-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbef6-130">-PassThru</span></span>
<span data-ttu-id="cbef6-131">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="cbef6-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="cbef6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbef6-132">-ResourceGroupName</span></span>
<span data-ttu-id="cbef6-133">Der Ressourcengruppenname des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="cbef6-133">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbef6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbef6-134">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbef6-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbef6-135">-Confirm</span></span>
<span data-ttu-id="cbef6-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cbef6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbef6-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cbef6-137">-WhatIf</span></span>
<span data-ttu-id="cbef6-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cbef6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbef6-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cbef6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbef6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbef6-140">CommonParameters</span></span>
<span data-ttu-id="cbef6-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbef6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbef6-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbef6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbef6-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cbef6-143">INPUTS</span></span>

### <span data-ttu-id="cbef6-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cbef6-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="cbef6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="cbef6-145">System.String</span></span>

## <span data-ttu-id="cbef6-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cbef6-146">OUTPUTS</span></span>

### <span data-ttu-id="cbef6-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cbef6-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="cbef6-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cbef6-148">NOTES</span></span>

## <span data-ttu-id="cbef6-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cbef6-149">RELATED LINKS</span></span>
