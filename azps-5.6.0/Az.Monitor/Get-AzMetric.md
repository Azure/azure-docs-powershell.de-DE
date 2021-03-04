---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
ms.openlocfilehash: bb2301fceef993e131472e497e2c89e7ef6ecbf2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932592"
---
# <span data-ttu-id="fb038-101">Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="fb038-101">Get-AzMetric</span></span>

## <span data-ttu-id="fb038-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb038-102">SYNOPSIS</span></span>
<span data-ttu-id="fb038-103">Ruft die Metrikwerte einer Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="fb038-103">Gets the metric values of a resource.</span></span>

## <span data-ttu-id="fb038-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb038-104">SYNTAX</span></span>

### <span data-ttu-id="fb038-105">GetWithDefaultParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="fb038-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb038-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="fb038-106">GetWithFullParameters</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb038-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb038-107">DESCRIPTION</span></span>
<span data-ttu-id="fb038-108">Das **Get-AzMetric-Cmdlet** ruft die Metrikwerte für eine angegebene Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="fb038-108">The **Get-AzMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="fb038-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fb038-109">EXAMPLES</span></span>

### <span data-ttu-id="fb038-110">Beispiel 1: Erhalten einer Metrik mit zusammengefasster Ausgabe</span><span class="sxs-lookup"><span data-stu-id="fb038-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
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

<span data-ttu-id="fb038-111">Dieser Befehl ruft die Metrikwerte für website3 mit einer Zeitkörnung von 1 Minute ab.</span><span class="sxs-lookup"><span data-stu-id="fb038-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="fb038-112">Beispiel 2: Erhalten einer Metrik mit detaillierter Ausgabe</span><span class="sxs-lookup"><span data-stu-id="fb038-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="fb038-113">Dieser Befehl ruft die Metrikwerte für website3 mit einer Zeitkörnung von 1 Minute ab.</span><span class="sxs-lookup"><span data-stu-id="fb038-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="fb038-114">Die Ausgabe ist detailliert.</span><span class="sxs-lookup"><span data-stu-id="fb038-114">The output is detailed.</span></span>

### <span data-ttu-id="fb038-115">Beispiel 3: Erhalten einer detaillierten Ausgabe für eine angegebene Metrik</span><span class="sxs-lookup"><span data-stu-id="fb038-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricName "Requests" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="fb038-116">Dieser Befehl ruft eine detaillierte Ausgabe für die Metrik Anforderungen ab.</span><span class="sxs-lookup"><span data-stu-id="fb038-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="fb038-117">Beispiel 4: Zusammenfassung der Ausgabe für eine angegebene Metrik mit angegebenem Dimensionsfilter</span><span class="sxs-lookup"><span data-stu-id="fb038-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","Toronto"), (New-AzMetricFilter -Dimension AuthenticationType -Operator eq -Value User))

PS C:\> Get-AzMetric -ResourceId <resourceId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
ResourceId  : [ResourceId]
MetricNamespace : Microsoft.Insights/ApplicationInsights
Metric Name :
                    LocalizedValue  : Page Views
                    Value       : PageViews
