---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472821"
---
# <span data-ttu-id="52642-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="52642-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="52642-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52642-102">SYNOPSIS</span></span>
<span data-ttu-id="52642-103">Erstellt ein neues Objekt vom Typ "PSSpatialSpec".</span><span class="sxs-lookup"><span data-stu-id="52642-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="52642-104">Sie kann als Parameterwert für "Set-AzCosmosDBGremlinIndexingPolicy" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="52642-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="52642-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52642-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52642-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52642-106">DESCRIPTION</span></span>
<span data-ttu-id="52642-107">Erstellt ein Objekt, das der "SpatialSpec" der Gremlin-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="52642-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="52642-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="52642-108">EXAMPLES</span></span>

### <span data-ttu-id="52642-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="52642-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="52642-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52642-110">PARAMETERS</span></span>

### <span data-ttu-id="52642-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52642-111">-DefaultProfile</span></span>
<span data-ttu-id="52642-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52642-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52642-113">-Path</span><span class="sxs-lookup"><span data-stu-id="52642-113">-Path</span></span>
<span data-ttu-id="52642-114">Pfad im JSON-Dokument, der indiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="52642-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="52642-115">-Type</span><span class="sxs-lookup"><span data-stu-id="52642-115">-Type</span></span>
<span data-ttu-id="52642-116">Array von Zeichenfolgen mit akzeptablen Werten: Punkt, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="52642-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="52642-117">Stellen Sie die Pfade des räumlichen Typs dar.</span><span class="sxs-lookup"><span data-stu-id="52642-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="52642-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52642-118">CommonParameters</span></span>
<span data-ttu-id="52642-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52642-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52642-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52642-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52642-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="52642-121">INPUTS</span></span>

### <span data-ttu-id="52642-122">Keine</span><span class="sxs-lookup"><span data-stu-id="52642-122">None</span></span>

## <span data-ttu-id="52642-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="52642-123">OUTPUTS</span></span>

### <span data-ttu-id="52642-124">Microsoft.Azure.Commands.DiesDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="52642-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="52642-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="52642-125">NOTES</span></span>

## <span data-ttu-id="52642-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="52642-126">RELATED LINKS</span></span>
