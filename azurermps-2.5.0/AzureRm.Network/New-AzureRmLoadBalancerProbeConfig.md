---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: f1d5ac87cc237e5a8ec92262255e996741346613
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850667"
---
# <span data-ttu-id="43b21-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="43b21-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="43b21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43b21-102">SYNOPSIS</span></span>
<span data-ttu-id="43b21-103">Erstellt eine Prüf Punkt Konfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="43b21-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43b21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43b21-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43b21-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43b21-105">DESCRIPTION</span></span>
<span data-ttu-id="43b21-106">Das Cmdlet **New-AzureRmLoadBalancerProbeConfig** erstellt eine Prüf Punkt Konfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="43b21-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="43b21-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43b21-107">EXAMPLES</span></span>

### <span data-ttu-id="43b21-108">Beispiel 1: Erstellen einer Prüf Punkt Konfiguration</span><span class="sxs-lookup"><span data-stu-id="43b21-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="43b21-109">Mit diesem Befehl wird eine Prüf Punkt Konfiguration mit dem Namen myprobe mithilfe des HTTP-Protokolls erstellt.</span><span class="sxs-lookup"><span data-stu-id="43b21-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="43b21-110">Der neue Prüfpunkt stellt eine Verbindung mit einem Lastenausgleichsdienst auf Port 80 her.</span><span class="sxs-lookup"><span data-stu-id="43b21-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="43b21-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="43b21-111">PARAMETERS</span></span>

### <span data-ttu-id="43b21-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b21-112">-DefaultProfile</span></span>
<span data-ttu-id="43b21-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43b21-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43b21-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="43b21-114">-IntervalInSeconds</span></span>
<span data-ttu-id="43b21-115">Gibt das Intervall in Sekunden zwischen Prüfpunkten für jede Instanz eines Lastenausgleichsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="43b21-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="43b21-116">-Name</span><span class="sxs-lookup"><span data-stu-id="43b21-116">-Name</span></span>
<span data-ttu-id="43b21-117">Gibt den Namen der zu erstellende Prüf Punkt Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="43b21-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="43b21-118">-Port</span><span class="sxs-lookup"><span data-stu-id="43b21-118">-Port</span></span>
<span data-ttu-id="43b21-119">Gibt den Port an, an dem der neue Prüfpunkt eine Verbindung mit einem Lastenausgleichsdienst herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="43b21-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="43b21-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="43b21-120">-ProbeCount</span></span>
<span data-ttu-id="43b21-121">Gibt an, wie viele aufeinanderfolgende Fehler pro Instanz auftreten, damit eine Instanz als unschädlich eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="43b21-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="43b21-122">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="43b21-122">-Protocol</span></span>
<span data-ttu-id="43b21-123">Gibt das für die Prüf Punkt Konfiguration zu verwendende Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="43b21-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="43b21-124">Die zulässigen Werte für diesen Parameter lauten: TCP oder http.</span><span class="sxs-lookup"><span data-stu-id="43b21-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="43b21-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="43b21-125">-RequestPath</span></span>
<span data-ttu-id="43b21-126">Gibt den Pfad in einem Lastenausgleichsdienst an, der zum Ermitteln der Integrität überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="43b21-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="43b21-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b21-127">CommonParameters</span></span>
<span data-ttu-id="43b21-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43b21-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b21-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43b21-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b21-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43b21-130">INPUTS</span></span>

## <span data-ttu-id="43b21-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43b21-131">OUTPUTS</span></span>

### <span data-ttu-id="43b21-132">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="43b21-132">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="43b21-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="43b21-133">NOTES</span></span>

## <span data-ttu-id="43b21-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43b21-134">RELATED LINKS</span></span>

[<span data-ttu-id="43b21-135">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="43b21-135">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="43b21-136">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="43b21-136">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="43b21-137">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="43b21-137">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="43b21-138">Satz-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="43b21-138">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


