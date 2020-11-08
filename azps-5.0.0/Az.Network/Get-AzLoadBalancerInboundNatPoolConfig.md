---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176432"
---
# <span data-ttu-id="995ae-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="995ae-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="995ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="995ae-102">SYNOPSIS</span></span>
<span data-ttu-id="995ae-103">Ruft mindestens eine eingehende NAT-Poolkonfiguration von einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="995ae-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="995ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="995ae-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="995ae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="995ae-105">DESCRIPTION</span></span>
<span data-ttu-id="995ae-106">Das Cmdlet " **Get-AzLoadBalancerInboundNatPoolConfig** " ruft mindestens eine eingehende NAT-Poolkonfiguration von einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="995ae-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="995ae-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="995ae-107">EXAMPLES</span></span>

### <span data-ttu-id="995ae-108">1: Abrufen</span><span class="sxs-lookup"><span data-stu-id="995ae-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="995ae-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="995ae-109">PARAMETERS</span></span>

### <span data-ttu-id="995ae-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="995ae-110">-DefaultProfile</span></span>
<span data-ttu-id="995ae-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="995ae-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="995ae-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="995ae-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="995ae-113">-Name</span><span class="sxs-lookup"><span data-stu-id="995ae-113">-Name</span></span>
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

### <span data-ttu-id="995ae-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="995ae-114">CommonParameters</span></span>
<span data-ttu-id="995ae-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="995ae-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="995ae-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="995ae-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="995ae-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="995ae-117">INPUTS</span></span>

### <span data-ttu-id="995ae-118">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="995ae-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="995ae-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="995ae-119">OUTPUTS</span></span>

### <span data-ttu-id="995ae-120">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="995ae-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="995ae-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="995ae-121">NOTES</span></span>

## <span data-ttu-id="995ae-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="995ae-122">RELATED LINKS</span></span>

[<span data-ttu-id="995ae-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="995ae-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="995ae-124">Neu – AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="995ae-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="995ae-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="995ae-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="995ae-126">Satz-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="995ae-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