Unit        : Seconds
Timeseries  :
            City            : Seattle
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 3518

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 1984

            City            : Toronto
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 894

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 967
```

<span data-ttu-id="fb038-118">Dieser Befehl ruft die Zusammenfassung der Ausgabe für die Metrik "PageViews" mit dem angegebenen Dimensionsfilter und Aggregationstyp ab.</span><span class="sxs-lookup"><span data-stu-id="fb038-118">This command gets summarized output for the PageViews metric with specified dimension filter and aggregation type.</span></span>

## <span data-ttu-id="fb038-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fb038-119">PARAMETERS</span></span>

### <span data-ttu-id="fb038-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="fb038-120">-AggregationType</span></span>
<span data-ttu-id="fb038-121">Der Aggregationstyp der Abfrage</span><span class="sxs-lookup"><span data-stu-id="fb038-121">The aggregation type of the query</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: None, Average, Count, Minimum, Maximum, Total

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb038-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb038-122">-DefaultProfile</span></span>
<span data-ttu-id="fb038-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb038-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb038-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="fb038-124">-DetailedOutput</span></span>
<span data-ttu-id="fb038-125">Gibt an, dass dieses Cmdlet eine detaillierte Ausgabe anzeigt.</span><span class="sxs-lookup"><span data-stu-id="fb038-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="fb038-126">Standardmäßig wird die Ausgabe zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="fb038-126">By default, output is summarized.</span></span>

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

### <span data-ttu-id="fb038-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="fb038-127">-EndTime</span></span>
<span data-ttu-id="fb038-128">Gibt die Endzeit der Abfrage in der lokalen Zeit an.</span><span class="sxs-lookup"><span data-stu-id="fb038-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="fb038-129">Die Standardeinstellung ist die aktuelle Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="fb038-129">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb038-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="fb038-130">-MetricFilter</span></span>
<span data-ttu-id="fb038-131">Gibt den Metrikdimensionsfilter an, nach dem Metriken abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="fb038-131">Specifies the metric dimension filter to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb038-132">-MetricName</span><span class="sxs-lookup"><span data-stu-id="fb038-132">-MetricName</span></span>
<span data-ttu-id="fb038-133">Gibt ein Array mit Namen von Metriken an.</span><span class="sxs-lookup"><span data-stu-id="fb038-133">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: GetWithDefaultParameters
Aliases: MetricNames

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: GetWithFullParameters
Aliases: MetricNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb038-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="fb038-134">-MetricNamespace</span></span>
<span data-ttu-id="fb038-135">Gibt den Metriknamespace an, für den Metriken abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="fb038-135">Specifies the metric namespace to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb038-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="fb038-136">-OrderBy</span></span>
<span data-ttu-id="fb038-137">Gibt die Aggregation an, die zum Sortieren von Ergebnissen verwendet werden soll, und die Sortierrichtung (Beispiel: Summe asc).</span><span class="sxs-lookup"><span data-stu-id="fb038-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb038-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb038-138">-ResourceId</span></span>
<span data-ttu-id="fb038-139">Gibt die Ressourcen-ID der Metrik an.</span><span class="sxs-lookup"><span data-stu-id="fb038-139">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="fb038-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="fb038-140">-ResultType</span></span>
<span data-ttu-id="fb038-141">Gibt den zurückgegebenen Ergebnistyp (Metadaten oder Daten) an.</span><span class="sxs-lookup"><span data-stu-id="fb038-141">Specifies the result type to be returned (metadata or data).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.ResultType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: Data, Metadata

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb038-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fb038-142">-StartTime</span></span>
<span data-ttu-id="fb038-143">Gibt die Startzeit der Abfrage in der lokalen Zeit an.</span><span class="sxs-lookup"><span data-stu-id="fb038-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="fb038-144">Die Standardeinstellung ist die aktuelle Ortszeit minus eine Stunde.</span><span class="sxs-lookup"><span data-stu-id="fb038-144">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb038-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="fb038-145">-TimeGrain</span></span>
<span data-ttu-id="fb038-146">Gibt die Zeitkörnung der Metrik als **TimeSpan-Objekt** im Format hh:mm:ss an.</span><span class="sxs-lookup"><span data-stu-id="fb038-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb038-147">-Top</span><span class="sxs-lookup"><span data-stu-id="fb038-147">-Top</span></span>
<span data-ttu-id="fb038-148">Gibt die maximale Anzahl der abzurufenden Datensätze (standard:10) an, die mit dem $filter.</span><span class="sxs-lookup"><span data-stu-id="fb038-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb038-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb038-149">CommonParameters</span></span>
<span data-ttu-id="fb038-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb038-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb038-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb038-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb038-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fb038-152">INPUTS</span></span>

### <span data-ttu-id="fb038-153">System.String</span><span class="sxs-lookup"><span data-stu-id="fb038-153">System.String</span></span>

### <span data-ttu-id="fb038-154">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="fb038-154">System.TimeSpan</span></span>

### <span data-ttu-id="fb038-155">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="fb038-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="fb038-156">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="fb038-156">System.DateTime</span></span>

### <span data-ttu-id="fb038-157">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb038-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fb038-158">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="fb038-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="fb038-159">System.String[]</span><span class="sxs-lookup"><span data-stu-id="fb038-159">System.String[]</span></span>

### <span data-ttu-id="fb038-160">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fb038-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fb038-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fb038-161">OUTPUTS</span></span>

### <span data-ttu-id="fb038-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span><span class="sxs-lookup"><span data-stu-id="fb038-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="fb038-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fb038-163">NOTES</span></span>

<span data-ttu-id="fb038-164">Weitere Informationen zu den unterstützten Metriken finden Sie unter: https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="fb038-164">More information about the supported metrics may be found at: https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="fb038-165">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fb038-165">RELATED LINKS</span></span>

<span data-ttu-id="fb038-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="fb038-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


