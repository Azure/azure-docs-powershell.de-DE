---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 57c0d491d5e330f45550381b099e20e5d02fd8f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663894"
---
# <span data-ttu-id="ac883-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ac883-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="ac883-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac883-102">SYNOPSIS</span></span>
<span data-ttu-id="ac883-103">Erstellt eine Prüf Punkt Konfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="ac883-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac883-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac883-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac883-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac883-105">DESCRIPTION</span></span>
<span data-ttu-id="ac883-106">Das Cmdlet **New-AzureRmLoadBalancerProbeConfig** erstellt eine Prüf Punkt Konfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="ac883-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ac883-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac883-107">EXAMPLES</span></span>

### <span data-ttu-id="ac883-108">Beispiel 1: Erstellen einer Prüf Punkt Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ac883-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="ac883-109">Mit diesem Befehl wird eine Prüf Punkt Konfiguration mit dem Namen myprobe mithilfe des HTTP-Protokolls erstellt.</span><span class="sxs-lookup"><span data-stu-id="ac883-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="ac883-110">Der neue Prüfpunkt stellt eine Verbindung mit einem Lastenausgleichsdienst auf Port 80 her.</span><span class="sxs-lookup"><span data-stu-id="ac883-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="ac883-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac883-111">PARAMETERS</span></span>

### <span data-ttu-id="ac883-112">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ac883-112">-IntervalInSeconds</span></span>
<span data-ttu-id="ac883-113">Gibt das Intervall in Sekunden zwischen Prüfpunkten für jede Instanz eines Lastenausgleichsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="ac883-113">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac883-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ac883-114">-Name</span></span>
<span data-ttu-id="ac883-115">Gibt den Namen der zu erstellende Prüf Punkt Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="ac883-115">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="ac883-116">-Port</span><span class="sxs-lookup"><span data-stu-id="ac883-116">-Port</span></span>
<span data-ttu-id="ac883-117">Gibt den Port an, an dem der neue Prüfpunkt eine Verbindung mit einem Lastenausgleichsdienst herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="ac883-117">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac883-118">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="ac883-118">-ProbeCount</span></span>
<span data-ttu-id="ac883-119">Gibt an, wie viele aufeinanderfolgende Fehler pro Instanz auftreten, damit eine Instanz als unschädlich eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="ac883-119">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac883-120">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ac883-120">-Protocol</span></span>
<span data-ttu-id="ac883-121">Gibt das für die Prüf Punkt Konfiguration zu verwendende Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="ac883-121">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="ac883-122">Die zulässigen Werte für diesen Parameter lauten: TCP oder http.</span><span class="sxs-lookup"><span data-stu-id="ac883-122">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac883-123">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="ac883-123">-RequestPath</span></span>
<span data-ttu-id="ac883-124">Gibt den Pfad in einem Lastenausgleichsdienst an, der zum Ermitteln der Integrität überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac883-124">Specifies the path in a load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac883-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac883-125">-DefaultProfile</span></span>
<span data-ttu-id="ac883-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac883-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac883-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac883-127">CommonParameters</span></span>
<span data-ttu-id="ac883-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac883-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac883-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac883-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac883-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac883-130">INPUTS</span></span>

## <span data-ttu-id="ac883-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac883-131">OUTPUTS</span></span>

### <span data-ttu-id="ac883-132">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="ac883-132">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="ac883-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac883-133">NOTES</span></span>

## <span data-ttu-id="ac883-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac883-134">RELATED LINKS</span></span>

[<span data-ttu-id="ac883-135">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ac883-135">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ac883-136">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ac883-136">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ac883-137">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ac883-137">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ac883-138">Satz-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ac883-138">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


