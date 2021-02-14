---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170009"
---
# <span data-ttu-id="3ed2b-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3ed2b-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="3ed2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ed2b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed2b-103">Ruft eine oder mehrere eingehende NAT-Poolkonfigurationen aus einem Lastenausgleich ab.</span><span class="sxs-lookup"><span data-stu-id="3ed2b-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="3ed2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ed2b-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ed2b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ed2b-105">DESCRIPTION</span></span>
<span data-ttu-id="3ed2b-106">Das **Cmdlet "Get-AzLoadBalancerInboundNatPoolConfig"** ruft eine oder mehrere eingehende NAT-Poolkonfigurationen aus einem Lastenausgleich ab.</span><span class="sxs-lookup"><span data-stu-id="3ed2b-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="3ed2b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ed2b-107">EXAMPLES</span></span>

### <span data-ttu-id="3ed2b-108">1: Erhalten</span><span class="sxs-lookup"><span data-stu-id="3ed2b-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="3ed2b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ed2b-109">PARAMETERS</span></span>

### <span data-ttu-id="3ed2b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed2b-110">-DefaultProfile</span></span>
<span data-ttu-id="3ed2b-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ed2b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ed2b-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3ed2b-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="3ed2b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3ed2b-113">-Name</span></span>
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

### <span data-ttu-id="3ed2b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed2b-114">CommonParameters</span></span>
<span data-ttu-id="3ed2b-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ed2b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed2b-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ed2b-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed2b-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ed2b-117">INPUTS</span></span>

### <span data-ttu-id="3ed2b-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3ed2b-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3ed2b-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ed2b-119">OUTPUTS</span></span>

### <span data-ttu-id="3ed2b-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="3ed2b-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="3ed2b-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3ed2b-121">NOTES</span></span>

## <span data-ttu-id="3ed2b-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3ed2b-122">RELATED LINKS</span></span>

[<span data-ttu-id="3ed2b-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3ed2b-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="3ed2b-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3ed2b-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="3ed2b-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3ed2b-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="3ed2b-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3ed2b-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
