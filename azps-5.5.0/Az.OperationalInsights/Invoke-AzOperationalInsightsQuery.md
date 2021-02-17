---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 0b2b27855e0c8248f0e7ceb9f1c096370a54e2fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169565"
---
# <span data-ttu-id="61b2e-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="61b2e-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="61b2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="61b2e-103">Gibt Suchergebnisse basierend auf den angegebenen Parametern zurück.</span><span class="sxs-lookup"><span data-stu-id="61b2e-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="61b2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61b2e-104">SYNTAX</span></span>

### <span data-ttu-id="61b2e-105">ByWorkspaceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="61b2e-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61b2e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="61b2e-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61b2e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61b2e-107">DESCRIPTION</span></span>
<span data-ttu-id="61b2e-108">Das **Cmdlet Invoke-AzOperationalInsightsQuery** gibt die Suchergebnisse basierend auf den angegebenen Parametern zurück.</span><span class="sxs-lookup"><span data-stu-id="61b2e-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="61b2e-109">Sie können auf den Status der Suche in der Metadateneigenschaft des zurückgegebenen Objekts zugreifen.</span><span class="sxs-lookup"><span data-stu-id="61b2e-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="61b2e-110">Wenn der Status "Ausstehend" ist, wurde die Suche nicht abgeschlossen, und die Ergebnisse werden aus dem Archiv entfernt.</span><span class="sxs-lookup"><span data-stu-id="61b2e-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="61b2e-111">Sie können die Ergebnisse der Suche aus der Eigenschaft "Value" des zurückgegebenen Objekts abrufen.</span><span class="sxs-lookup"><span data-stu-id="61b2e-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>
<span data-ttu-id="61b2e-112">Überprüfen Sie hier die Details allgemeiner Abfragegrenzwerte: https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language</span><span class="sxs-lookup"><span data-stu-id="61b2e-112">Please check detail of general query limits here: https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language.</span></span>

## <span data-ttu-id="61b2e-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="61b2e-113">EXAMPLES</span></span>

### <span data-ttu-id="61b2e-114">Beispiel 1: Erhalten von Suchergebnissen mithilfe einer Abfrage</span><span class="sxs-lookup"><span data-stu-id="61b2e-114">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="61b2e-115">Nach dem Aufruf enthält $queryResults.Results alle resultierenden Zeilen aus Ihrer Abfrage.</span><span class="sxs-lookup"><span data-stu-id="61b2e-115">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="61b2e-116">Beispiel 2: Konvertieren $results. Ergebnis iEnumerable für eine Matrix</span><span class="sxs-lookup"><span data-stu-id="61b2e-116">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="61b2e-117">Einige Abfragen können dazu führen, dass sehr große Datensätze zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="61b2e-117">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="61b2e-118">Daher besteht das Standardverhalten des Cmdlets in der Rückgabe eines IEnumerable-Speichers, um die Speicherkosten zu verringern.</span><span class="sxs-lookup"><span data-stu-id="61b2e-118">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="61b2e-119">Wenn Sie ein Array mit Ergebnissen bevorzugen, können Sie die LinQ Enumerable.ToArray()-Erweiterungsmethode verwenden, um IEnumerable in ein Array zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="61b2e-119">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="61b2e-120">Beispiel 3: Erhalten von Suchergebnissen mithilfe einer Abfrage über einen bestimmten Zeitraum</span><span class="sxs-lookup"><span data-stu-id="61b2e-120">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="61b2e-121">Die Ergebnisse dieser Abfrage sind auf die letzten 24 Stunden beschränkt.</span><span class="sxs-lookup"><span data-stu-id="61b2e-121">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="61b2e-122">Beispiel 4: Hinzufügen von Render- & in Abfrageergebnisse</span><span class="sxs-lookup"><span data-stu-id="61b2e-122">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="61b2e-123">Weitere [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) Informationen zum Rendern und zur Statistik finden Sie im Detail.</span><span class="sxs-lookup"><span data-stu-id="61b2e-123">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="61b2e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61b2e-124">PARAMETERS</span></span>

### <span data-ttu-id="61b2e-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61b2e-125">-AsJob</span></span>
<span data-ttu-id="61b2e-126">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="61b2e-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b2e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61b2e-127">-DefaultProfile</span></span>
<span data-ttu-id="61b2e-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61b2e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61b2e-129">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="61b2e-129">-IncludeRender</span></span>
<span data-ttu-id="61b2e-130">Falls angegeben, werden Renderinformationen für metrische Abfragen in die Antwort einbezogen.</span><span class="sxs-lookup"><span data-stu-id="61b2e-130">If specified, rendering information for metric queries will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b2e-131">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="61b2e-131">-IncludeStatistics</span></span>
<span data-ttu-id="61b2e-132">Falls angegeben, werden Abfragestatistiken in die Antwort einbezogen.</span><span class="sxs-lookup"><span data-stu-id="61b2e-132">If specified, query statistics will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b2e-133">-Query</span><span class="sxs-lookup"><span data-stu-id="61b2e-133">-Query</span></span>
<span data-ttu-id="61b2e-134">Die auszuführende Abfrage.</span><span class="sxs-lookup"><span data-stu-id="61b2e-134">The query to execute.</span></span>

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

### <span data-ttu-id="61b2e-135">-Timespan</span><span class="sxs-lookup"><span data-stu-id="61b2e-135">-Timespan</span></span>
<span data-ttu-id="61b2e-136">Die Zeitspanne, über die die Abfrage gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="61b2e-136">The timespan to bound the query by.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b2e-137">-Wait</span><span class="sxs-lookup"><span data-stu-id="61b2e-137">-Wait</span></span>
<span data-ttu-id="61b2e-138">Legt eine obere Grenze für die Zeit ein, die der Server für die Verarbeitung der Abfrage aufbringt.</span><span class="sxs-lookup"><span data-stu-id="61b2e-138">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="61b2e-139">Sieh: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="61b2e-139">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b2e-140">-Workspace</span><span class="sxs-lookup"><span data-stu-id="61b2e-140">-Workspace</span></span>
<span data-ttu-id="61b2e-141">Der Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="61b2e-141">The workspace</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61b2e-142">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="61b2e-142">-WorkspaceId</span></span>
<span data-ttu-id="61b2e-143">Die Arbeitsbereichs-ID.</span><span class="sxs-lookup"><span data-stu-id="61b2e-143">The workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b2e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b2e-144">CommonParameters</span></span>
<span data-ttu-id="61b2e-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61b2e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b2e-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61b2e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b2e-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="61b2e-147">INPUTS</span></span>

### <span data-ttu-id="61b2e-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="61b2e-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="61b2e-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="61b2e-149">OUTPUTS</span></span>

### <span data-ttu-id="61b2e-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="61b2e-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="61b2e-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="61b2e-151">NOTES</span></span>

## <span data-ttu-id="61b2e-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="61b2e-152">RELATED LINKS</span></span>
