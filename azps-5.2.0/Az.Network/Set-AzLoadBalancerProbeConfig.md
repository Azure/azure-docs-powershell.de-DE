---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: d0e3d2b11f79dee858849935d71872f1f1b2dd7f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291287"
---
# <span data-ttu-id="eaf0a-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eaf0a-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="eaf0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaf0a-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf0a-103">Aktualisiert eine Probekonfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="eaf0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eaf0a-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaf0a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eaf0a-105">DESCRIPTION</span></span>
<span data-ttu-id="eaf0a-106">Das **Cmdlet Set-AzLoadBalancerProbeConfig** aktualisiert eine Beispielkonfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="eaf0a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eaf0a-107">EXAMPLES</span></span>

### <span data-ttu-id="eaf0a-108">Beispiel 1: Ändern der Sondenkonfiguration für einen Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="eaf0a-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="eaf0a-109">Der erste Befehl ruft den Lastenausgleichsnamen "MyLoadBalancer" ab und speichert ihn dann in der $slb Variable.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="eaf0a-110">Der zweite Befehl verwendet den Pipelineoperator, um den Lastenausgleich in $slb an Add-AzLoadBalancerProbeConfig zu übergeben, wodurch eine neue Beispielkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="eaf0a-111">Der dritte Befehl übergibt den Lastenausgleich an **Set-AzLoadBalancerProbeConfig,** wodurch die neue Konfiguration festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig**, which sets the new configuration.</span></span>
<span data-ttu-id="eaf0a-112">Beachten Sie, dass sie mehrere der gleichen Parameter angeben müssen, die im vorherigen Befehl angegeben wurden, da sie für das aktuelle Cmdlet erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="eaf0a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eaf0a-113">PARAMETERS</span></span>

### <span data-ttu-id="eaf0a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf0a-114">-DefaultProfile</span></span>
<span data-ttu-id="eaf0a-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaf0a-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="eaf0a-116">-IntervalInSeconds</span></span>
<span data-ttu-id="eaf0a-117">Gibt das Intervall (in Sekunden) zwischen den Einzelnen Instanzen des Diensts mit Lastenausgleich an.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="eaf0a-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eaf0a-118">-LoadBalancer</span></span>
<span data-ttu-id="eaf0a-119">Gibt einen Lastenausgleich an.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-119">Specifies a load balancer.</span></span>
<span data-ttu-id="eaf0a-120">Dieses Cmdlet aktualisiert eine Probekonfiguration für den Lastenausgleich, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="eaf0a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="eaf0a-121">-Name</span></span>
<span data-ttu-id="eaf0a-122">Gibt den Namen der Von diesem Cmdlet festgelegten Sondenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="eaf0a-123">-Port</span><span class="sxs-lookup"><span data-stu-id="eaf0a-123">-Port</span></span>
<span data-ttu-id="eaf0a-124">Gibt den Port an, an dem Sonden eine Verbindung mit einem Dienst mit Lastenausgleich herstellen sollen.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="eaf0a-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="eaf0a-125">-ProbeCount</span></span>
<span data-ttu-id="eaf0a-126">Gibt die Anzahl der aufeinanderfolgenden Instanzfehler für eine Instanz an, die als fehlerhaft angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="eaf0a-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="eaf0a-127">-Protocol</span></span>
<span data-ttu-id="eaf0a-128">Gibt das Protokoll an, das für die Bedenkzeit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="eaf0a-129">Die zulässigen Werte für diesen Parameter sind: Tcp oder Http.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="eaf0a-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="eaf0a-130">-RequestPath</span></span>
<span data-ttu-id="eaf0a-131">Gibt den Pfad im Dienst mit Lastenausgleich an, um die Integrität zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="eaf0a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eaf0a-132">-Confirm</span></span>
<span data-ttu-id="eaf0a-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaf0a-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="eaf0a-134">-WhatIf</span></span>
<span data-ttu-id="eaf0a-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eaf0a-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaf0a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf0a-137">CommonParameters</span></span>
<span data-ttu-id="eaf0a-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaf0a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf0a-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaf0a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf0a-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eaf0a-140">INPUTS</span></span>

### <span data-ttu-id="eaf0a-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eaf0a-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="eaf0a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="eaf0a-142">System.String</span></span>

### <span data-ttu-id="eaf0a-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="eaf0a-143">System.Int32</span></span>

## <span data-ttu-id="eaf0a-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eaf0a-144">OUTPUTS</span></span>

### <span data-ttu-id="eaf0a-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eaf0a-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="eaf0a-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eaf0a-146">NOTES</span></span>

## <span data-ttu-id="eaf0a-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eaf0a-147">RELATED LINKS</span></span>

[<span data-ttu-id="eaf0a-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eaf0a-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="eaf0a-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eaf0a-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="eaf0a-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eaf0a-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="eaf0a-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eaf0a-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="eaf0a-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eaf0a-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


