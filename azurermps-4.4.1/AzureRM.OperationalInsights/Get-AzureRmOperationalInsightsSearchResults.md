---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
ms.openlocfilehash: 161365ee947a118221fa922ab9e7d05486d3908d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663877"
---
# <span data-ttu-id="66d55-101">Get-AzureRmOperationalInsightsSearchResults</span><span class="sxs-lookup"><span data-stu-id="66d55-101">Get-AzureRmOperationalInsightsSearchResults</span></span>

## <span data-ttu-id="66d55-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66d55-102">SYNOPSIS</span></span>
<span data-ttu-id="66d55-103">Gibt Suchergebnisse basierend auf den angegebenen Parametern zurück.</span><span class="sxs-lookup"><span data-stu-id="66d55-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66d55-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66d55-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Top] <Int64>] [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>]
 [[-Start] <DateTime>] [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66d55-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66d55-105">DESCRIPTION</span></span>
<span data-ttu-id="66d55-106">Das Cmdlet " **Get-AzureRmOperationalInsightsSearchResults** " gibt die Suchergebnisse auf der Grundlage der angegebenen Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="66d55-106">The **Get-AzureRmOperationalInsightsSearchResults** cmdlet returns the search results based on the specified parameters.</span></span>

<span data-ttu-id="66d55-107">Sie können auf den Status der Suche in der Metadata-Eigenschaft des zurückgegebenen Objekts zugreifen.</span><span class="sxs-lookup"><span data-stu-id="66d55-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="66d55-108">Wenn der Status Ausstehend ist, wurde die Suche nicht abgeschlossen, und die Ergebnisse werden aus dem Archiv angezeigt.</span><span class="sxs-lookup"><span data-stu-id="66d55-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>

<span data-ttu-id="66d55-109">Sie können die Suchergebnisse aus der Value-Eigenschaft des zurückgegebenen Objekts abrufen.</span><span class="sxs-lookup"><span data-stu-id="66d55-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="66d55-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66d55-110">EXAMPLES</span></span>

### <span data-ttu-id="66d55-111">Beispiel 1: Abrufen von Suchergebnissen mithilfe einer Abfrage</span><span class="sxs-lookup"><span data-stu-id="66d55-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="66d55-112">Dieser Befehl ruft alle Suchergebnisse mithilfe einer Abfrage ab.</span><span class="sxs-lookup"><span data-stu-id="66d55-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="66d55-113">Beispiel 2: Abrufen von Suchergebnissen mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="66d55-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="66d55-114">Dieser Befehl ruft Suchergebnisse mithilfe einer ID ab.</span><span class="sxs-lookup"><span data-stu-id="66d55-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="66d55-115">Beispiel 3: warten Sie, bis eine Suche abgeschlossen ist, bevor Sie Ergebnisse anzeigen</span><span class="sxs-lookup"><span data-stu-id="66d55-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="66d55-116">Dieses Skript startet eine Suche und wartet bis zum Abschluss, bevor die Ergebnisse angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="66d55-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="66d55-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="66d55-117">PARAMETERS</span></span>

### <span data-ttu-id="66d55-118">-Ende</span><span class="sxs-lookup"><span data-stu-id="66d55-118">-End</span></span>
<span data-ttu-id="66d55-119">Ende des abgefragten Zeitbereichs.</span><span class="sxs-lookup"><span data-stu-id="66d55-119">End of the queried time range.</span></span>

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

### <span data-ttu-id="66d55-120">-ID</span><span class="sxs-lookup"><span data-stu-id="66d55-120">-Id</span></span>
<span data-ttu-id="66d55-121">Wenn eine ID angegeben wird, werden die Suchergebnisse für diese ID unter Verwendung der ursprünglichen Abfrageparameter abgerufen.</span><span class="sxs-lookup"><span data-stu-id="66d55-121">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

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

### <span data-ttu-id="66d55-122">– Posthighlight</span><span class="sxs-lookup"><span data-stu-id="66d55-122">-PostHighlight</span></span>
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

### <span data-ttu-id="66d55-123">-Prehighlight</span><span class="sxs-lookup"><span data-stu-id="66d55-123">-PreHighlight</span></span>
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

### <span data-ttu-id="66d55-124">-Query</span><span class="sxs-lookup"><span data-stu-id="66d55-124">-Query</span></span>
<span data-ttu-id="66d55-125">Die Suchabfrage, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66d55-125">The search query that will be executed.</span></span>

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

### <span data-ttu-id="66d55-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66d55-126">-ResourceGroupName</span></span>
<span data-ttu-id="66d55-127">Der Name der Ressourcengruppe, in der sich der Arbeitsbereich befindet.</span><span class="sxs-lookup"><span data-stu-id="66d55-127">The name of the resource group that contains the workspace.</span></span>

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

### <span data-ttu-id="66d55-128">-Start</span><span class="sxs-lookup"><span data-stu-id="66d55-128">-Start</span></span>
<span data-ttu-id="66d55-129">Anfang des abgefragten Zeitbereichs.</span><span class="sxs-lookup"><span data-stu-id="66d55-129">Start of the queried time range.</span></span>

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

### <span data-ttu-id="66d55-130">-Top</span><span class="sxs-lookup"><span data-stu-id="66d55-130">-Top</span></span>
<span data-ttu-id="66d55-131">Die maximale Anzahl von Ergebnissen, die zurückgegeben werden sollen, auf 5000.</span><span class="sxs-lookup"><span data-stu-id="66d55-131">The maximum number of results to be returned, limited to 5000.</span></span>

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

### <span data-ttu-id="66d55-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="66d55-132">-WorkspaceName</span></span>
<span data-ttu-id="66d55-133">Gibt einen Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="66d55-133">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="66d55-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d55-134">-DefaultProfile</span></span>
<span data-ttu-id="66d55-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66d55-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66d55-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d55-136">CommonParameters</span></span>
<span data-ttu-id="66d55-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66d55-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d55-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66d55-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d55-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66d55-139">INPUTS</span></span>

## <span data-ttu-id="66d55-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66d55-140">OUTPUTS</span></span>

### <span data-ttu-id="66d55-141">PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="66d55-141">PSSearchGetSearchResultsResponse</span></span>
<span data-ttu-id="66d55-142">Das **PSSearchGetSearchResultsResponse** -Objekt enthält eine Value-Eigenschaft, die die Datensätze enthält, die von der Suche im JSON-Format zurückgegeben wurden, und ein Metadatenobjekt, das Informationen zu den Ergebnissen der Suche enthält.</span><span class="sxs-lookup"><span data-stu-id="66d55-142">The **PSSearchGetSearchResultsResponse** object includes a Value property that includes the records returned from the search in JSON format and a metadata object that includes information about the results of the search.</span></span>

## <span data-ttu-id="66d55-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="66d55-143">NOTES</span></span>

## <span data-ttu-id="66d55-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66d55-144">RELATED LINKS</span></span>

[<span data-ttu-id="66d55-145">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="66d55-145">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>](./Get-AzureRmOperationalInsightsSavedSearchResults.md)


