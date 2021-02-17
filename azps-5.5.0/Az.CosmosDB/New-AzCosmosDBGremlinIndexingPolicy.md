---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: 10a928be0827f280d7fe00a1307535dbad6eda1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164036"
---
# <span data-ttu-id="29e01-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="29e01-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="29e01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29e01-102">SYNOPSIS</span></span>
<span data-ttu-id="29e01-103">Erstellt ein neues Indizierungspolicy-Objekt aus Untern.</span><span class="sxs-lookup"><span data-stu-id="29e01-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="29e01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29e01-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29e01-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29e01-105">DESCRIPTION</span></span>
<span data-ttu-id="29e01-106">Das **Cmdlet "New-AzCosmosDBGremlinIndexingPolicy"** erstellt ein neues Objekt vom Typ "PSIndexingPolicy".</span><span class="sxs-lookup"><span data-stu-id="29e01-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="29e01-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29e01-107">EXAMPLES</span></span>

### <span data-ttu-id="29e01-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29e01-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $ipath2 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $IncludedPath = New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>>  $SpatialSpec = New-AzCosmosDBGremlinSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\>> $cp1 = New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending
PS C:\>>  $cp2 = New-AzCosmosDBGremlinCompositePath -Path "/aberc" -Order Descending
PS C:\>> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\>> New-AzCosmosDBGremlinIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent


Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

<span data-ttu-id="29e01-109">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="29e01-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="29e01-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29e01-110">PARAMETERS</span></span>

### <span data-ttu-id="29e01-111">-Automatisch</span><span class="sxs-lookup"><span data-stu-id="29e01-111">-Automatic</span></span>
<span data-ttu-id="29e01-112">Bool, um anzugeben, ob die Indizierungsrichtlinie automatisch ist</span><span class="sxs-lookup"><span data-stu-id="29e01-112">Bool to indicate if the indexing policy is automatic</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e01-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="29e01-113">-CompositePath</span></span>
<span data-ttu-id="29e01-114">Array von Objekten vom Typ "Microsoft.Azure.Commands.UmsDB.PSCompositePath"</span><span class="sxs-lookup"><span data-stu-id="29e01-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

```yaml
Type: PSCompositePath[][]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e01-115">-DefaultProfile</span></span>
<span data-ttu-id="29e01-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29e01-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e01-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="29e01-117">-ExcludedPath</span></span>
<span data-ttu-id="29e01-118">Array von Zeichenfolgen, die "excludedPath" enthalten(Gibt einen Pfad innerhalb eines JSON-Dokuments an, der im Azure Azure Db-Dienst ausgeschlossen werden soll.)  elemente.</span><span class="sxs-lookup"><span data-stu-id="29e01-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e01-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="29e01-119">-IncludedPath</span></span>
<span data-ttu-id="29e01-120">Array von Zeichenfolgen, die "includedPath"-Elemente enthalten (Gibt einen Pfad in einem JSON-Dokument an, der in den Azure Azure Db-Dienst eingeschlossen werden soll).)</span><span class="sxs-lookup"><span data-stu-id="29e01-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

```yaml
Type: PSIncludedPath[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e01-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="29e01-121">-IndexingMode</span></span>
<span data-ttu-id="29e01-122">Gibt den Indizierungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="29e01-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="29e01-123">Mögliche Werte sind: "Consistent", "Lazy", "None".</span><span class="sxs-lookup"><span data-stu-id="29e01-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="29e01-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="29e01-124">-SpatialSpec</span></span>
<span data-ttu-id="29e01-125">Array von Objekten vom Typ "Microsoft.Azure.Commands.ArraysDB.PSSpatialSpec"</span><span class="sxs-lookup"><span data-stu-id="29e01-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

```yaml
Type: PSSpatialSpec[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e01-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e01-126">CommonParameters</span></span>
<span data-ttu-id="29e01-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29e01-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e01-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29e01-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e01-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29e01-129">INPUTS</span></span>

### <span data-ttu-id="29e01-130">Keine</span><span class="sxs-lookup"><span data-stu-id="29e01-130">None</span></span>

## <span data-ttu-id="29e01-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29e01-131">OUTPUTS</span></span>

### <span data-ttu-id="29e01-132">Microsoft.Azure.Commands.DiesDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="29e01-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="29e01-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="29e01-133">NOTES</span></span>

## <span data-ttu-id="29e01-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="29e01-134">RELATED LINKS</span></span>
