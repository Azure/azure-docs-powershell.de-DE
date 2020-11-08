---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
ms.openlocfilehash: d02a6f9ca3f4821fa8a552f92ef90fa24a9e6bd2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180249"
---
# <span data-ttu-id="5e5d2-101">Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="5e5d2-101">Get-AzMetric</span></span>

## <span data-ttu-id="5e5d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="5e5d2-103">Ruft die metrischen Werte einer Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-103">Gets the metric values of a resource.</span></span>

## <span data-ttu-id="5e5d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e5d2-104">SYNTAX</span></span>

### <span data-ttu-id="5e5d2-105">GetWithDefaultParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e5d2-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e5d2-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="5e5d2-106">GetWithFullParameters</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e5d2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e5d2-107">DESCRIPTION</span></span>
<span data-ttu-id="5e5d2-108">Das Cmdlet " **Get-AzMetric** " Ruft die metrischen Werte für eine angegebene Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-108">The **Get-AzMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="5e5d2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e5d2-109">EXAMPLES</span></span>

### <span data-ttu-id="5e5d2-110">Beispiel 1: Abrufen einer Metrik mit zusammengefasster Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5e5d2-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="5e5d2-111">Dieser Befehl ruft die metrischen Werte für website3 mit einer Zeit Körnung von 1 Minute ab.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="5e5d2-112">Beispiel 2: Abrufen einer Metrik mit einer detaillierten Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5e5d2-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="5e5d2-113">Dieser Befehl ruft die metrischen Werte für website3 mit einer Zeit Körnung von 1 Minute ab.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="5e5d2-114">Die Ausgabe ist detailliert.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-114">The output is detailed.</span></span>

### <span data-ttu-id="5e5d2-115">Beispiel 3: Abrufen der detaillierten Ausgabe für eine angegebene Metrik</span><span class="sxs-lookup"><span data-stu-id="5e5d2-115">Example 3: Get detailed output for a specified metric</span></span>
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

<span data-ttu-id="5e5d2-116">Dieser Befehl ruft eine detaillierte Ausgabe für die Anforderungs Metrik ab.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="5e5d2-117">Beispiel 4: Abrufen einer zusammengefassten Ausgabe für eine angegebene Metrik mit dem angegebenen Dimensionsfilter</span><span class="sxs-lookup"><span data-stu-id="5e5d2-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
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

<span data-ttu-id="5e5d2-118">Mit diesem Befehl wird eine zusammengefasste Ausgabe für die Metrik "Seitenzugriffe" mit dem angegebenen Dimensionsfilter und Aggregations abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-118">This command gets summarized output for the PageViews metric with specified dimension filter and aggregation type.</span></span>

## <span data-ttu-id="5e5d2-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e5d2-119">PARAMETERS</span></span>

### <span data-ttu-id="5e5d2-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="5e5d2-120">-AggregationType</span></span>
<span data-ttu-id="5e5d2-121">Der Aggregations der Abfrage</span><span class="sxs-lookup"><span data-stu-id="5e5d2-121">The aggregation type of the query</span></span>

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

### <span data-ttu-id="5e5d2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e5d2-122">-DefaultProfile</span></span>
<span data-ttu-id="5e5d2-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e5d2-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="5e5d2-124">-DetailedOutput</span></span>
<span data-ttu-id="5e5d2-125">Gibt an, dass dieses Cmdlet eine detaillierte Ausgabe anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="5e5d2-126">Standardmäßig wird die Ausgabe zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-126">By default, output is summarized.</span></span>

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

### <span data-ttu-id="5e5d2-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5e5d2-127">-EndTime</span></span>
<span data-ttu-id="5e5d2-128">Gibt die Endzeit der Abfrage in Ortszeit an.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="5e5d2-129">Der Standardwert ist die aktuelle Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-129">The default is the current time.</span></span>

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

### <span data-ttu-id="5e5d2-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="5e5d2-130">-MetricFilter</span></span>
<span data-ttu-id="5e5d2-131">Gibt den metrischen Dimensionsfilter für Abfrage Metriken an.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-131">Specifies the metric dimension filter to query metrics for.</span></span>

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

