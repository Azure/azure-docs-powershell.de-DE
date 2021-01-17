---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bde16a6f3ecd68307574ae5eac7760a177101cc1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468907"
---
# <span data-ttu-id="39aa5-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="39aa5-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="39aa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="39aa5-103">Entfernt eine Front-End-IP-Konfiguration aus einem Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="39aa5-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="39aa5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39aa5-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39aa5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39aa5-105">DESCRIPTION</span></span>
<span data-ttu-id="39aa5-106">Das **Cmdlet "Remove-AzLoadBalancerFrontendIpConfig"** entfernt eine Front-End-IP-Konfiguration aus einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="39aa5-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="39aa5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39aa5-107">EXAMPLES</span></span>

### <span data-ttu-id="39aa5-108">Beispiel 1: Entfernen einer Front-End-IP-Konfiguration aus einem Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="39aa5-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="39aa5-109">Der erste Befehl ruft den Lastenausgleich ab, der der Front-End-IP-Konfiguration zugeordnet ist, die Sie entfernen möchten, und speichert ihn dann in der $loadbalancer Variable.</span><span class="sxs-lookup"><span data-stu-id="39aa5-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="39aa5-110">Der zweite Befehl entfernt die zugehörige Frontend-IP-Konfiguration aus dem Lastenausgleich in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="39aa5-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="39aa5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39aa5-111">PARAMETERS</span></span>

### <span data-ttu-id="39aa5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39aa5-112">-DefaultProfile</span></span>
<span data-ttu-id="39aa5-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39aa5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39aa5-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39aa5-114">-LoadBalancer</span></span>
<span data-ttu-id="39aa5-115">Gibt den Lastenausgleich an, der die Front-End-IP-Konfiguration enthält, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39aa5-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="39aa5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="39aa5-116">-Name</span></span>
<span data-ttu-id="39aa5-117">Gibt den Namen der Front-End-IP-Adresskonfiguration an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39aa5-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="39aa5-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39aa5-118">-Confirm</span></span>
<span data-ttu-id="39aa5-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39aa5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39aa5-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="39aa5-120">-WhatIf</span></span>
<span data-ttu-id="39aa5-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39aa5-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39aa5-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39aa5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39aa5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39aa5-123">CommonParameters</span></span>
<span data-ttu-id="39aa5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39aa5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39aa5-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39aa5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39aa5-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39aa5-126">INPUTS</span></span>

### <span data-ttu-id="39aa5-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39aa5-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="39aa5-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39aa5-128">OUTPUTS</span></span>

### <span data-ttu-id="39aa5-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39aa5-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="39aa5-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="39aa5-130">NOTES</span></span>

## <span data-ttu-id="39aa5-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="39aa5-131">RELATED LINKS</span></span>

[<span data-ttu-id="39aa5-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="39aa5-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="39aa5-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39aa5-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="39aa5-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="39aa5-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="39aa5-135">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="39aa5-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="39aa5-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="39aa5-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


