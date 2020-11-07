---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
ms.openlocfilehash: 47a8edf304ebc5481073151c180c01a65259149c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824115"
---
# <span data-ttu-id="2dbaf-101">Get-AzOperationalInsightsSearchResult</span><span class="sxs-lookup"><span data-stu-id="2dbaf-101">Get-AzOperationalInsightsSearchResult</span></span>

## <span data-ttu-id="2dbaf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2dbaf-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbaf-103">Gibt Suchergebnisse basierend auf den angegebenen Parametern zurück.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="2dbaf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dbaf-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String> [[-Top] <Int64>]
 [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>] [[-Start] <DateTime>]
 [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dbaf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dbaf-105">DESCRIPTION</span></span>
<span data-ttu-id="2dbaf-106">Das Cmdlet " **Get-AzOperationalInsightsSearchResult** " gibt die Suchergebnisse auf der Grundlage der angegebenen Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-106">The **Get-AzOperationalInsightsSearchResult** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="2dbaf-107">Sie können auf den Status der Suche in der Metadata-Eigenschaft des zurückgegebenen Objekts zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="2dbaf-108">Wenn der Status Ausstehend ist, wurde die Suche nicht abgeschlossen, und die Ergebnisse werden aus dem Archiv angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="2dbaf-109">Sie können die Suchergebnisse aus der Value-Eigenschaft des zurückgegebenen Objekts abrufen.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="2dbaf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2dbaf-110">EXAMPLES</span></span>

### <span data-ttu-id="2dbaf-111">Beispiel 1: Abrufen von Suchergebnissen mithilfe einer Abfrage</span><span class="sxs-lookup"><span data-stu-id="2dbaf-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="2dbaf-112">Dieser Befehl ruft alle Suchergebnisse mithilfe einer Abfrage ab.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="2dbaf-113">Beispiel 2: Abrufen von Suchergebnissen mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="2dbaf-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="2dbaf-114">Dieser Befehl ruft Suchergebnisse mithilfe einer ID ab.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="2dbaf-115">Beispiel 3: warten Sie, bis eine Suche abgeschlossen ist, bevor Sie Ergebnisse anzeigen</span><span class="sxs-lookup"><span data-stu-id="2dbaf-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="2dbaf-116">Dieses Skript startet eine Suche und wartet bis zum Abschluss, bevor die Ergebnisse angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="2dbaf-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dbaf-117">PARAMETERS</span></span>

### <span data-ttu-id="2dbaf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dbaf-118">-DefaultProfile</span></span>
<span data-ttu-id="2dbaf-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2dbaf-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dbaf-120">-Ende</span><span class="sxs-lookup"><span data-stu-id="2dbaf-120">-End</span></span>
<span data-ttu-id="2dbaf-121">Ende des abgefragten Zeitbereichs.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-121">End of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dbaf-122">-ID</span><span class="sxs-lookup"><span data-stu-id="2dbaf-122">-Id</span></span>
<span data-ttu-id="2dbaf-123">Wenn eine ID angegeben wird, werden die Suchergebnisse für diese ID unter Verwendung der ursprünglichen Abfrageparameter abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-123">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dbaf-124">– Posthighlight</span><span class="sxs-lookup"><span data-stu-id="2dbaf-124">-PostHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dbaf-125">-Prehighlight</span><span class="sxs-lookup"><span data-stu-id="2dbaf-125">-PreHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dbaf-126">-Query</span><span class="sxs-lookup"><span data-stu-id="2dbaf-126">-Query</span></span>
<span data-ttu-id="2dbaf-127">Die Suchabfrage, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-127">The search query that will be executed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dbaf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dbaf-128">-ResourceGroupName</span></span>
<span data-ttu-id="2dbaf-129">Der Name der Ressourcengruppe, in der sich der Arbeitsbereich befindet.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-129">The name of the resource group that contains the workspace.</span></span>

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

### <span data-ttu-id="2dbaf-130">-Start</span><span class="sxs-lookup"><span data-stu-id="2dbaf-130">-Start</span></span>
<span data-ttu-id="2dbaf-131">Anfang des abgefragten Zeitbereichs.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-131">Start of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dbaf-132">-Top</span><span class="sxs-lookup"><span data-stu-id="2dbaf-132">-Top</span></span>
<span data-ttu-id="2dbaf-133">Die maximale Anzahl von Ergebnissen, die zurückgegeben werden sollen, auf 5000.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-133">The maximum number of results to be returned, limited to 5000.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 10
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dbaf-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2dbaf-134">-WorkspaceName</span></span>
<span data-ttu-id="2dbaf-135">Gibt einen Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-135">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dbaf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbaf-136">CommonParameters</span></span>
<span data-ttu-id="2dbaf-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dbaf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbaf-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dbaf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbaf-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2dbaf-139">INPUTS</span></span>

### <span data-ttu-id="2dbaf-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2dbaf-140">System.String</span></span>

### <span data-ttu-id="2dbaf-141">System. Int64</span><span class="sxs-lookup"><span data-stu-id="2dbaf-141">System.Int64</span></span>

### <span data-ttu-id="2dbaf-142">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2dbaf-142">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2dbaf-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2dbaf-143">OUTPUTS</span></span>

### <span data-ttu-id="2dbaf-144">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="2dbaf-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="2dbaf-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="2dbaf-145">NOTES</span></span>

## <span data-ttu-id="2dbaf-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2dbaf-146">RELATED LINKS</span></span>

[<span data-ttu-id="2dbaf-147">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="2dbaf-147">Get-AzOperationalInsightsSavedSearchResult</span></span>](./Get-AzOperationalInsightsSavedSearchResult.md)