### <span data-ttu-id="5e5d2-132">-Metricname</span><span class="sxs-lookup"><span data-stu-id="5e5d2-132">-MetricName</span></span>
<span data-ttu-id="5e5d2-133">Gibt ein Array mit Namen von Metriken an.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-133">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="5e5d2-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="5e5d2-134">-MetricNamespace</span></span>
<span data-ttu-id="5e5d2-135">Gibt den metrischen Namespace an, für den Metriken abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-135">Specifies the metric namespace to query metrics for.</span></span>

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

### <span data-ttu-id="5e5d2-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="5e5d2-136">-OrderBy</span></span>
<span data-ttu-id="5e5d2-137">Gibt die Aggregation an, die für das Sortieren von Ergebnissen und die Richtung der Sortierung verwendet werden soll (Beispiel: Sum ASC).</span><span class="sxs-lookup"><span data-stu-id="5e5d2-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

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

### <span data-ttu-id="5e5d2-138">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5e5d2-138">-ResourceId</span></span>
<span data-ttu-id="5e5d2-139">Gibt die Ressourcen-ID der Metrik an.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-139">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="5e5d2-140">-Ergebnistyp</span><span class="sxs-lookup"><span data-stu-id="5e5d2-140">-ResultType</span></span>
<span data-ttu-id="5e5d2-141">Gibt den zurückzugebenden Ergebnistyp an (Metadaten oder Daten).</span><span class="sxs-lookup"><span data-stu-id="5e5d2-141">Specifies the result type to be returned (metadata or data).</span></span>

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

### <span data-ttu-id="5e5d2-142">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="5e5d2-142">-StartTime</span></span>
<span data-ttu-id="5e5d2-143">Gibt die Startzeit der Abfrage in Ortszeit an.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="5e5d2-144">Der Standardwert ist die aktuelle Ortszeit minus 1 Stunde.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-144">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="5e5d2-145">-Zeitkorn</span><span class="sxs-lookup"><span data-stu-id="5e5d2-145">-TimeGrain</span></span>
<span data-ttu-id="5e5d2-146">Gibt die Zeit Körnung der Metrik als **TimeSpan** -Objekt im Format hh: mm: SS an.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

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

### <span data-ttu-id="5e5d2-147">-Top</span><span class="sxs-lookup"><span data-stu-id="5e5d2-147">-Top</span></span>
<span data-ttu-id="5e5d2-148">Gibt die maximale Anzahl von Datensätzen an, die abgerufen werden sollen (Standardwert: 10), die mit $Filter angegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

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

### <span data-ttu-id="5e5d2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e5d2-149">CommonParameters</span></span>
<span data-ttu-id="5e5d2-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e5d2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e5d2-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e5d2-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e5d2-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e5d2-152">INPUTS</span></span>

### <span data-ttu-id="5e5d2-153">System. String</span><span class="sxs-lookup"><span data-stu-id="5e5d2-153">System.String</span></span>

### <span data-ttu-id="5e5d2-154">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="5e5d2-154">System.TimeSpan</span></span>

### <span data-ttu-id="5e5d2-155">System. Nullable ' 1 [[Microsoft. Azure. Management. Monitor. Models. AggregationType, Microsoft. Azure. Management. Monitor, Version = 0.21.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5e5d2-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5e5d2-156">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="5e5d2-156">System.DateTime</span></span>

### <span data-ttu-id="5e5d2-157">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5e5d2-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5e5d2-158">System. Nullable ' 1 [[Microsoft. Azure. Management. Monitor. Models. ResultType, Microsoft. Azure. Management. Monitor, Version = 0.21.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5e5d2-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5e5d2-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="5e5d2-159">System.String[]</span></span>

### <span data-ttu-id="5e5d2-160">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="5e5d2-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5e5d2-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e5d2-161">OUTPUTS</span></span>

### <span data-ttu-id="5e5d2-162">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric</span><span class="sxs-lookup"><span data-stu-id="5e5d2-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="5e5d2-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e5d2-163">NOTES</span></span>

<span data-ttu-id="5e5d2-164">Weitere Informationen zu den unterstützten Metriken finden Sie unter: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="5e5d2-164">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="5e5d2-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e5d2-165">RELATED LINKS</span></span>

<span data-ttu-id="5e5d2-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md) 
 [Neu – AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="5e5d2-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


