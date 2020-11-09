---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299229"
---
# <span data-ttu-id="6efcf-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="6efcf-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="6efcf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6efcf-102">SYNOPSIS</span></span>
<span data-ttu-id="6efcf-103">Erstellt ein neues Objekt vom Typ PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="6efcf-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="6efcf-104">Sie kann als Parameterwert für "AzCosmosDBSqlIndexingPolicy" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="6efcf-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="6efcf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6efcf-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6efcf-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6efcf-106">DESCRIPTION</span></span>
<span data-ttu-id="6efcf-107">Erstellt ein Objekt, das dem SpatialSpec der SQL-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="6efcf-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="6efcf-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6efcf-108">EXAMPLES</span></span>

### <span data-ttu-id="6efcf-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6efcf-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="6efcf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6efcf-110">PARAMETERS</span></span>

### <span data-ttu-id="6efcf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6efcf-111">-DefaultProfile</span></span>
<span data-ttu-id="6efcf-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6efcf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6efcf-113">-Path</span><span class="sxs-lookup"><span data-stu-id="6efcf-113">-Path</span></span>
<span data-ttu-id="6efcf-114">Pfad im JSON-Dokument zum Indizieren.</span><span class="sxs-lookup"><span data-stu-id="6efcf-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="6efcf-115">-Typ</span><span class="sxs-lookup"><span data-stu-id="6efcf-115">-Type</span></span>
<span data-ttu-id="6efcf-116">Array von Zeichenfolgen mit akzeptablen Werten: Point, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="6efcf-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="6efcf-117">Stellen Sie die Pfade räumlicher Typ dar.</span><span class="sxs-lookup"><span data-stu-id="6efcf-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="6efcf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6efcf-118">CommonParameters</span></span>
<span data-ttu-id="6efcf-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6efcf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6efcf-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6efcf-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6efcf-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6efcf-121">INPUTS</span></span>

### <span data-ttu-id="6efcf-122">Keine</span><span class="sxs-lookup"><span data-stu-id="6efcf-122">None</span></span>

## <span data-ttu-id="6efcf-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6efcf-123">OUTPUTS</span></span>

### <span data-ttu-id="6efcf-124">Microsoft. Azure. Commands. CosmosDB. Models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="6efcf-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="6efcf-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="6efcf-125">NOTES</span></span>

## <span data-ttu-id="6efcf-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6efcf-126">RELATED LINKS</span></span>
