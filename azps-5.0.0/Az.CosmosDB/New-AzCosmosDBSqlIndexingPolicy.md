---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299236"
---
# <span data-ttu-id="57371-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="57371-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="57371-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57371-102">SYNOPSIS</span></span>
<span data-ttu-id="57371-103">Erstellt ein neues CosmosDB SQL-IndexingPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="57371-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="57371-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57371-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57371-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57371-105">DESCRIPTION</span></span>
<span data-ttu-id="57371-106">Das Cmdlet **New-AzCosmosDBSqlIndexingPolicy** erstellt ein neues Objekt vom Typ PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="57371-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="57371-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57371-107">EXAMPLES</span></span>

### <span data-ttu-id="57371-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="57371-108">Example 1</span></span>
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

## <span data-ttu-id="57371-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="57371-109">PARAMETERS</span></span>

### <span data-ttu-id="57371-110">-Automatisch</span><span class="sxs-lookup"><span data-stu-id="57371-110">-Automatic</span></span>
<span data-ttu-id="57371-111">Bool, um anzugeben, ob die Indizierungs Richtlinie automatisch ist</span><span class="sxs-lookup"><span data-stu-id="57371-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="57371-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="57371-112">-CompositePath</span></span>
<span data-ttu-id="57371-113">Array von Array von Objekten vom Typ Microsoft. Azure. Commands. CosmosDB. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="57371-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="57371-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57371-114">-DefaultProfile</span></span>
<span data-ttu-id="57371-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57371-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57371-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="57371-116">-ExcludedPath</span></span>
<span data-ttu-id="57371-117">Array von Zeichenfolgen mit excludedPath (gibt einen Pfad in einem JSON-Dokument an, der im Azure Cosmos DB-Dienst ausgeschlossen werden soll)  Elemente.</span><span class="sxs-lookup"><span data-stu-id="57371-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="57371-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="57371-118">-IncludedPath</span></span>
<span data-ttu-id="57371-119">Array von Zeichenfolgen mit includedPath (gibt einen Pfad in einem JSON-Dokument an, der in die Azure Cosmos DB Service.)-Elemente eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="57371-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="57371-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="57371-120">-IndexingMode</span></span>
<span data-ttu-id="57371-121">Gibt den Indizierungs Modus an.</span><span class="sxs-lookup"><span data-stu-id="57371-121">indicates the indexing mode.</span></span>
<span data-ttu-id="57371-122">Mögliche Werte sind "konsistent", "faul", "keine".</span><span class="sxs-lookup"><span data-stu-id="57371-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="57371-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="57371-123">-SpatialSpec</span></span>
<span data-ttu-id="57371-124">Array von Objekten des Typs "Microsoft. Azure. Commands. CosmosDB. PSSpatialSpec"</span><span class="sxs-lookup"><span data-stu-id="57371-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="57371-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57371-125">CommonParameters</span></span>
<span data-ttu-id="57371-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57371-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57371-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57371-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57371-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57371-128">INPUTS</span></span>

### <span data-ttu-id="57371-129">Keine</span><span class="sxs-lookup"><span data-stu-id="57371-129">None</span></span>

## <span data-ttu-id="57371-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57371-130">OUTPUTS</span></span>

### <span data-ttu-id="57371-131">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="57371-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="57371-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="57371-132">NOTES</span></span>

## <span data-ttu-id="57371-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57371-133">RELATED LINKS</span></span>
