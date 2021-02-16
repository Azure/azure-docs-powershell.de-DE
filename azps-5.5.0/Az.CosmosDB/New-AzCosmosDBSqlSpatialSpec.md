---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171029"
---
# <span data-ttu-id="e9412-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="e9412-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="e9412-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9412-102">SYNOPSIS</span></span>
<span data-ttu-id="e9412-103">Erstellt ein neues Objekt vom Typ "PSSpatialSpec".</span><span class="sxs-lookup"><span data-stu-id="e9412-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="e9412-104">Sie kann als Parameterwert für "Set-AzCosmosDBSqlIndexingPolicy" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e9412-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="e9412-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9412-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9412-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9412-106">DESCRIPTION</span></span>
<span data-ttu-id="e9412-107">Erstellt ein Objekt, das der Sql-API "SpatialSpec" entspricht.</span><span class="sxs-lookup"><span data-stu-id="e9412-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="e9412-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e9412-108">EXAMPLES</span></span>

### <span data-ttu-id="e9412-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e9412-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="e9412-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9412-110">PARAMETERS</span></span>

### <span data-ttu-id="e9412-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9412-111">-DefaultProfile</span></span>
<span data-ttu-id="e9412-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9412-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9412-113">-Path</span><span class="sxs-lookup"><span data-stu-id="e9412-113">-Path</span></span>
<span data-ttu-id="e9412-114">Pfad im JSON-Dokument, der indiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9412-114">Path in JSON document to index.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9412-115">-Type</span><span class="sxs-lookup"><span data-stu-id="e9412-115">-Type</span></span>
<span data-ttu-id="e9412-116">Array von Zeichenfolgen mit akzeptablen Werten: Punkt, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="e9412-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="e9412-117">Stellen Die Pfade des räumlichen Typs dar.</span><span class="sxs-lookup"><span data-stu-id="e9412-117">Represent's paths spatial type.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9412-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9412-118">CommonParameters</span></span>
<span data-ttu-id="e9412-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9412-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9412-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9412-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9412-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e9412-121">INPUTS</span></span>

### <span data-ttu-id="e9412-122">Keine</span><span class="sxs-lookup"><span data-stu-id="e9412-122">None</span></span>

## <span data-ttu-id="e9412-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e9412-123">OUTPUTS</span></span>

### <span data-ttu-id="e9412-124">Microsoft.Azure.Commands.DiesDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="e9412-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="e9412-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e9412-125">NOTES</span></span>

## <span data-ttu-id="e9412-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e9412-126">RELATED LINKS</span></span>
