---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a4889190e58edd896d1a93222a35688dd5884c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495902"
---
# <span data-ttu-id="22ea1-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22ea1-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="22ea1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="22ea1-103">Erstellt eine Prüf Punkt Konfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="22ea1-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22ea1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22ea1-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22ea1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22ea1-105">DESCRIPTION</span></span>
<span data-ttu-id="22ea1-106">Das Cmdlet **New-AzureRmLoadBalancerProbeConfig** erstellt eine Prüf Punkt Konfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="22ea1-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="22ea1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22ea1-107">EXAMPLES</span></span>

### <span data-ttu-id="22ea1-108">Beispiel 1: Erstellen einer Prüf Punkt Konfiguration</span><span class="sxs-lookup"><span data-stu-id="22ea1-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="22ea1-109">Mit diesem Befehl wird eine Prüf Punkt Konfiguration mit dem Namen myprobe mithilfe des HTTP-Protokolls erstellt.</span><span class="sxs-lookup"><span data-stu-id="22ea1-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="22ea1-110">Der neue Prüfpunkt stellt eine Verbindung mit einem Lastenausgleichsdienst auf Port 80 her.</span><span class="sxs-lookup"><span data-stu-id="22ea1-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="22ea1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="22ea1-111">PARAMETERS</span></span>

### <span data-ttu-id="22ea1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ea1-112">-DefaultProfile</span></span>
<span data-ttu-id="22ea1-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="22ea1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22ea1-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="22ea1-114">-IntervalInSeconds</span></span>
<span data-ttu-id="22ea1-115">Gibt das Intervall in Sekunden zwischen Prüfpunkten für jede Instanz eines Lastenausgleichsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="22ea1-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="22ea1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="22ea1-116">-Name</span></span>
<span data-ttu-id="22ea1-117">Gibt den Namen der zu erstellende Prüf Punkt Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="22ea1-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="22ea1-118">-Port</span><span class="sxs-lookup"><span data-stu-id="22ea1-118">-Port</span></span>
<span data-ttu-id="22ea1-119">Gibt den Port an, an dem der neue Prüfpunkt eine Verbindung mit einem Lastenausgleichsdienst herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="22ea1-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="22ea1-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="22ea1-120">-ProbeCount</span></span>
<span data-ttu-id="22ea1-121">Gibt an, wie viele aufeinanderfolgende Fehler pro Instanz auftreten, damit eine Instanz als unschädlich eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="22ea1-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="22ea1-122">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="22ea1-122">-Protocol</span></span>
<span data-ttu-id="22ea1-123">Gibt das für die Prüf Punkt Konfiguration zu verwendende Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="22ea1-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="22ea1-124">Die zulässigen Werte für diesen Parameter lauten: TCP oder http.</span><span class="sxs-lookup"><span data-stu-id="22ea1-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="22ea1-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="22ea1-125">-RequestPath</span></span>
<span data-ttu-id="22ea1-126">Gibt den Pfad in einem Lastenausgleichsdienst an, der zum Ermitteln der Integrität überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="22ea1-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="22ea1-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="22ea1-127">-Confirm</span></span>
<span data-ttu-id="22ea1-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22ea1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22ea1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22ea1-129">-WhatIf</span></span>
<span data-ttu-id="22ea1-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22ea1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22ea1-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22ea1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22ea1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ea1-132">CommonParameters</span></span>
<span data-ttu-id="22ea1-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ea1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ea1-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22ea1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ea1-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22ea1-135">INPUTS</span></span>

### <span data-ttu-id="22ea1-136">Keine</span><span class="sxs-lookup"><span data-stu-id="22ea1-136">None</span></span>

## <span data-ttu-id="22ea1-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22ea1-137">OUTPUTS</span></span>

### <span data-ttu-id="22ea1-138">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="22ea1-138">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="22ea1-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="22ea1-139">NOTES</span></span>

## <span data-ttu-id="22ea1-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22ea1-140">RELATED LINKS</span></span>

[<span data-ttu-id="22ea1-141">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22ea1-141">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="22ea1-142">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22ea1-142">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="22ea1-143">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22ea1-143">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="22ea1-144">Satz-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22ea1-144">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


