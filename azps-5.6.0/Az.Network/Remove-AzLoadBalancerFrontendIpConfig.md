---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 30b66350cffeae7fa42da7c9230a9f3976ab6cc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940115"
---
# <span data-ttu-id="df447-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="df447-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="df447-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df447-102">SYNOPSIS</span></span>
<span data-ttu-id="df447-103">Entfernt eine Front-End-IP-Konfiguration aus einem Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="df447-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="df447-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df447-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df447-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df447-105">DESCRIPTION</span></span>
<span data-ttu-id="df447-106">Das **Cmdlet Remove-AzLoadBalancerFrontendIpConfig** entfernt eine Front-End-IP-Konfiguration aus einem Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="df447-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="df447-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="df447-107">EXAMPLES</span></span>

### <span data-ttu-id="df447-108">Beispiel 1: Entfernen einer Front-End-IP-Konfiguration aus einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="df447-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="df447-109">Der erste Befehl ruft den Load Balancer ab, der der front-end-IP-Konfiguration zugeordnet ist, die Sie entfernen möchten, und speichert ihn dann in der $loadbalancer Variablen.</span><span class="sxs-lookup"><span data-stu-id="df447-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="df447-110">Der zweite Befehl entfernt die zugeordnete Frontend-IP-Konfiguration aus dem Load Balancer in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="df447-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="df447-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="df447-111">PARAMETERS</span></span>

### <span data-ttu-id="df447-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df447-112">-DefaultProfile</span></span>
<span data-ttu-id="df447-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df447-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df447-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="df447-114">-LoadBalancer</span></span>
<span data-ttu-id="df447-115">Gibt den Load Balancer an, der die zu entfernende Front-End-IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="df447-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="df447-116">-Name</span><span class="sxs-lookup"><span data-stu-id="df447-116">-Name</span></span>
<span data-ttu-id="df447-117">Gibt den Namen der zu entfernenden Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="df447-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="df447-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="df447-118">-Confirm</span></span>
<span data-ttu-id="df447-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df447-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df447-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df447-120">-WhatIf</span></span>
<span data-ttu-id="df447-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df447-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df447-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df447-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df447-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df447-123">CommonParameters</span></span>
<span data-ttu-id="df447-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df447-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df447-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df447-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df447-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="df447-126">INPUTS</span></span>

### <span data-ttu-id="df447-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="df447-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="df447-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="df447-128">OUTPUTS</span></span>

### <span data-ttu-id="df447-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="df447-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="df447-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="df447-130">NOTES</span></span>

## <span data-ttu-id="df447-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="df447-131">RELATED LINKS</span></span>

[<span data-ttu-id="df447-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="df447-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="df447-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="df447-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="df447-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="df447-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="df447-135">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="df447-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="df447-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="df447-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


