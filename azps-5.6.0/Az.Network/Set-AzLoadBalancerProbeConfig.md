---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 2dd00c21a0badaca90419615df179299dc2d4240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944872"
---
# <span data-ttu-id="0b124-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b124-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="0b124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b124-102">SYNOPSIS</span></span>
<span data-ttu-id="0b124-103">Aktualisiert eine Prüfpunktkonfiguration für einen Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="0b124-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="0b124-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b124-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b124-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b124-105">DESCRIPTION</span></span>
<span data-ttu-id="0b124-106">Das **Cmdlet Set-AzLoadBalancerProbeConfig** aktualisiert eine Prüfpunktkonfiguration für einen Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="0b124-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="0b124-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b124-107">EXAMPLES</span></span>

### <span data-ttu-id="0b124-108">Beispiel 1: Ändern der Testkonfiguration für einen Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="0b124-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="0b124-109">Der erste Befehl ruft den Loadbalancer mit dem Namen MyLoadBalancer ab und speichert ihn dann in der $slb Variablen.</span><span class="sxs-lookup"><span data-stu-id="0b124-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="0b124-110">Der zweite Befehl verwendet den Pipelineoperator, um den Lastenausgleich in $slb an Add-AzLoadBalancerProbeConfig zu übergeben, wodurch eine neue Sondenkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="0b124-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="0b124-111">Der dritte Befehl übergibt den Load Balancer an **Set-AzLoadBalancerProbeConfig**, wodurch die neue Konfiguration festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="0b124-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig**, which sets the new configuration.</span></span>
<span data-ttu-id="0b124-112">Beachten Sie, dass mehrere der gleichen Parameter angegeben werden müssen, die im vorherigen Befehl angegeben wurden, da sie für das aktuelle Cmdlet erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0b124-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="0b124-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0b124-113">PARAMETERS</span></span>

### <span data-ttu-id="0b124-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b124-114">-DefaultProfile</span></span>
<span data-ttu-id="0b124-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b124-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b124-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0b124-116">-IntervalInSeconds</span></span>
<span data-ttu-id="0b124-117">Gibt das Intervall in Sekunden zwischen Denksonden für jede Instanz des Lastenausgleichsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="0b124-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b124-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b124-118">-LoadBalancer</span></span>
<span data-ttu-id="0b124-119">Gibt einen Lastenausgleich an.</span><span class="sxs-lookup"><span data-stu-id="0b124-119">Specifies a load balancer.</span></span>
<span data-ttu-id="0b124-120">Dieses Cmdlet aktualisiert eine Prüfpunktkonfiguration für den Load Balancer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0b124-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="0b124-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0b124-121">-Name</span></span>
<span data-ttu-id="0b124-122">Gibt den Namen der Prüfpunktkonfiguration an, die von diesem Cmdlet festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="0b124-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b124-123">-Port</span><span class="sxs-lookup"><span data-stu-id="0b124-123">-Port</span></span>
<span data-ttu-id="0b124-124">Gibt den Port an, für den Prüfpunkte eine Verbindung mit einem Lastenausgleichsdienst herstellen sollen.</span><span class="sxs-lookup"><span data-stu-id="0b124-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b124-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="0b124-125">-ProbeCount</span></span>
<span data-ttu-id="0b124-126">Gibt die Anzahl aufeinander folgender Fehler pro Instanz an, damit eine Instanz als fehlerhaft betrachtet wird.</span><span class="sxs-lookup"><span data-stu-id="0b124-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b124-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0b124-127">-Protocol</span></span>
<span data-ttu-id="0b124-128">Gibt das Protokoll an, das für die Sondierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b124-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="0b124-129">Die zulässigen Werte für diesen Parameter sind: Tcp oder Http.</span><span class="sxs-lookup"><span data-stu-id="0b124-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b124-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="0b124-130">-RequestPath</span></span>
<span data-ttu-id="0b124-131">Gibt den Pfad im Lastenausgleichsdienst an, um den Zustand zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="0b124-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b124-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b124-132">-Confirm</span></span>
<span data-ttu-id="0b124-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b124-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b124-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b124-134">-WhatIf</span></span>
<span data-ttu-id="0b124-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b124-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b124-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b124-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b124-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b124-137">CommonParameters</span></span>
<span data-ttu-id="0b124-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b124-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b124-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b124-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b124-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b124-140">INPUTS</span></span>

### <span data-ttu-id="0b124-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b124-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="0b124-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0b124-142">System.String</span></span>

### <span data-ttu-id="0b124-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0b124-143">System.Int32</span></span>

## <span data-ttu-id="0b124-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b124-144">OUTPUTS</span></span>

### <span data-ttu-id="0b124-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b124-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0b124-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0b124-146">NOTES</span></span>

## <span data-ttu-id="0b124-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0b124-147">RELATED LINKS</span></span>

[<span data-ttu-id="0b124-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b124-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="0b124-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b124-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0b124-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b124-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="0b124-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b124-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="0b124-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b124-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


