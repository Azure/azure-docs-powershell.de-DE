---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: aa71a338dadbbaa4dc12d490b259b3e358dc4a6c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995730"
---
# <span data-ttu-id="75530-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75530-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="75530-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75530-102">SYNOPSIS</span></span>
<span data-ttu-id="75530-103">Fügt eine Prüf Punkt Konfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="75530-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="75530-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75530-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75530-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75530-105">DESCRIPTION</span></span>
<span data-ttu-id="75530-106">Das Cmdlet **Add-AzLoadBalancerProbeConfig** fügt eine Prüf Punkt Konfiguration zu einem Azure-Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="75530-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="75530-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75530-107">EXAMPLES</span></span>

### <span data-ttu-id="75530-108">Beispiel 1 Hinzufügen einer Prüf Punkt Konfiguration zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="75530-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="75530-109">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen myLb ab, fügt die angegebene Prüf Punkt Konfiguration hinzu und verwendet dann das Cmdlet " **Satz-AzLoadBalancer** ", um das Lastenausgleichsmodul zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="75530-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="75530-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="75530-110">PARAMETERS</span></span>

### <span data-ttu-id="75530-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75530-111">-DefaultProfile</span></span>
<span data-ttu-id="75530-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75530-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75530-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="75530-113">-IntervalInSeconds</span></span>
<span data-ttu-id="75530-114">Gibt das Intervall in Sekunden zwischen Prüfpunkten für jede Instanz des Lastenausgleichsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="75530-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="75530-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75530-115">-LoadBalancer</span></span>
<span data-ttu-id="75530-116">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="75530-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="75530-117">Dieses Cmdlet fügt dem Load Balancer eine Prüf Punkt Konfiguration hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="75530-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="75530-118">-Name</span><span class="sxs-lookup"><span data-stu-id="75530-118">-Name</span></span>
<span data-ttu-id="75530-119">Gibt den Namen der zu hinzuzufügenden Prüf Punkt Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="75530-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="75530-120">-Port</span><span class="sxs-lookup"><span data-stu-id="75530-120">-Port</span></span>
<span data-ttu-id="75530-121">Gibt den Port an, an dem die Sonden mit einem Dienst mit Lastenausgleich verbunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="75530-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="75530-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="75530-122">-ProbeCount</span></span>
<span data-ttu-id="75530-123">Gibt an, wie viele aufeinanderfolgende Fehler pro Instanz auftreten, damit eine Instanz als unschädlich eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="75530-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="75530-124">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="75530-124">-Protocol</span></span>
<span data-ttu-id="75530-125">Gibt das für den Prüfpunkt zu verwendende Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="75530-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="75530-126">Die zulässigen Werte für diesen Parameter lauten: TCP oder http.</span><span class="sxs-lookup"><span data-stu-id="75530-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="75530-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="75530-127">-RequestPath</span></span>
<span data-ttu-id="75530-128">Gibt den Pfad im Lastenausgleichsdienst an, der zum Ermitteln der Integrität überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="75530-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="75530-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75530-129">-Confirm</span></span>
<span data-ttu-id="75530-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75530-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75530-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75530-131">-WhatIf</span></span>
<span data-ttu-id="75530-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75530-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75530-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75530-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75530-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75530-134">CommonParameters</span></span>
<span data-ttu-id="75530-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75530-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75530-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75530-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75530-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75530-137">INPUTS</span></span>

### <span data-ttu-id="75530-138">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75530-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="75530-139">System. String</span><span class="sxs-lookup"><span data-stu-id="75530-139">System.String</span></span>

### <span data-ttu-id="75530-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="75530-140">System.Int32</span></span>

## <span data-ttu-id="75530-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75530-141">OUTPUTS</span></span>

### <span data-ttu-id="75530-142">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75530-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="75530-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="75530-143">NOTES</span></span>

## <span data-ttu-id="75530-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75530-144">RELATED LINKS</span></span>

[<span data-ttu-id="75530-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75530-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="75530-146">Neu – AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75530-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="75530-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75530-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="75530-148">Satz-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75530-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="75530-149">Satz-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75530-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


