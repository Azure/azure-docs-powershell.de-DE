---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6bcf0957d389f45bb0e010446381303c6124146b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660525"
---
# <span data-ttu-id="9bce3-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9bce3-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="9bce3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9bce3-102">SYNOPSIS</span></span>
<span data-ttu-id="9bce3-103">Erstellt eine Prüf Punkt Konfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="9bce3-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="9bce3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bce3-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bce3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9bce3-105">DESCRIPTION</span></span>
<span data-ttu-id="9bce3-106">Das Cmdlet **New-AzLoadBalancerProbeConfig** erstellt eine Prüf Punkt Konfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="9bce3-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9bce3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9bce3-107">EXAMPLES</span></span>

### <span data-ttu-id="9bce3-108">Beispiel 1: Erstellen einer Prüf Punkt Konfiguration</span><span class="sxs-lookup"><span data-stu-id="9bce3-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="9bce3-109">Mit diesem Befehl wird eine Prüf Punkt Konfiguration mit dem Namen myprobe mithilfe des HTTP-Protokolls erstellt.</span><span class="sxs-lookup"><span data-stu-id="9bce3-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="9bce3-110">Der neue Prüfpunkt stellt eine Verbindung mit einem Lastenausgleichsdienst auf Port 80 her.</span><span class="sxs-lookup"><span data-stu-id="9bce3-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="9bce3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bce3-111">PARAMETERS</span></span>

### <span data-ttu-id="9bce3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bce3-112">-DefaultProfile</span></span>
<span data-ttu-id="9bce3-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9bce3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bce3-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9bce3-114">-IntervalInSeconds</span></span>
<span data-ttu-id="9bce3-115">Gibt das Intervall in Sekunden zwischen Prüfpunkten für jede Instanz eines Lastenausgleichsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="9bce3-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="9bce3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9bce3-116">-Name</span></span>
<span data-ttu-id="9bce3-117">Gibt den Namen der zu erstellende Prüf Punkt Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="9bce3-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="9bce3-118">-Port</span><span class="sxs-lookup"><span data-stu-id="9bce3-118">-Port</span></span>
<span data-ttu-id="9bce3-119">Gibt den Port an, an dem der neue Prüfpunkt eine Verbindung mit einem Lastenausgleichsdienst herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="9bce3-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="9bce3-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="9bce3-120">-ProbeCount</span></span>
<span data-ttu-id="9bce3-121">Gibt an, wie viele aufeinanderfolgende Fehler pro Instanz auftreten, damit eine Instanz als unschädlich eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="9bce3-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="9bce3-122">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="9bce3-122">-Protocol</span></span>
<span data-ttu-id="9bce3-123">Gibt das für die Prüf Punkt Konfiguration zu verwendende Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="9bce3-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="9bce3-124">Die zulässigen Werte für diesen Parameter lauten: TCP oder http.</span><span class="sxs-lookup"><span data-stu-id="9bce3-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="9bce3-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="9bce3-125">-RequestPath</span></span>
<span data-ttu-id="9bce3-126">Gibt den Pfad in einem Lastenausgleichsdienst an, der zum Ermitteln der Integrität überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="9bce3-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="9bce3-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9bce3-127">-Confirm</span></span>
<span data-ttu-id="9bce3-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9bce3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bce3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bce3-129">-WhatIf</span></span>
<span data-ttu-id="9bce3-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9bce3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bce3-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9bce3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bce3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bce3-132">CommonParameters</span></span>
<span data-ttu-id="9bce3-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bce3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bce3-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bce3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bce3-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9bce3-135">INPUTS</span></span>

### <span data-ttu-id="9bce3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9bce3-136">System.String</span></span>

### <span data-ttu-id="9bce3-137">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9bce3-137">System.Int32</span></span>

## <span data-ttu-id="9bce3-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9bce3-138">OUTPUTS</span></span>

### <span data-ttu-id="9bce3-139">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="9bce3-139">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="9bce3-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="9bce3-140">NOTES</span></span>

## <span data-ttu-id="9bce3-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9bce3-141">RELATED LINKS</span></span>

[<span data-ttu-id="9bce3-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9bce3-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9bce3-143">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9bce3-143">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9bce3-144">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9bce3-144">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9bce3-145">Satz-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9bce3-145">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


