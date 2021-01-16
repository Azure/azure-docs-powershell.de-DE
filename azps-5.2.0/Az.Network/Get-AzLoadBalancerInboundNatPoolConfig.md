---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358895"
---
# <span data-ttu-id="f74af-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f74af-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="f74af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f74af-102">SYNOPSIS</span></span>
<span data-ttu-id="f74af-103">Ruft eine oder mehrere eingehende NAT-Poolkonfigurationen aus einem Lastenausgleich ab.</span><span class="sxs-lookup"><span data-stu-id="f74af-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="f74af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f74af-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f74af-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f74af-105">DESCRIPTION</span></span>
<span data-ttu-id="f74af-106">Das **Cmdlet "Get-AzLoadBalancerInboundNatPoolConfig"** ruft eine oder mehrere eingehende NAT-Poolkonfigurationen aus einem Lastenausgleich ab.</span><span class="sxs-lookup"><span data-stu-id="f74af-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="f74af-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f74af-107">EXAMPLES</span></span>

### <span data-ttu-id="f74af-108">1: Erhalten</span><span class="sxs-lookup"><span data-stu-id="f74af-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="f74af-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f74af-109">PARAMETERS</span></span>

### <span data-ttu-id="f74af-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f74af-110">-DefaultProfile</span></span>
<span data-ttu-id="f74af-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f74af-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f74af-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f74af-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="f74af-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f74af-113">-Name</span></span>
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

### <span data-ttu-id="f74af-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f74af-114">CommonParameters</span></span>
<span data-ttu-id="f74af-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f74af-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f74af-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f74af-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f74af-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f74af-117">INPUTS</span></span>

### <span data-ttu-id="f74af-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f74af-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f74af-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f74af-119">OUTPUTS</span></span>

### <span data-ttu-id="f74af-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="f74af-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="f74af-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f74af-121">NOTES</span></span>

## <span data-ttu-id="f74af-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f74af-122">RELATED LINKS</span></span>

[<span data-ttu-id="f74af-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f74af-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="f74af-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f74af-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="f74af-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f74af-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="f74af-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f74af-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
