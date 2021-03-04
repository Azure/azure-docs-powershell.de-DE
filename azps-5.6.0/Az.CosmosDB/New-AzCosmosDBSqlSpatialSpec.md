---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: e22c8931cf70fba970e71b7a2d099cda725287d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945208"
---
# <span data-ttu-id="9f948-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="9f948-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="9f948-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f948-102">SYNOPSIS</span></span>
<span data-ttu-id="9f948-103">Erstellt ein neues Objekt vom Typ PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="9f948-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="9f948-104">Sie kann als Parameterwert für Set-AzCosmosDBSqlIndexingPolicy übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="9f948-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="9f948-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f948-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f948-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f948-106">DESCRIPTION</span></span>
<span data-ttu-id="9f948-107">Erstellt das Objekt, das dem SpatialSpec der Sql-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="9f948-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="9f948-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f948-108">EXAMPLES</span></span>

### <span data-ttu-id="9f948-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9f948-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="9f948-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9f948-110">PARAMETERS</span></span>

### <span data-ttu-id="9f948-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f948-111">-DefaultProfile</span></span>
<span data-ttu-id="9f948-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f948-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f948-113">-Path</span><span class="sxs-lookup"><span data-stu-id="9f948-113">-Path</span></span>
<span data-ttu-id="9f948-114">Pfad im JSON-Dokument zum Indizieren.</span><span class="sxs-lookup"><span data-stu-id="9f948-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="9f948-115">-Type</span><span class="sxs-lookup"><span data-stu-id="9f948-115">-Type</span></span>
<span data-ttu-id="9f948-116">Array von Zeichenfolgen mit akzeptablen Werten: Punkt, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="9f948-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="9f948-117">Stellen Sie die Pfade des räumlichen Typs dar.</span><span class="sxs-lookup"><span data-stu-id="9f948-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="9f948-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f948-118">CommonParameters</span></span>
<span data-ttu-id="9f948-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f948-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f948-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f948-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f948-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f948-121">INPUTS</span></span>

### <span data-ttu-id="9f948-122">Keine</span><span class="sxs-lookup"><span data-stu-id="9f948-122">None</span></span>

## <span data-ttu-id="9f948-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f948-123">OUTPUTS</span></span>

### <span data-ttu-id="9f948-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="9f948-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="9f948-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9f948-125">NOTES</span></span>

## <span data-ttu-id="9f948-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9f948-126">RELATED LINKS</span></span>
