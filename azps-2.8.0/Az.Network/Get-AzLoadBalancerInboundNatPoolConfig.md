---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: da7004c8737bf454ea8847b529f003f5b1909f9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821823"
---
# <span data-ttu-id="8ffd8-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ffd8-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="8ffd8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ffd8-102">SYNOPSIS</span></span>
<span data-ttu-id="8ffd8-103">Ruft mindestens eine eingehende NAT-Poolkonfiguration von einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="8ffd8-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="8ffd8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ffd8-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ffd8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ffd8-105">DESCRIPTION</span></span>
<span data-ttu-id="8ffd8-106">Das Cmdlet " **Get-AzLoadBalancerInboundNatPoolConfig** " ruft mindestens eine eingehende NAT-Poolkonfiguration von einem Load Balancer ab.</span><span class="sxs-lookup"><span data-stu-id="8ffd8-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="8ffd8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ffd8-107">EXAMPLES</span></span>

### <span data-ttu-id="8ffd8-108">1: Abrufen</span><span class="sxs-lookup"><span data-stu-id="8ffd8-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="8ffd8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ffd8-109">PARAMETERS</span></span>

### <span data-ttu-id="8ffd8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ffd8-110">-DefaultProfile</span></span>
<span data-ttu-id="8ffd8-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ffd8-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ffd8-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8ffd8-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="8ffd8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8ffd8-113">-Name</span></span>
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

### <span data-ttu-id="8ffd8-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ffd8-114">CommonParameters</span></span>
<span data-ttu-id="8ffd8-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ffd8-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ffd8-116">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ffd8-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ffd8-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ffd8-117">INPUTS</span></span>

### <span data-ttu-id="8ffd8-118">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8ffd8-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8ffd8-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ffd8-119">OUTPUTS</span></span>

### <span data-ttu-id="8ffd8-120">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="8ffd8-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="8ffd8-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ffd8-121">NOTES</span></span>

## <span data-ttu-id="8ffd8-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ffd8-122">RELATED LINKS</span></span>

[<span data-ttu-id="8ffd8-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ffd8-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8ffd8-124">Neu – AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ffd8-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8ffd8-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ffd8-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8ffd8-126">Satz-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ffd8-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
