---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: dd887874540a216cc826f807059e6534b99e28f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472243"
---
# <span data-ttu-id="b4034-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4034-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="b4034-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4034-102">SYNOPSIS</span></span>
<span data-ttu-id="b4034-103">Ruft einen Lastenausgleich ab.</span><span class="sxs-lookup"><span data-stu-id="b4034-103">Gets a load balancer.</span></span>

## <span data-ttu-id="b4034-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4034-104">SYNTAX</span></span>

### <span data-ttu-id="b4034-105">NoExpand (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4034-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4034-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="b4034-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4034-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4034-107">DESCRIPTION</span></span>
<span data-ttu-id="b4034-108">Das **Cmdlet "Get-AzLoadBalancer"** ruft einen oder mehrere Azure Load Balancer ab, die in einer Ressourcengruppe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b4034-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="b4034-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b4034-109">EXAMPLES</span></span>

### <span data-ttu-id="b4034-110">Beispiel 1: Ladenausgleich</span><span class="sxs-lookup"><span data-stu-id="b4034-110">Example 1: Get a load balancer</span></span>
```
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer1" -ResourceGroupName "MyResourceGroup"

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="b4034-111">Dieser Befehl ruft den Lastenausgleich mit dem Namen "MyLoadBalancer" ab.</span><span class="sxs-lookup"><span data-stu-id="b4034-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="b4034-112">Bevor Sie dieses Cmdlet ausführen können, muss ein Lastenausgleich vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b4034-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="b4034-113">Beispiel 2: Auflisten von Lastenausgleichslisten mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="b4034-113">Example 2: List load balancers using filtering</span></span>
```
PS C:\> Get-AzLoadBalancer -Name MyLoadBalancer*

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }

Name                     : MyLoadBalancer2
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="b4034-114">Dieser Befehl ruft alle Lastenausgleichszeilen mit einem Namen ab, der mit "MyLoadBalancer" beginnt.</span><span class="sxs-lookup"><span data-stu-id="b4034-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="b4034-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4034-115">PARAMETERS</span></span>

### <span data-ttu-id="b4034-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4034-116">-DefaultProfile</span></span>
<span data-ttu-id="b4034-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4034-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4034-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b4034-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4034-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b4034-119">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b4034-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4034-120">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b4034-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4034-121">CommonParameters</span></span>
<span data-ttu-id="b4034-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4034-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4034-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4034-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4034-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b4034-124">INPUTS</span></span>

### <span data-ttu-id="b4034-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b4034-125">System.String</span></span>

## <span data-ttu-id="b4034-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b4034-126">OUTPUTS</span></span>

### <span data-ttu-id="b4034-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4034-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b4034-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b4034-128">NOTES</span></span>

## <span data-ttu-id="b4034-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b4034-129">RELATED LINKS</span></span>

[<span data-ttu-id="b4034-130">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4034-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="b4034-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4034-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="b4034-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4034-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


