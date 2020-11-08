---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 341bd8df76870de638db949fb844ac7187776509
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004236"
---
# <span data-ttu-id="ae7f7-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae7f7-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="ae7f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae7f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7f7-103">Entfernt eine Prüf Punkt Konfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="ae7f7-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="ae7f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae7f7-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae7f7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae7f7-105">DESCRIPTION</span></span>
<span data-ttu-id="ae7f7-106">Das Cmdlet **Remove-AzLoadBalancerProbeConfig** entfernt eine Prüf Punkt Konfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="ae7f7-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="ae7f7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae7f7-107">EXAMPLES</span></span>

### <span data-ttu-id="ae7f7-108">Beispiel 1: Entfernen einer Prüf Punkt Konfiguration von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="ae7f7-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="ae7f7-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ae7f7-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="ae7f7-110">Der zweite Befehl löscht die Konfiguration mit dem Namen myprobe aus dem Lastenausgleichsmodul in $LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="ae7f7-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="ae7f7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae7f7-111">PARAMETERS</span></span>

### <span data-ttu-id="ae7f7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae7f7-112">-DefaultProfile</span></span>
<span data-ttu-id="ae7f7-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ae7f7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae7f7-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae7f7-114">-LoadBalancer</span></span>
<span data-ttu-id="ae7f7-115">Gibt das Load Balancer an, das die vom Cmdlet entfernte Prüf Punkt Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="ae7f7-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ae7f7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ae7f7-116">-Name</span></span>
<span data-ttu-id="ae7f7-117">Gibt den Namen der Prüf Punkt Konfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ae7f7-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ae7f7-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ae7f7-118">-Confirm</span></span>
<span data-ttu-id="ae7f7-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae7f7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae7f7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae7f7-120">-WhatIf</span></span>
<span data-ttu-id="ae7f7-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae7f7-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae7f7-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae7f7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae7f7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7f7-123">CommonParameters</span></span>
<span data-ttu-id="ae7f7-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae7f7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7f7-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae7f7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7f7-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae7f7-126">INPUTS</span></span>

### <span data-ttu-id="ae7f7-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae7f7-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ae7f7-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae7f7-128">OUTPUTS</span></span>

### <span data-ttu-id="ae7f7-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae7f7-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ae7f7-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae7f7-130">NOTES</span></span>

## <span data-ttu-id="ae7f7-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae7f7-131">RELATED LINKS</span></span>

[<span data-ttu-id="ae7f7-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae7f7-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ae7f7-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae7f7-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ae7f7-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae7f7-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ae7f7-135">Neu – AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae7f7-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ae7f7-136">Satz-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ae7f7-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


