---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174826"
---
# <span data-ttu-id="17b9d-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="17b9d-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="17b9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="17b9d-103">Erstellt ein neues Objekt vom Typ PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="17b9d-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="17b9d-104">Sie kann als Parameterwert für "AzCosmosDBSqlIndexingPolicy" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="17b9d-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="17b9d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17b9d-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17b9d-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17b9d-106">DESCRIPTION</span></span>
<span data-ttu-id="17b9d-107">Erstellt ein Objekt, das dem SpatialSpec der SQL-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="17b9d-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="17b9d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17b9d-108">EXAMPLES</span></span>

### <span data-ttu-id="17b9d-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="17b9d-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="17b9d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="17b9d-110">PARAMETERS</span></span>

### <span data-ttu-id="17b9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b9d-111">-DefaultProfile</span></span>
<span data-ttu-id="17b9d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17b9d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17b9d-113">-Path</span><span class="sxs-lookup"><span data-stu-id="17b9d-113">-Path</span></span>
<span data-ttu-id="17b9d-114">Pfad im JSON-Dokument zum Indizieren.</span><span class="sxs-lookup"><span data-stu-id="17b9d-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="17b9d-115">-Typ</span><span class="sxs-lookup"><span data-stu-id="17b9d-115">-Type</span></span>
<span data-ttu-id="17b9d-116">Array von Zeichenfolgen mit akzeptablen Werten: Point, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="17b9d-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="17b9d-117">Stellen Sie die Pfade räumlicher Typ dar.</span><span class="sxs-lookup"><span data-stu-id="17b9d-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="17b9d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b9d-118">CommonParameters</span></span>
<span data-ttu-id="17b9d-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b9d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b9d-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17b9d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b9d-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17b9d-121">INPUTS</span></span>

### <span data-ttu-id="17b9d-122">Keine</span><span class="sxs-lookup"><span data-stu-id="17b9d-122">None</span></span>

## <span data-ttu-id="17b9d-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17b9d-123">OUTPUTS</span></span>

### <span data-ttu-id="17b9d-124">Microsoft. Azure. Commands. CosmosDB. Models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="17b9d-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="17b9d-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="17b9d-125">NOTES</span></span>

## <span data-ttu-id="17b9d-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17b9d-126">RELATED LINKS</span></span>
