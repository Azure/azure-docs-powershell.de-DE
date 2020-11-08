---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 26f7e0dde825305e888d598a23af0b2fbaff81cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176285"
---
# <span data-ttu-id="ceb8a-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ceb8a-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="ceb8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ceb8a-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb8a-103">Entfernt eine Konfiguration des Back-End-Adresspools aus einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="ceb8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ceb8a-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceb8a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ceb8a-105">DESCRIPTION</span></span>
<span data-ttu-id="ceb8a-106">Das Cmdlet **Remove-AzLoadBalancerBackendAddressPoolConfig** entfernt einen Back-End-Adresspool aus einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="ceb8a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ceb8a-107">EXAMPLES</span></span>

### <span data-ttu-id="ceb8a-108">Beispiel 1: Entfernen einer Konfiguration des Back-End-Adresspools von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="ceb8a-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="ceb8a-109">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und übergibt es an **Remove-AzLoadBalancerBackendAddressPoolConfig** , wodurch die BackendAddressPool02-Konfiguration von MyLoadBalancer entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="ceb8a-110">Schließlich aktualisiert das Set-AzLoadBalancer-Cmdlet MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="ceb8a-111">Beachten Sie, dass eine Konfiguration des Back-End-Adresspools vorhanden sein muss, bevor Sie Sie löschen können.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="ceb8a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ceb8a-112">PARAMETERS</span></span>

### <span data-ttu-id="ceb8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceb8a-113">-DefaultProfile</span></span>
<span data-ttu-id="ceb8a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceb8a-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ceb8a-115">-LoadBalancer</span></span>
<span data-ttu-id="ceb8a-116">Gibt das Load Balancer an, das den zu entfernenden Back-End-Adresspool enthält.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="ceb8a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ceb8a-117">-Name</span></span>
<span data-ttu-id="ceb8a-118">Gibt den Namen des Back-End-Adresspools an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ceb8a-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ceb8a-119">-Confirm</span></span>
<span data-ttu-id="ceb8a-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceb8a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceb8a-121">-WhatIf</span></span>
<span data-ttu-id="ceb8a-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ceb8a-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceb8a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb8a-124">CommonParameters</span></span>
<span data-ttu-id="ceb8a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb8a-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceb8a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb8a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ceb8a-127">INPUTS</span></span>

### <span data-ttu-id="ceb8a-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ceb8a-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ceb8a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ceb8a-129">OUTPUTS</span></span>

### <span data-ttu-id="ceb8a-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ceb8a-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ceb8a-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="ceb8a-131">NOTES</span></span>

## <span data-ttu-id="ceb8a-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ceb8a-132">RELATED LINKS</span></span>

[<span data-ttu-id="ceb8a-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ceb8a-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="ceb8a-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ceb8a-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ceb8a-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ceb8a-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="ceb8a-136">Neu – AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ceb8a-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


