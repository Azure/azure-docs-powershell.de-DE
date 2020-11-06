---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: d8b7c83ff2804de3e60af7c5ea8ce9f3e2d1eb97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501857"
---
# <span data-ttu-id="f9884-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="f9884-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="f9884-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9884-102">SYNOPSIS</span></span>
<span data-ttu-id="f9884-103">Ruft die metrischen Werte einer Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="f9884-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9884-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9884-104">SYNTAX</span></span>

### <span data-ttu-id="f9884-105">Parameter für Get-AzureRmMetric-Cmdlet im Standardmodus</span><span class="sxs-lookup"><span data-stu-id="f9884-105">Parameters for Get-AzureRmMetric cmdlet in the default mode</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-MetricNames <String[]>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9884-106">Parameter für Get-AzureRmMetric-Cmdlet im vollständigen Parame-Satzmodus</span><span class="sxs-lookup"><span data-stu-id="f9884-106">Parameters for Get-AzureRmMetric cmdlet in the full param set mode</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [[-TimeGrain] <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] -MetricNames <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9884-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9884-107">DESCRIPTION</span></span>
<span data-ttu-id="f9884-108">Das Cmdlet " **Get-AzureRmMetric** " Ruft die metrischen Werte für eine angegebene Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="f9884-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="f9884-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9884-109">EXAMPLES</span></span>

### <span data-ttu-id="f9884-110">Beispiel 1: Abrufen einer Metrik mit zusammengefasster Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f9884-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
DimensionName  : 
DimensionValue : 
Name           : AverageMemoryWorkingSet
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Bytes
```

<span data-ttu-id="f9884-111">Dieser Befehl ruft die metrischen Werte für website3 mit einer Zeit Körnung von 1 Minute ab.</span><span class="sxs-lookup"><span data-stu-id="f9884-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="f9884-112">Beispiel 2: Abrufen einer Metrik mit einer detaillierten Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f9884-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:37:00 PM
                     Total      : 0
                     Average    : 0.106
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 0.106
                     Average    : 0.064
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 0.064
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:43:33 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:43:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
```

<span data-ttu-id="f9884-113">Dieser Befehl ruft die metrischen Werte für website3 mit einer Zeit Körnung von 1 Minute ab.</span><span class="sxs-lookup"><span data-stu-id="f9884-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="f9884-114">Die Ausgabe ist detailliert.</span><span class="sxs-lookup"><span data-stu-id="f9884-114">The output is detailed.</span></span>

### <span data-ttu-id="f9884-115">Beispiel 3: Abrufen der detaillierten Ausgabe für eine angegebene Metrik</span><span class="sxs-lookup"><span data-stu-id="f9884-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput -MetricNames "Requests"
MetricValues   : 
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 1
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:43:00 PM
                     Total      : 0
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:44:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:45:00 PM
                     Total      : 0
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : Requests
EndTime        : 3/20/2015 6:47:56 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:47:00 PM
TimeGrain      : 00:01:00
Unit           : Count
```

<span data-ttu-id="f9884-116">Dieser Befehl ruft eine detaillierte Ausgabe für die Anforderungs Metrik ab.</span><span class="sxs-lookup"><span data-stu-id="f9884-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="f9884-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9884-117">PARAMETERS</span></span>

### <span data-ttu-id="f9884-118">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="f9884-118">-DetailedOutput</span></span>
<span data-ttu-id="f9884-119">Gibt an, dass dieses Cmdlet eine detaillierte Ausgabe anzeigt.</span><span class="sxs-lookup"><span data-stu-id="f9884-119">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="f9884-120">Standardmäßig wird die Ausgabe zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="f9884-120">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9884-121">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f9884-121">-EndTime</span></span>
<span data-ttu-id="f9884-122">Gibt die Endzeit der Abfrage in Ortszeit an.</span><span class="sxs-lookup"><span data-stu-id="f9884-122">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="f9884-123">Der Standardwert ist die aktuelle Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="f9884-123">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9884-124">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="f9884-124">-MetricNames</span></span>
<span data-ttu-id="f9884-125">Gibt ein Array mit Namen von Metriken an.</span><span class="sxs-lookup"><span data-stu-id="f9884-125">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the default mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9884-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f9884-126">-ResourceId</span></span>
<span data-ttu-id="f9884-127">Gibt die Ressourcen-ID der Metrik an.</span><span class="sxs-lookup"><span data-stu-id="f9884-127">Specifies the resource ID of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9884-128">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="f9884-128">-StartTime</span></span>
<span data-ttu-id="f9884-129">Gibt die Startzeit der Abfrage in Ortszeit an.</span><span class="sxs-lookup"><span data-stu-id="f9884-129">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="f9884-130">Der Standardwert ist die aktuelle Ortszeit minus 1 Stunde.</span><span class="sxs-lookup"><span data-stu-id="f9884-130">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9884-131">-Zeitkorn</span><span class="sxs-lookup"><span data-stu-id="f9884-131">-TimeGrain</span></span>
<span data-ttu-id="f9884-132">Gibt die Zeit Körnung der Metrik als **TimeSpan** -Objekt im Format hh: mm: SS an.</span><span class="sxs-lookup"><span data-stu-id="f9884-132">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9884-133">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="f9884-133">-AggregationType</span></span>
<span data-ttu-id="f9884-134">Der Aggregations des quer</span><span class="sxs-lookup"><span data-stu-id="f9884-134">The aggregation type of the quer</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9884-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9884-135">-DefaultProfile</span></span>
<span data-ttu-id="f9884-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9884-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9884-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9884-137">CommonParameters</span></span>
<span data-ttu-id="f9884-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9884-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9884-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9884-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9884-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9884-140">INPUTS</span></span>

## <span data-ttu-id="f9884-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9884-141">OUTPUTS</span></span>

### <span data-ttu-id="f9884-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric []</span><span class="sxs-lookup"><span data-stu-id="f9884-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="f9884-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9884-143">NOTES</span></span>

## <span data-ttu-id="f9884-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9884-144">RELATED LINKS</span></span>

[<span data-ttu-id="f9884-145">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="f9884-145">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


