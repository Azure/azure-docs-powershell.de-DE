---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470713"
---
# <span data-ttu-id="421d1-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="421d1-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="421d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="421d1-102">SYNOPSIS</span></span>
<span data-ttu-id="421d1-103">Erstellt ein neues Sql IndexingPolicy-Objekt aus".</span><span class="sxs-lookup"><span data-stu-id="421d1-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="421d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="421d1-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="421d1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="421d1-105">DESCRIPTION</span></span>
<span data-ttu-id="421d1-106">Das **Cmdlet "New-AzCosmosDBSqlIndexingPolicy"** erstellt ein neues Objekt vom Typ "PSSqlIndexingPolicy".</span><span class="sxs-lookup"><span data-stu-id="421d1-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="421d1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="421d1-107">EXAMPLES</span></span>

### <span data-ttu-id="421d1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="421d1-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $ipath2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $IncludedPath = New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>  $SpatialSpec = New-AzCosmosDBSqlSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\> $cp1 = New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending
PS C:\>  $cp2 = New-AzCosmosDBSqlCompositePath -Path "/aberc" -Order Descending
PS C:\> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\> New-AzCosmosDBSqlIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent

Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

## <span data-ttu-id="421d1-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="421d1-109">PARAMETERS</span></span>

### <span data-ttu-id="421d1-110">-Automatisch</span><span class="sxs-lookup"><span data-stu-id="421d1-110">-Automatic</span></span>
<span data-ttu-id="421d1-111">Bool, um anzugeben, ob die Indizierungsrichtlinie automatisch ist</span><span class="sxs-lookup"><span data-stu-id="421d1-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="421d1-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="421d1-112">-CompositePath</span></span>
<span data-ttu-id="421d1-113">Array von Objekten vom Typ "Microsoft.Azure.Commands.UmsDB.PSCompositePath"</span><span class="sxs-lookup"><span data-stu-id="421d1-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="421d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="421d1-114">-DefaultProfile</span></span>
<span data-ttu-id="421d1-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="421d1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="421d1-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="421d1-116">-ExcludedPath</span></span>
<span data-ttu-id="421d1-117">Array von Zeichenfolgen, die "excludedPath" enthalten(Gibt einen Pfad innerhalb eines JSON-Dokuments an, der im Azure Azure Db-Dienst ausgeschlossen werden soll.)  elemente.</span><span class="sxs-lookup"><span data-stu-id="421d1-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="421d1-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="421d1-118">-IncludedPath</span></span>
<span data-ttu-id="421d1-119">Array von Zeichenfolgen, die "includedPath"-Elemente enthalten (Gibt einen Pfad in einem JSON-Dokument an, der in den Azure Azure Db-Dienst eingeschlossen werden soll.)</span><span class="sxs-lookup"><span data-stu-id="421d1-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="421d1-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="421d1-120">-IndexingMode</span></span>
<span data-ttu-id="421d1-121">gibt den Indizierungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="421d1-121">indicates the indexing mode.</span></span>
<span data-ttu-id="421d1-122">Mögliche Werte sind: "Consistent", "Lazy", "None".</span><span class="sxs-lookup"><span data-stu-id="421d1-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="421d1-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="421d1-123">-SpatialSpec</span></span>
<span data-ttu-id="421d1-124">Array von Objekten vom Typ "Microsoft.Azure.Commands.ArraysDB.PSSpatialSpec"</span><span class="sxs-lookup"><span data-stu-id="421d1-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="421d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="421d1-125">CommonParameters</span></span>
<span data-ttu-id="421d1-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="421d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="421d1-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="421d1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="421d1-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="421d1-128">INPUTS</span></span>

### <span data-ttu-id="421d1-129">Keine</span><span class="sxs-lookup"><span data-stu-id="421d1-129">None</span></span>

## <span data-ttu-id="421d1-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="421d1-130">OUTPUTS</span></span>

### <span data-ttu-id="421d1-131">Microsoft.Azure.Commands.DiesDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="421d1-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="421d1-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="421d1-132">NOTES</span></span>

## <span data-ttu-id="421d1-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="421d1-133">RELATED LINKS</span></span>
