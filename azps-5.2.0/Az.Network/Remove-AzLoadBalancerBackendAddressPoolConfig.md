---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 26f7e0dde825305e888d598a23af0b2fbaff81cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293501"
---
# <span data-ttu-id="7bf8e-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7bf8e-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="7bf8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bf8e-102">SYNOPSIS</span></span>
<span data-ttu-id="7bf8e-103">Entfernt die Konfiguration eines Back-End-Adresspools aus einem Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="7bf8e-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="7bf8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bf8e-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bf8e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bf8e-105">DESCRIPTION</span></span>
<span data-ttu-id="7bf8e-106">Das **Cmdlet "Remove-AzLoadBalancerBackendAddressPoolConfig"** entfernt einen Back-End-Adresspool aus einem Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="7bf8e-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="7bf8e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7bf8e-107">EXAMPLES</span></span>

### <span data-ttu-id="7bf8e-108">Beispiel 1: Entfernen einer Back-End-Adresspoolkonfiguration aus einem Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="7bf8e-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="7bf8e-109">Dieser Befehl ruft den Lastenausgleich namens "MyLoadBalancer" ab und übergibt ihn an **"Remove-AzLoadBalancerBackendAddressPoolConfig",** wodurch die Back-EndAddressPool02-Konfiguration aus MyLoadBalancer entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7bf8e-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig**, which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="7bf8e-110">Schließlich aktualisiert das Set-AzLoadBalancer Das Cmdlet MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="7bf8e-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="7bf8e-111">Beachten Sie, dass eine Konfiguration des Back-End-Adresspools vorhanden sein muss, bevor Sie sie löschen können.</span><span class="sxs-lookup"><span data-stu-id="7bf8e-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="7bf8e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bf8e-112">PARAMETERS</span></span>

### <span data-ttu-id="7bf8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bf8e-113">-DefaultProfile</span></span>
<span data-ttu-id="7bf8e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7bf8e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bf8e-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7bf8e-115">-LoadBalancer</span></span>
<span data-ttu-id="7bf8e-116">Gibt den Lastenausgleich an, der den zu entfernenden Back-End-Adresspool enthält.</span><span class="sxs-lookup"><span data-stu-id="7bf8e-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="7bf8e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7bf8e-117">-Name</span></span>
<span data-ttu-id="7bf8e-118">Gibt den Namen des Back-End-Adresspools an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="7bf8e-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7bf8e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bf8e-119">-Confirm</span></span>
<span data-ttu-id="7bf8e-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bf8e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bf8e-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7bf8e-121">-WhatIf</span></span>
<span data-ttu-id="7bf8e-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bf8e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bf8e-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7bf8e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bf8e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bf8e-124">CommonParameters</span></span>
<span data-ttu-id="7bf8e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bf8e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bf8e-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bf8e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bf8e-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7bf8e-127">INPUTS</span></span>

### <span data-ttu-id="7bf8e-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7bf8e-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7bf8e-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7bf8e-129">OUTPUTS</span></span>

### <span data-ttu-id="7bf8e-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7bf8e-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7bf8e-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7bf8e-131">NOTES</span></span>

## <span data-ttu-id="7bf8e-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7bf8e-132">RELATED LINKS</span></span>

[<span data-ttu-id="7bf8e-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7bf8e-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="7bf8e-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7bf8e-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7bf8e-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7bf8e-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="7bf8e-136">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7bf8e-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


