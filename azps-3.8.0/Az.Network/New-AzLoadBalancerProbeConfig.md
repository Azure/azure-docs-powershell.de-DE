---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 60c54895d4bff7f8825964b32c96e2d3c8b69798
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845236"
---
# <span data-ttu-id="5cdc4-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5cdc4-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="5cdc4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5cdc4-102">SYNOPSIS</span></span>
<span data-ttu-id="5cdc4-103">Erstellt eine Prüf Punkt Konfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="5cdc4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cdc4-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5cdc4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cdc4-105">DESCRIPTION</span></span>
<span data-ttu-id="5cdc4-106">Das Cmdlet **New-AzLoadBalancerProbeConfig** erstellt eine Prüf Punkt Konfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="5cdc4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5cdc4-107">EXAMPLES</span></span>

### <span data-ttu-id="5cdc4-108">Beispiel 1: Erstellen einer Prüf Punkt Konfiguration</span><span class="sxs-lookup"><span data-stu-id="5cdc4-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="5cdc4-109">Mit diesem Befehl wird eine Prüf Punkt Konfiguration mit dem Namen myprobe mithilfe des HTTP-Protokolls erstellt.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="5cdc4-110">Der neue Prüfpunkt stellt eine Verbindung mit einem Lastenausgleichsdienst auf Port 80 her.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="5cdc4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cdc4-111">PARAMETERS</span></span>

### <span data-ttu-id="5cdc4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cdc4-112">-DefaultProfile</span></span>
<span data-ttu-id="5cdc4-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cdc4-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5cdc4-114">-IntervalInSeconds</span></span>
<span data-ttu-id="5cdc4-115">Gibt das Intervall in Sekunden zwischen Prüfpunkten für jede Instanz eines Lastenausgleichsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="5cdc4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5cdc4-116">-Name</span></span>
<span data-ttu-id="5cdc4-117">Gibt den Namen der zu erstellende Prüf Punkt Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="5cdc4-118">-Port</span><span class="sxs-lookup"><span data-stu-id="5cdc4-118">-Port</span></span>
<span data-ttu-id="5cdc4-119">Gibt den Port an, an dem der neue Prüfpunkt eine Verbindung mit einem Lastenausgleichsdienst herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="5cdc4-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="5cdc4-120">-ProbeCount</span></span>
<span data-ttu-id="5cdc4-121">Gibt an, wie viele aufeinanderfolgende Fehler pro Instanz auftreten, damit eine Instanz als unschädlich eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="5cdc4-122">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="5cdc4-122">-Protocol</span></span>
<span data-ttu-id="5cdc4-123">Gibt das für die Prüf Punkt Konfiguration zu verwendende Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="5cdc4-124">Die zulässigen Werte für diesen Parameter lauten: TCP oder http.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="5cdc4-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="5cdc4-125">-RequestPath</span></span>
<span data-ttu-id="5cdc4-126">Gibt den Pfad in einem Lastenausgleichsdienst an, der zum Ermitteln der Integrität überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="5cdc4-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5cdc4-127">-Confirm</span></span>
<span data-ttu-id="5cdc4-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cdc4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cdc4-129">-WhatIf</span></span>
<span data-ttu-id="5cdc4-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cdc4-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cdc4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cdc4-132">CommonParameters</span></span>
<span data-ttu-id="5cdc4-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cdc4-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cdc4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cdc4-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5cdc4-135">INPUTS</span></span>

### <span data-ttu-id="5cdc4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5cdc4-136">System.String</span></span>

### <span data-ttu-id="5cdc4-137">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5cdc4-137">System.Int32</span></span>

## <span data-ttu-id="5cdc4-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5cdc4-138">OUTPUTS</span></span>

### <span data-ttu-id="5cdc4-139">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="5cdc4-139">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="5cdc4-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="5cdc4-140">NOTES</span></span>

## <span data-ttu-id="5cdc4-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5cdc4-141">RELATED LINKS</span></span>

[<span data-ttu-id="5cdc4-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5cdc4-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5cdc4-143">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5cdc4-143">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5cdc4-144">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5cdc4-144">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5cdc4-145">Satz-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5cdc4-145">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


