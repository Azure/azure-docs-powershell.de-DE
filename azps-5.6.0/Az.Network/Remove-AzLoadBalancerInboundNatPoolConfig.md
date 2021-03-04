---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9e266ad824d5637137649c73d4e3b427af2f176b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941611"
---
# <span data-ttu-id="ba3cb-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ba3cb-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="ba3cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba3cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ba3cb-103">Entfernt eine eingehende NAT-Poolkonfiguration aus einem Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="ba3cb-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="ba3cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba3cb-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba3cb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba3cb-105">DESCRIPTION</span></span>
<span data-ttu-id="ba3cb-106">Das **Cmdlet Remove-AzLoadBalancerInboundNatPoolConfig** entfernt eine eingehende NAT-Poolkonfiguration aus einem Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="ba3cb-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="ba3cb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba3cb-107">EXAMPLES</span></span>

### <span data-ttu-id="ba3cb-108">1: Entfernen</span><span class="sxs-lookup"><span data-stu-id="ba3cb-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="ba3cb-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ba3cb-109">PARAMETERS</span></span>

### <span data-ttu-id="ba3cb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba3cb-110">-DefaultProfile</span></span>
<span data-ttu-id="ba3cb-111">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba3cb-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba3cb-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ba3cb-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="ba3cb-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ba3cb-113">-Name</span></span>
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

### <span data-ttu-id="ba3cb-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba3cb-114">-Confirm</span></span>
<span data-ttu-id="ba3cb-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba3cb-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba3cb-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba3cb-116">-WhatIf</span></span>
<span data-ttu-id="ba3cb-117">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba3cb-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba3cb-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba3cb-118">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba3cb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba3cb-119">CommonParameters</span></span>
<span data-ttu-id="ba3cb-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba3cb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba3cb-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba3cb-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba3cb-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba3cb-122">INPUTS</span></span>

### <span data-ttu-id="ba3cb-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ba3cb-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ba3cb-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba3cb-124">OUTPUTS</span></span>

### <span data-ttu-id="ba3cb-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ba3cb-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ba3cb-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ba3cb-126">NOTES</span></span>

## <span data-ttu-id="ba3cb-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ba3cb-127">RELATED LINKS</span></span>

[<span data-ttu-id="ba3cb-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ba3cb-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="ba3cb-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ba3cb-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="ba3cb-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ba3cb-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="ba3cb-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ba3cb-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
