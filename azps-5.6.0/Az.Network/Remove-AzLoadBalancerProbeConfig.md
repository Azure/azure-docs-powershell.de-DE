---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 3e7433c8c779c078ab1b264e6b724d06cd884bab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940112"
---
# <span data-ttu-id="eec3d-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eec3d-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="eec3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eec3d-102">SYNOPSIS</span></span>
<span data-ttu-id="eec3d-103">Entfernt eine Sondenkonfiguration aus einem Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="eec3d-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="eec3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eec3d-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eec3d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eec3d-105">DESCRIPTION</span></span>
<span data-ttu-id="eec3d-106">Das **Cmdlet Remove-AzLoadBalancerProbeConfig** entfernt eine Prüfpunktkonfiguration aus einem Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="eec3d-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="eec3d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eec3d-107">EXAMPLES</span></span>

### <span data-ttu-id="eec3d-108">Beispiel 1: Entfernen einer Prüfpunktkonfiguration aus einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="eec3d-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="eec3d-109">Der erste Befehl ruft den Load Balancer mit dem Namen MyLoadBalancer ab und speichert ihn dann in $loadbalancer Variablen.</span><span class="sxs-lookup"><span data-stu-id="eec3d-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="eec3d-110">Mit dem zweiten Befehl wird die Konfiguration mit dem Namen MyProbe aus dem Load Balancer in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="eec3d-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="eec3d-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eec3d-111">PARAMETERS</span></span>

### <span data-ttu-id="eec3d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec3d-112">-DefaultProfile</span></span>
<span data-ttu-id="eec3d-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eec3d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eec3d-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eec3d-114">-LoadBalancer</span></span>
<span data-ttu-id="eec3d-115">Gibt den Lastenausgleich an, der die Prüfpunktkonfiguration enthält, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="eec3d-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eec3d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="eec3d-116">-Name</span></span>
<span data-ttu-id="eec3d-117">Gibt den Namen der Prüfpunktkonfiguration an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="eec3d-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eec3d-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eec3d-118">-Confirm</span></span>
<span data-ttu-id="eec3d-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eec3d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eec3d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eec3d-120">-WhatIf</span></span>
<span data-ttu-id="eec3d-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eec3d-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eec3d-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eec3d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eec3d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec3d-123">CommonParameters</span></span>
<span data-ttu-id="eec3d-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eec3d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec3d-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eec3d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec3d-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eec3d-126">INPUTS</span></span>

### <span data-ttu-id="eec3d-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eec3d-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="eec3d-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eec3d-128">OUTPUTS</span></span>

### <span data-ttu-id="eec3d-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eec3d-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="eec3d-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eec3d-130">NOTES</span></span>

## <span data-ttu-id="eec3d-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eec3d-131">RELATED LINKS</span></span>

[<span data-ttu-id="eec3d-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eec3d-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="eec3d-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eec3d-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="eec3d-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eec3d-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="eec3d-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eec3d-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="eec3d-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eec3d-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


