---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: ce554f3591f022bdbc375c12a50ea9dae85b8baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943051"
---
# <span data-ttu-id="b135a-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="b135a-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="b135a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b135a-102">SYNOPSIS</span></span>
<span data-ttu-id="b135a-103">Erstellt ein neues CosmosDB IndexingPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b135a-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="b135a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b135a-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b135a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b135a-105">DESCRIPTION</span></span>
<span data-ttu-id="b135a-106">Das **Cmdlet New-AzCosmosDBGremlinIndexingPolicy** erstellt ein neues Objekt vom Typ PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="b135a-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="b135a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b135a-107">EXAMPLES</span></span>

### <span data-ttu-id="b135a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b135a-108">Example 1</span></span>
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

<span data-ttu-id="b135a-109">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="b135a-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b135a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b135a-110">PARAMETERS</span></span>

### <span data-ttu-id="b135a-111">-Automatisch</span><span class="sxs-lookup"><span data-stu-id="b135a-111">-Automatic</span></span>
<span data-ttu-id="b135a-112">Bool, um anzugeben, ob die Indizierungsrichtlinie automatisch ist</span><span class="sxs-lookup"><span data-stu-id="b135a-112">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="b135a-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="b135a-113">-CompositePath</span></span>
<span data-ttu-id="b135a-114">Array von Array von Objekten vom Typ Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="b135a-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="b135a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b135a-115">-DefaultProfile</span></span>
<span data-ttu-id="b135a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b135a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b135a-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="b135a-117">-ExcludedPath</span></span>
<span data-ttu-id="b135a-118">Array von Zeichenfolgen, die excludedPath enthalten(Gibt einen Pfad innerhalb eines JSON-Dokuments an, der im Azure Cosmos DB-Dienst ausgeschlossen werden soll.)  -Elemente.</span><span class="sxs-lookup"><span data-stu-id="b135a-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="b135a-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="b135a-119">-IncludedPath</span></span>
<span data-ttu-id="b135a-120">Array von Zeichenfolgen, die includedPath enthalten (Gibt einen Pfad in einem JSON-Dokument an, der in die Azure Cosmos DB-Dienstelemente einbezogen werden soll.)</span><span class="sxs-lookup"><span data-stu-id="b135a-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="b135a-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="b135a-121">-IndexingMode</span></span>
<span data-ttu-id="b135a-122">Gibt den Indizierungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="b135a-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="b135a-123">Mögliche Werte sind: "Konsistent", "Lazy", "Keine"</span><span class="sxs-lookup"><span data-stu-id="b135a-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="b135a-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="b135a-124">-SpatialSpec</span></span>
<span data-ttu-id="b135a-125">Array von Objekten vom Typ Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="b135a-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="b135a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b135a-126">CommonParameters</span></span>
<span data-ttu-id="b135a-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b135a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b135a-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b135a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b135a-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b135a-129">INPUTS</span></span>

### <span data-ttu-id="b135a-130">Keine</span><span class="sxs-lookup"><span data-stu-id="b135a-130">None</span></span>

## <span data-ttu-id="b135a-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b135a-131">OUTPUTS</span></span>

### <span data-ttu-id="b135a-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="b135a-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="b135a-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b135a-133">NOTES</span></span>

## <span data-ttu-id="b135a-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b135a-134">RELATED LINKS</span></span>
