---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 3fe5345e6d3cbad90d99f5a94e72873beaca7c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663000"
---
# <span data-ttu-id="32e85-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="32e85-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="32e85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32e85-102">SYNOPSIS</span></span>
<span data-ttu-id="32e85-103">Legt den Zielstatus für eine Prüf Punkt Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="32e85-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32e85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32e85-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32e85-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32e85-105">DESCRIPTION</span></span>
<span data-ttu-id="32e85-106">Das Cmdlet " **Set-AzureRmLoadBalancerProbeConfig** " legt den Zielstatus für eine Prüf Punkt Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="32e85-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="32e85-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32e85-107">EXAMPLES</span></span>

### <span data-ttu-id="32e85-108">Beispiel 1: Ändern der Prüf Punkt Konfiguration auf einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="32e85-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="32e85-109">Der erste Befehl ruft den LoadBalancer mit dem Namen MyLoadBalancer ab und speichert ihn dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="32e85-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="32e85-110">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzureRmLoadBalancerProbeConfig zu übergeben, wodurch eine neue Prüf Punkt Konfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="32e85-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="32e85-111">Der dritte Befehl übergibt das Load Balancer an **Set-AzureRmLoadBalancerProbeConfig** , wodurch die neue Konfiguration festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="32e85-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="32e85-112">Beachten Sie, dass mehrere der gleichen Parameter angegeben werden müssen, die im vorherigen Befehl angegeben wurden, da Sie für das aktuelle Cmdlet erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="32e85-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="32e85-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="32e85-113">PARAMETERS</span></span>

### <span data-ttu-id="32e85-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e85-114">-DefaultProfile</span></span>
<span data-ttu-id="32e85-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32e85-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32e85-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="32e85-116">-IntervalInSeconds</span></span>
<span data-ttu-id="32e85-117">Gibt das Intervall in Sekunden zwischen Prüfpunkten für jede Instanz des Lastenausgleichsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="32e85-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="32e85-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="32e85-118">-LoadBalancer</span></span>
<span data-ttu-id="32e85-119">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="32e85-119">Specifies a load balancer.</span></span>
<span data-ttu-id="32e85-120">Mit diesem Cmdlet wird der Zielstatus für eine Prüf Punkt Konfiguration für das Load Balancer festgelegt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="32e85-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="32e85-121">-Name</span><span class="sxs-lookup"><span data-stu-id="32e85-121">-Name</span></span>
<span data-ttu-id="32e85-122">Gibt den Namen der Prüf Punkt Konfiguration an, die dieses Cmdlet festlegt.</span><span class="sxs-lookup"><span data-stu-id="32e85-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="32e85-123">-Port</span><span class="sxs-lookup"><span data-stu-id="32e85-123">-Port</span></span>
<span data-ttu-id="32e85-124">Gibt den Port an, an dem die Sonden mit einem Dienst mit Lastenausgleich verbunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="32e85-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="32e85-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="32e85-125">-ProbeCount</span></span>
<span data-ttu-id="32e85-126">Gibt an, wie viele aufeinanderfolgende Fehler pro Instanz auftreten, damit eine Instanz als unschädlich eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="32e85-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="32e85-127">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="32e85-127">-Protocol</span></span>
<span data-ttu-id="32e85-128">Gibt das für die Sondierung zu verwendende Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="32e85-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="32e85-129">Die zulässigen Werte für diesen Parameter lauten: TCP oder http.</span><span class="sxs-lookup"><span data-stu-id="32e85-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="32e85-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="32e85-130">-RequestPath</span></span>
<span data-ttu-id="32e85-131">Gibt den Pfad im Lastenausgleichsdienst an, der zum Ermitteln der Integrität überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="32e85-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="32e85-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="32e85-132">-Confirm</span></span>
<span data-ttu-id="32e85-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="32e85-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32e85-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32e85-134">-WhatIf</span></span>
<span data-ttu-id="32e85-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32e85-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32e85-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32e85-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32e85-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e85-137">CommonParameters</span></span>
<span data-ttu-id="32e85-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32e85-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e85-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e85-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e85-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32e85-140">INPUTS</span></span>

### <span data-ttu-id="32e85-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="32e85-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="32e85-142">Parameter: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="32e85-142">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="32e85-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32e85-143">OUTPUTS</span></span>

### <span data-ttu-id="32e85-144">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="32e85-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="32e85-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="32e85-145">NOTES</span></span>

## <span data-ttu-id="32e85-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32e85-146">RELATED LINKS</span></span>

[<span data-ttu-id="32e85-147">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="32e85-147">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="32e85-148">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="32e85-148">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="32e85-149">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="32e85-149">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="32e85-150">Neu – AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="32e85-150">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="32e85-151">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="32e85-151">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


