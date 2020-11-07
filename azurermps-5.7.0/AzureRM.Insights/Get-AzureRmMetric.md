---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: 63ade199b63e57cc72e965002942773f47214494
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662470"
---
# <span data-ttu-id="37559-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="37559-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="37559-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37559-102">SYNOPSIS</span></span>
<span data-ttu-id="37559-103">Ruft die metrischen Werte einer Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="37559-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37559-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37559-104">SYNTAX</span></span>

### <span data-ttu-id="37559-105">GetWithDefaultParameters</span><span class="sxs-lookup"><span data-stu-id="37559-105">GetWithDefaultParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37559-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="37559-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37559-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37559-107">DESCRIPTION</span></span>
<span data-ttu-id="37559-108">Das Cmdlet " **Get-AzureRmMetric** " Ruft die metrischen Werte für eine angegebene Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="37559-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="37559-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37559-109">EXAMPLES</span></span>

### <span data-ttu-id="37559-110">Beispiel 1: Abrufen einer Metrik mit zusammengefasster Ausgabe</span><span class="sxs-lookup"><span data-stu-id="37559-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="37559-111">Dieser Befehl ruft die metrischen Werte für website3 mit einer Zeit Körnung von 1 Minute ab.</span><span class="sxs-lookup"><span data-stu-id="37559-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="37559-112">Beispiel 2: Abrufen einer Metrik mit einer detaillierten Ausgabe</span><span class="sxs-lookup"><span data-stu-id="37559-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="37559-113">Dieser Befehl ruft die metrischen Werte für website3 mit einer Zeit Körnung von 1 Minute ab.</span><span class="sxs-lookup"><span data-stu-id="37559-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="37559-114">Die Ausgabe ist detailliert.</span><span class="sxs-lookup"><span data-stu-id="37559-114">The output is detailed.</span></span>

### <span data-ttu-id="37559-115">Beispiel 3: Abrufen der detaillierten Ausgabe für eine angegebene Metrik</span><span class="sxs-lookup"><span data-stu-id="37559-115">Example 3: Get detailed output for a specified metric</span></span>
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

<span data-ttu-id="37559-116">Dieser Befehl ruft eine detaillierte Ausgabe für die Anforderungs Metrik ab.</span><span class="sxs-lookup"><span data-stu-id="37559-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="37559-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="37559-117">PARAMETERS</span></span>

### <span data-ttu-id="37559-118">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="37559-118">-AggregationType</span></span>
<span data-ttu-id="37559-119">Der Aggregations der Abfrage</span><span class="sxs-lookup"><span data-stu-id="37559-119">The aggregation type of the query</span></span>

```yaml
Type: AggregationType
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37559-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37559-120">-DefaultProfile</span></span>
<span data-ttu-id="37559-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37559-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37559-122">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="37559-122">-DetailedOutput</span></span>
<span data-ttu-id="37559-123">Gibt an, dass dieses Cmdlet eine detaillierte Ausgabe anzeigt.</span><span class="sxs-lookup"><span data-stu-id="37559-123">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="37559-124">Standardmäßig wird die Ausgabe zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="37559-124">By default, output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37559-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="37559-125">-EndTime</span></span>
<span data-ttu-id="37559-126">Gibt die Endzeit der Abfrage in Ortszeit an.</span><span class="sxs-lookup"><span data-stu-id="37559-126">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="37559-127">Der Standardwert ist die aktuelle Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="37559-127">The default is the current time.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37559-128">-Metricname</span><span class="sxs-lookup"><span data-stu-id="37559-128">-MetricName</span></span>
<span data-ttu-id="37559-129">Gibt ein Array mit Namen von Metriken an.</span><span class="sxs-lookup"><span data-stu-id="37559-129">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False (GetWithDefaultParameters), True (GetAzureRmAMetricFullParamGroup)
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: GetWithFullParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37559-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="37559-130">-ResourceId</span></span>
<span data-ttu-id="37559-131">Gibt die Ressourcen-ID der Metrik an.</span><span class="sxs-lookup"><span data-stu-id="37559-131">Specifies the resource ID of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37559-132">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="37559-132">-StartTime</span></span>
<span data-ttu-id="37559-133">Gibt die Startzeit der Abfrage in Ortszeit an.</span><span class="sxs-lookup"><span data-stu-id="37559-133">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="37559-134">Der Standardwert ist die aktuelle Ortszeit minus 1 Stunde.</span><span class="sxs-lookup"><span data-stu-id="37559-134">The default is the current local time minus one hour.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37559-135">-Zeitkorn</span><span class="sxs-lookup"><span data-stu-id="37559-135">-TimeGrain</span></span>
<span data-ttu-id="37559-136">Gibt die Zeit Körnung der Metrik als **TimeSpan** -Objekt im Format hh: mm: SS an.</span><span class="sxs-lookup"><span data-stu-id="37559-136">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37559-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37559-137">CommonParameters</span></span>
<span data-ttu-id="37559-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37559-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37559-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37559-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37559-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37559-140">INPUTS</span></span>

### <span data-ttu-id="37559-141">Keine</span><span class="sxs-lookup"><span data-stu-id="37559-141">None</span></span>
<span data-ttu-id="37559-142">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="37559-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37559-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37559-143">OUTPUTS</span></span>

### <span data-ttu-id="37559-144">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric []</span><span class="sxs-lookup"><span data-stu-id="37559-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="37559-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="37559-145">NOTES</span></span>

## <span data-ttu-id="37559-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37559-146">RELATED LINKS</span></span>

[<span data-ttu-id="37559-147">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="37559-147">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


