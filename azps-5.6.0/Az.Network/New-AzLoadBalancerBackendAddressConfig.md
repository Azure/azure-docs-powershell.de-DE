---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 980b16d373f17101266908c0a24443764d96561f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920515"
---
# <span data-ttu-id="4256b-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="4256b-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="4256b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4256b-102">SYNOPSIS</span></span>
<span data-ttu-id="4256b-103">Gibt eine Load Balancer-Back-End-Adresskonfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="4256b-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="4256b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4256b-104">SYNTAX</span></span>

### <span data-ttu-id="4256b-105">SetByResourcePublicIpAddress (Standard)</span><span class="sxs-lookup"><span data-stu-id="4256b-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4256b-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4256b-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4256b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4256b-107">DESCRIPTION</span></span>
<span data-ttu-id="4256b-108">Gibt eine Load Balancer-Back-End-Adresskonfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="4256b-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="4256b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4256b-109">EXAMPLES</span></span>

### <span data-ttu-id="4256b-110">Beispiel 1: Konfiguration der neuen Loadbalanceradresse mit virtuellem Netzwerkverweis</span><span class="sxs-lookup"><span data-stu-id="4256b-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="4256b-111">Beispiel 2: Neue Loadbalanceradressenkonfiguration mit Loadbalancer-Frontend-IP-Konfigurationsreferenz</span><span class="sxs-lookup"><span data-stu-id="4256b-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="4256b-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4256b-112">PARAMETERS</span></span>

### <span data-ttu-id="4256b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4256b-113">-DefaultProfile</span></span>
<span data-ttu-id="4256b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4256b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4256b-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="4256b-115">-IpAddress</span></span>
<span data-ttu-id="4256b-116">Die zum Back-End-Pool hinzuzufügende IPAddress</span><span class="sxs-lookup"><span data-stu-id="4256b-116">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4256b-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4256b-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="4256b-118">Die Load Balancer-Frontend-IP-Konfiguration, die der Konfiguration der Back-End-Adresse zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="4256b-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceFrontendIPConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4256b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4256b-119">-Name</span></span>
<span data-ttu-id="4256b-120">Der Name der Konfiguration der Back-End-Adresse</span><span class="sxs-lookup"><span data-stu-id="4256b-120">The name of the Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4256b-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="4256b-121">-VirtualNetworkId</span></span>
<span data-ttu-id="4256b-122">Das virtuelle Netzwerk, das der Konfiguration der Back-End-Adresse zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="4256b-122">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4256b-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4256b-123">-Confirm</span></span>
<span data-ttu-id="4256b-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4256b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4256b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4256b-125">-WhatIf</span></span>
<span data-ttu-id="4256b-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4256b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4256b-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4256b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4256b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4256b-128">CommonParameters</span></span>
<span data-ttu-id="4256b-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4256b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4256b-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4256b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4256b-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4256b-131">INPUTS</span></span>

### <span data-ttu-id="4256b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4256b-132">System.String</span></span>

### <span data-ttu-id="4256b-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4256b-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4256b-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4256b-134">OUTPUTS</span></span>

### <span data-ttu-id="4256b-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="4256b-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="4256b-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4256b-136">NOTES</span></span>

## <span data-ttu-id="4256b-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4256b-137">RELATED LINKS</span></span>
