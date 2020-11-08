---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf8afee04e8aaf1a8909988465dc4371575b4309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004241"
---
# <span data-ttu-id="90418-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90418-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="90418-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90418-102">SYNOPSIS</span></span>
<span data-ttu-id="90418-103">Entfernt eine eingehende NAT-Poolkonfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="90418-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="90418-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90418-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90418-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90418-105">DESCRIPTION</span></span>
<span data-ttu-id="90418-106">Das Cmdlet **Remove-AzLoadBalancerInboundNatPoolConfig** entfernt eine eingehende NAT-Poolkonfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="90418-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="90418-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90418-107">EXAMPLES</span></span>

### <span data-ttu-id="90418-108">1: Entfernen</span><span class="sxs-lookup"><span data-stu-id="90418-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="90418-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="90418-109">PARAMETERS</span></span>

### <span data-ttu-id="90418-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90418-110">-DefaultProfile</span></span>
<span data-ttu-id="90418-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90418-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90418-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="90418-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="90418-113">-Name</span><span class="sxs-lookup"><span data-stu-id="90418-113">-Name</span></span>
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

### <span data-ttu-id="90418-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90418-114">-Confirm</span></span>
<span data-ttu-id="90418-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90418-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90418-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90418-116">-WhatIf</span></span>
<span data-ttu-id="90418-117">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90418-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90418-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90418-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90418-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90418-119">CommonParameters</span></span>
<span data-ttu-id="90418-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90418-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90418-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90418-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90418-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90418-122">INPUTS</span></span>

### <span data-ttu-id="90418-123">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="90418-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="90418-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90418-124">OUTPUTS</span></span>

### <span data-ttu-id="90418-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="90418-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="90418-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="90418-126">NOTES</span></span>

## <span data-ttu-id="90418-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90418-127">RELATED LINKS</span></span>

[<span data-ttu-id="90418-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90418-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="90418-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90418-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="90418-130">Neu – AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90418-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="90418-131">Satz-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90418-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
