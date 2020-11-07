---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a14196a98be2f901cc120926e716efe884a747a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843623"
---
# <span data-ttu-id="8dac3-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8dac3-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="8dac3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8dac3-102">SYNOPSIS</span></span>
<span data-ttu-id="8dac3-103">Legt den Zielstatus für eine Prüf Punkt Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="8dac3-103">Sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="8dac3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dac3-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dac3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8dac3-105">DESCRIPTION</span></span>
<span data-ttu-id="8dac3-106">Das Cmdlet " **Set-AzLoadBalancerProbeConfig** " legt den Zielstatus für eine Prüf Punkt Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="8dac3-106">The **Set-AzLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="8dac3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8dac3-107">EXAMPLES</span></span>

### <span data-ttu-id="8dac3-108">Beispiel 1: Ändern der Prüf Punkt Konfiguration auf einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="8dac3-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="8dac3-109">Der erste Befehl ruft den LoadBalancer mit dem Namen MyLoadBalancer ab und speichert ihn dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8dac3-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="8dac3-110">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzLoadBalancerProbeConfig zu übergeben, wodurch eine neue Prüf Punkt Konfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8dac3-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="8dac3-111">Der dritte Befehl übergibt das Load Balancer an **Set-AzLoadBalancerProbeConfig** , wodurch die neue Konfiguration festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8dac3-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="8dac3-112">Beachten Sie, dass mehrere der gleichen Parameter angegeben werden müssen, die im vorherigen Befehl angegeben wurden, da Sie für das aktuelle Cmdlet erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8dac3-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="8dac3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8dac3-113">PARAMETERS</span></span>

### <span data-ttu-id="8dac3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dac3-114">-DefaultProfile</span></span>
<span data-ttu-id="8dac3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8dac3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dac3-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8dac3-116">-IntervalInSeconds</span></span>
<span data-ttu-id="8dac3-117">Gibt das Intervall in Sekunden zwischen Prüfpunkten für jede Instanz des Lastenausgleichsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="8dac3-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dac3-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8dac3-118">-LoadBalancer</span></span>
<span data-ttu-id="8dac3-119">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="8dac3-119">Specifies a load balancer.</span></span>
<span data-ttu-id="8dac3-120">Mit diesem Cmdlet wird der Zielstatus für eine Prüf Punkt Konfiguration für das Load Balancer festgelegt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8dac3-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dac3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8dac3-121">-Name</span></span>
<span data-ttu-id="8dac3-122">Gibt den Namen der Prüf Punkt Konfiguration an, die dieses Cmdlet festlegt.</span><span class="sxs-lookup"><span data-stu-id="8dac3-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dac3-123">-Port</span><span class="sxs-lookup"><span data-stu-id="8dac3-123">-Port</span></span>
<span data-ttu-id="8dac3-124">Gibt den Port an, an dem die Sonden mit einem Dienst mit Lastenausgleich verbunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8dac3-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dac3-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="8dac3-125">-ProbeCount</span></span>
<span data-ttu-id="8dac3-126">Gibt an, wie viele aufeinanderfolgende Fehler pro Instanz auftreten, damit eine Instanz als unschädlich eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="8dac3-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dac3-127">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="8dac3-127">-Protocol</span></span>
<span data-ttu-id="8dac3-128">Gibt das für die Sondierung zu verwendende Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="8dac3-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="8dac3-129">Die zulässigen Werte für diesen Parameter lauten: TCP oder http.</span><span class="sxs-lookup"><span data-stu-id="8dac3-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dac3-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="8dac3-130">-RequestPath</span></span>
<span data-ttu-id="8dac3-131">Gibt den Pfad im Lastenausgleichsdienst an, der zum Ermitteln der Integrität überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="8dac3-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dac3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dac3-132">CommonParameters</span></span>
<span data-ttu-id="8dac3-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dac3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dac3-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dac3-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dac3-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8dac3-135">INPUTS</span></span>

### <span data-ttu-id="8dac3-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8dac3-136">PSLoadBalancer</span></span>
<span data-ttu-id="8dac3-137">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8dac3-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="8dac3-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8dac3-138">OUTPUTS</span></span>

### <span data-ttu-id="8dac3-139">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8dac3-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8dac3-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="8dac3-140">NOTES</span></span>

## <span data-ttu-id="8dac3-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8dac3-141">RELATED LINKS</span></span>

[<span data-ttu-id="8dac3-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8dac3-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="8dac3-143">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8dac3-143">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="8dac3-144">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8dac3-144">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="8dac3-145">Neu – AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8dac3-145">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="8dac3-146">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8dac3-146">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


