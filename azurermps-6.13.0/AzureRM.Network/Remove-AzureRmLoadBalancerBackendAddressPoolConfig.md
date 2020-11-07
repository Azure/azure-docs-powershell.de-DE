---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 065aa3718f1a66949265e7dca39880c1eff21fa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662676"
---
# <span data-ttu-id="63341-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="63341-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="63341-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63341-102">SYNOPSIS</span></span>
<span data-ttu-id="63341-103">Entfernt eine Konfiguration des Back-End-Adresspools aus einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="63341-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63341-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63341-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63341-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63341-105">DESCRIPTION</span></span>
<span data-ttu-id="63341-106">Das Cmdlet **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** entfernt einen Back-End-Adresspool aus einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="63341-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="63341-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63341-107">EXAMPLES</span></span>

### <span data-ttu-id="63341-108">Beispiel 1: Entfernen einer Konfiguration des Back-End-Adresspools von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="63341-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="63341-109">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und übergibt es an **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , wodurch die BackendAddressPool02-Konfiguration von MyLoadBalancer entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="63341-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="63341-110">Schließlich aktualisiert das Set-AzureRmLoadBalancer-Cmdlet MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="63341-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="63341-111">Beachten Sie, dass eine Konfiguration des Back-End-Adresspools vorhanden sein muss, bevor Sie Sie löschen können.</span><span class="sxs-lookup"><span data-stu-id="63341-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="63341-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="63341-112">PARAMETERS</span></span>

### <span data-ttu-id="63341-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63341-113">-DefaultProfile</span></span>
<span data-ttu-id="63341-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="63341-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63341-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="63341-115">-LoadBalancer</span></span>
<span data-ttu-id="63341-116">Gibt das Load Balancer an, das den zu entfernenden Back-End-Adresspool enthält.</span><span class="sxs-lookup"><span data-stu-id="63341-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="63341-117">-Name</span><span class="sxs-lookup"><span data-stu-id="63341-117">-Name</span></span>
<span data-ttu-id="63341-118">Gibt den Namen des Back-End-Adresspools an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="63341-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="63341-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="63341-119">-Confirm</span></span>
<span data-ttu-id="63341-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63341-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63341-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63341-121">-WhatIf</span></span>
<span data-ttu-id="63341-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63341-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63341-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63341-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63341-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63341-124">CommonParameters</span></span>
<span data-ttu-id="63341-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63341-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63341-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63341-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63341-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63341-127">INPUTS</span></span>

### <span data-ttu-id="63341-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="63341-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="63341-129">Parameter: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="63341-129">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="63341-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63341-130">OUTPUTS</span></span>

### <span data-ttu-id="63341-131">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="63341-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="63341-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="63341-132">NOTES</span></span>

## <span data-ttu-id="63341-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63341-133">RELATED LINKS</span></span>

[<span data-ttu-id="63341-134">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="63341-134">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="63341-135">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="63341-135">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="63341-136">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="63341-136">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="63341-137">Neu – AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="63341-137">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


