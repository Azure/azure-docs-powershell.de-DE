---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 08644bd8b9846b0eb7d647b3df9c12008070c059
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940123"
---
# <span data-ttu-id="491c7-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="491c7-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="491c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="491c7-102">SYNOPSIS</span></span>
<span data-ttu-id="491c7-103">Entfernt eine Back-End-Adresspoolkonfiguration aus einem Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="491c7-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="491c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="491c7-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="491c7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="491c7-105">DESCRIPTION</span></span>
<span data-ttu-id="491c7-106">Das **Cmdlet Remove-AzLoadBalancerBackendAddressPoolConfig** entfernt einen Back-End-Adresspool aus einem Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="491c7-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="491c7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="491c7-107">EXAMPLES</span></span>

### <span data-ttu-id="491c7-108">Beispiel 1: Entfernen einer Back-End-Adresspoolkonfiguration aus einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="491c7-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="491c7-109">Dieser Befehl ruft den Load Balancer mit dem Namen MyLoadBalancer ab und übergibt ihn an **Remove-AzLoadBalancerBackendAddressPoolConfig**, wodurch die Back-EndAddressPool02-Konfiguration aus MyLoadBalancer entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="491c7-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig**, which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="491c7-110">Schließlich aktualisiert das Set-AzLoadBalancer MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="491c7-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="491c7-111">Beachten Sie, dass eine Konfiguration des Back-End-Adresspools vorhanden sein muss, bevor Sie sie löschen können.</span><span class="sxs-lookup"><span data-stu-id="491c7-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="491c7-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="491c7-112">PARAMETERS</span></span>

### <span data-ttu-id="491c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="491c7-113">-DefaultProfile</span></span>
<span data-ttu-id="491c7-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="491c7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="491c7-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="491c7-115">-LoadBalancer</span></span>
<span data-ttu-id="491c7-116">Gibt den Load Balancer an, der den zu entfernenden Back-End-Adresspool enthält.</span><span class="sxs-lookup"><span data-stu-id="491c7-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="491c7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="491c7-117">-Name</span></span>
<span data-ttu-id="491c7-118">Gibt den Namen des Back-End-Adresspools an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="491c7-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="491c7-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="491c7-119">-Confirm</span></span>
<span data-ttu-id="491c7-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="491c7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="491c7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="491c7-121">-WhatIf</span></span>
<span data-ttu-id="491c7-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="491c7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="491c7-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="491c7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="491c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="491c7-124">CommonParameters</span></span>
<span data-ttu-id="491c7-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="491c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="491c7-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="491c7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="491c7-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="491c7-127">INPUTS</span></span>

### <span data-ttu-id="491c7-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="491c7-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="491c7-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="491c7-129">OUTPUTS</span></span>

### <span data-ttu-id="491c7-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="491c7-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="491c7-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="491c7-131">NOTES</span></span>

## <span data-ttu-id="491c7-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="491c7-132">RELATED LINKS</span></span>

[<span data-ttu-id="491c7-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="491c7-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="491c7-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="491c7-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="491c7-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="491c7-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="491c7-136">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="491c7-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


