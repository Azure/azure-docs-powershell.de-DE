---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 475a85353e4731a1bdb8f95a88328ffa27f99cb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821208"
---
# <span data-ttu-id="e5ac8-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e5ac8-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="e5ac8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ac8-103">Aktualisiert eine Prüf Punkt Konfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="e5ac8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5ac8-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5ac8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5ac8-105">DESCRIPTION</span></span>
<span data-ttu-id="e5ac8-106">Das Cmdlet " **Satz-AzLoadBalancerProbeConfig** " aktualisiert eine Prüf Punkt Konfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="e5ac8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5ac8-107">EXAMPLES</span></span>

### <span data-ttu-id="e5ac8-108">Beispiel 1: Ändern der Prüf Punkt Konfiguration auf einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="e5ac8-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="e5ac8-109">Der erste Befehl ruft den LoadBalancer mit dem Namen MyLoadBalancer ab und speichert ihn dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="e5ac8-110">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzLoadBalancerProbeConfig zu übergeben, wodurch eine neue Prüf Punkt Konfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="e5ac8-111">Der dritte Befehl übergibt das Load Balancer an **Set-AzLoadBalancerProbeConfig** , wodurch die neue Konfiguration festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="e5ac8-112">Beachten Sie, dass mehrere der gleichen Parameter angegeben werden müssen, die im vorherigen Befehl angegeben wurden, da Sie für das aktuelle Cmdlet erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="e5ac8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5ac8-113">PARAMETERS</span></span>

### <span data-ttu-id="e5ac8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ac8-114">-DefaultProfile</span></span>
<span data-ttu-id="e5ac8-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5ac8-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e5ac8-116">-IntervalInSeconds</span></span>
<span data-ttu-id="e5ac8-117">Gibt das Intervall in Sekunden zwischen Prüfpunkten für jede Instanz des Lastenausgleichsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="e5ac8-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5ac8-118">-LoadBalancer</span></span>
<span data-ttu-id="e5ac8-119">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-119">Specifies a load balancer.</span></span>
<span data-ttu-id="e5ac8-120">Dieses Cmdlet aktualisiert eine Prüf Punkt Konfiguration für das Load Balancer, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5ac8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e5ac8-121">-Name</span></span>
<span data-ttu-id="e5ac8-122">Gibt den Namen der Prüf Punkt Konfiguration an, die dieses Cmdlet festlegt.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="e5ac8-123">-Port</span><span class="sxs-lookup"><span data-stu-id="e5ac8-123">-Port</span></span>
<span data-ttu-id="e5ac8-124">Gibt den Port an, an dem die Sonden mit einem Dienst mit Lastenausgleich verbunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="e5ac8-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="e5ac8-125">-ProbeCount</span></span>
<span data-ttu-id="e5ac8-126">Gibt an, wie viele aufeinanderfolgende Fehler pro Instanz auftreten, damit eine Instanz als unschädlich eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="e5ac8-127">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e5ac8-127">-Protocol</span></span>
<span data-ttu-id="e5ac8-128">Gibt das für die Sondierung zu verwendende Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="e5ac8-129">Die zulässigen Werte für diesen Parameter lauten: TCP oder http.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="e5ac8-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="e5ac8-130">-RequestPath</span></span>
<span data-ttu-id="e5ac8-131">Gibt den Pfad im Lastenausgleichsdienst an, der zum Ermitteln der Integrität überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="e5ac8-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5ac8-132">-Confirm</span></span>
<span data-ttu-id="e5ac8-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5ac8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5ac8-134">-WhatIf</span></span>
<span data-ttu-id="e5ac8-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5ac8-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5ac8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ac8-137">CommonParameters</span></span>
<span data-ttu-id="e5ac8-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5ac8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ac8-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5ac8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ac8-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5ac8-140">INPUTS</span></span>

### <span data-ttu-id="e5ac8-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5ac8-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="e5ac8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e5ac8-142">System.String</span></span>

### <span data-ttu-id="e5ac8-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e5ac8-143">System.Int32</span></span>

## <span data-ttu-id="e5ac8-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5ac8-144">OUTPUTS</span></span>

### <span data-ttu-id="e5ac8-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5ac8-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e5ac8-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5ac8-146">NOTES</span></span>

## <span data-ttu-id="e5ac8-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5ac8-147">RELATED LINKS</span></span>

[<span data-ttu-id="e5ac8-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e5ac8-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e5ac8-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e5ac8-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e5ac8-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e5ac8-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e5ac8-151">Neu – AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e5ac8-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e5ac8-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e5ac8-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


