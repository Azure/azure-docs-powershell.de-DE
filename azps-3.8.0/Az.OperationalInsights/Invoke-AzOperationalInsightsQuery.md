---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 528588ac4a85303809b6e287f3e99b06db9f2a6d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995346"
---
# <span data-ttu-id="9624b-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="9624b-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="9624b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9624b-102">SYNOPSIS</span></span>
<span data-ttu-id="9624b-103">Gibt Suchergebnisse basierend auf den angegebenen Parametern zurück.</span><span class="sxs-lookup"><span data-stu-id="9624b-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="9624b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9624b-104">SYNTAX</span></span>

### <span data-ttu-id="9624b-105">ByWorkspaceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="9624b-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9624b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9624b-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9624b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9624b-107">DESCRIPTION</span></span>
<span data-ttu-id="9624b-108">Das Cmdlet **Invoke-AzOperationalInsightsQuery** gibt die Suchergebnisse auf der Grundlage der angegebenen Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="9624b-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="9624b-109">Sie können auf den Status der Suche in der Metadata-Eigenschaft des zurückgegebenen Objekts zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9624b-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="9624b-110">Wenn der Status Ausstehend ist, wurde die Suche nicht abgeschlossen, und die Ergebnisse werden aus dem Archiv angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9624b-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="9624b-111">Sie können die Suchergebnisse aus der Value-Eigenschaft des zurückgegebenen Objekts abrufen.</span><span class="sxs-lookup"><span data-stu-id="9624b-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="9624b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9624b-112">EXAMPLES</span></span>

### <span data-ttu-id="9624b-113">Beispiel 1: Abrufen von Suchergebnissen mithilfe einer Abfrage</span><span class="sxs-lookup"><span data-stu-id="9624b-113">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="9624b-114">Sobald aufgerufen, enthält $queryResults. results alle resultierenden Zeilen aus der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="9624b-114">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="9624b-115">Beispiel 2: Konvertieren von $results. Ergebnis IEnumerable in ein Array</span><span class="sxs-lookup"><span data-stu-id="9624b-115">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="9624b-116">Einige Abfragen können dazu führen, dass sehr große Datensätze zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9624b-116">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="9624b-117">Aus diesem Grund ist das Standardverhalten des Cmdlets, ein IEnumerable zurückzugeben, um die Speicherkosten zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="9624b-117">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="9624b-118">Wenn Sie ein Array von Ergebnissen bevorzugen, können Sie die IEnumerable-Methode Enumerable. ToArray () verwenden, um die IEnumerable in ein Array zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="9624b-118">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="9624b-119">Beispiel 3: Abrufen von Suchergebnissen mithilfe einer Abfrage über einen bestimmten Zeitraum</span><span class="sxs-lookup"><span data-stu-id="9624b-119">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="9624b-120">Die Ergebnisse dieser Abfrage sind auf die letzten 24 Stunden limitiert.</span><span class="sxs-lookup"><span data-stu-id="9624b-120">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="9624b-121">Beispiel 4: Rendern & Statistiken in Abfrageergebnis einbeziehen</span><span class="sxs-lookup"><span data-stu-id="9624b-121">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="9624b-122">[https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions)Details zu den Render-und Statistikinformationen finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="9624b-122">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="9624b-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="9624b-123">PARAMETERS</span></span>

### <span data-ttu-id="9624b-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9624b-124">-AsJob</span></span>
<span data-ttu-id="9624b-125">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9624b-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9624b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9624b-126">-DefaultProfile</span></span>
<span data-ttu-id="9624b-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9624b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9624b-128">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="9624b-128">-IncludeRender</span></span>
<span data-ttu-id="9624b-129">Wenn angegeben, werden Renderinginformationen für metrische Abfragen in die Antwort aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="9624b-129">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="9624b-130">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="9624b-130">-IncludeStatistics</span></span>
<span data-ttu-id="9624b-131">Wenn angegeben, werden Abfragestatistiken in der Antwort berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="9624b-131">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="9624b-132">-Query</span><span class="sxs-lookup"><span data-stu-id="9624b-132">-Query</span></span>
<span data-ttu-id="9624b-133">Die auszuführende Abfrage.</span><span class="sxs-lookup"><span data-stu-id="9624b-133">The query to execute.</span></span>

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

### <span data-ttu-id="9624b-134">-TimeSpan</span><span class="sxs-lookup"><span data-stu-id="9624b-134">-Timespan</span></span>
<span data-ttu-id="9624b-135">Die TimeSpan, an die die Abfrage gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="9624b-135">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="9624b-136">-Wait</span><span class="sxs-lookup"><span data-stu-id="9624b-136">-Wait</span></span>
<span data-ttu-id="9624b-137">Legt eine Obergrenze für die Zeitspanne an, die der Server für die Verarbeitung der Abfrage aufwendet.</span><span class="sxs-lookup"><span data-stu-id="9624b-137">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="9624b-138">Sieh: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="9624b-138">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="9624b-139">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="9624b-139">-Workspace</span></span>
<span data-ttu-id="9624b-140">Der Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="9624b-140">The workspace</span></span>

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

### <span data-ttu-id="9624b-141">-Arbeitsbereichs-Nr</span><span class="sxs-lookup"><span data-stu-id="9624b-141">-WorkspaceId</span></span>
<span data-ttu-id="9624b-142">Die Arbeitsbereichs-ID.</span><span class="sxs-lookup"><span data-stu-id="9624b-142">The workspace ID.</span></span>

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

### <span data-ttu-id="9624b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9624b-143">CommonParameters</span></span>
<span data-ttu-id="9624b-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9624b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9624b-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9624b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9624b-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9624b-146">INPUTS</span></span>

### <span data-ttu-id="9624b-147">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9624b-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="9624b-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9624b-148">OUTPUTS</span></span>

### <span data-ttu-id="9624b-149">Microsoft. Azure. Commands. OperationalInsights. Models. PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="9624b-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="9624b-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="9624b-150">NOTES</span></span>

## <span data-ttu-id="9624b-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9624b-151">RELATED LINKS</span></span>
