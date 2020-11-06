---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: c52546ba0477a2911ac34533060d7a47df0b0698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479470"
---
# <span data-ttu-id="083a0-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="083a0-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="083a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="083a0-102">SYNOPSIS</span></span>
<span data-ttu-id="083a0-103">Entfernt eine Prüf Punkt Konfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="083a0-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="083a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="083a0-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="083a0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="083a0-105">DESCRIPTION</span></span>
<span data-ttu-id="083a0-106">Das Cmdlet **Remove-AzureRmLoadBalancerProbeConfig** entfernt eine Prüf Punkt Konfiguration von einem Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="083a0-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="083a0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="083a0-107">EXAMPLES</span></span>

### <span data-ttu-id="083a0-108">Beispiel 1: Entfernen einer Prüf Punkt Konfiguration von einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="083a0-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="083a0-109">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $LoadBalancer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="083a0-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="083a0-110">Der zweite Befehl löscht die Konfiguration mit dem Namen myprobe aus dem Lastenausgleichsmodul in $LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="083a0-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="083a0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="083a0-111">PARAMETERS</span></span>

### <span data-ttu-id="083a0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083a0-112">-DefaultProfile</span></span>
<span data-ttu-id="083a0-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="083a0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="083a0-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="083a0-114">-LoadBalancer</span></span>
<span data-ttu-id="083a0-115">Gibt das Load Balancer an, das die vom Cmdlet entfernte Prüf Punkt Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="083a0-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="083a0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="083a0-116">-Name</span></span>
<span data-ttu-id="083a0-117">Gibt den Namen der Prüf Punkt Konfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="083a0-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="083a0-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="083a0-118">-Confirm</span></span>
<span data-ttu-id="083a0-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="083a0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="083a0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="083a0-120">-WhatIf</span></span>
<span data-ttu-id="083a0-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="083a0-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="083a0-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="083a0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="083a0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083a0-123">CommonParameters</span></span>
<span data-ttu-id="083a0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083a0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083a0-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="083a0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083a0-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="083a0-126">INPUTS</span></span>

### <span data-ttu-id="083a0-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="083a0-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="083a0-128">Parameter: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="083a0-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="083a0-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="083a0-129">OUTPUTS</span></span>

### <span data-ttu-id="083a0-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="083a0-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="083a0-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="083a0-131">NOTES</span></span>

## <span data-ttu-id="083a0-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="083a0-132">RELATED LINKS</span></span>

[<span data-ttu-id="083a0-133">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="083a0-133">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="083a0-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="083a0-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="083a0-135">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="083a0-135">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="083a0-136">Neu – AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="083a0-136">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="083a0-137">Satz-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="083a0-137">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


