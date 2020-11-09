---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299313"
---
# <span data-ttu-id="f1735-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="f1735-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="f1735-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1735-102">SYNOPSIS</span></span>
<span data-ttu-id="f1735-103">Erstellt ein neues Objekt vom Typ PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="f1735-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="f1735-104">Sie kann als Parameterwert für "AzCosmosDBGremlinIndexingPolicy" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="f1735-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="f1735-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1735-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1735-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1735-106">DESCRIPTION</span></span>
<span data-ttu-id="f1735-107">Erstellt ein Objekt, das dem SpatialSpec der Gremlin-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="f1735-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="f1735-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1735-108">EXAMPLES</span></span>

### <span data-ttu-id="f1735-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1735-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="f1735-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1735-110">PARAMETERS</span></span>

### <span data-ttu-id="f1735-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1735-111">-DefaultProfile</span></span>
<span data-ttu-id="f1735-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1735-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1735-113">-Path</span><span class="sxs-lookup"><span data-stu-id="f1735-113">-Path</span></span>
<span data-ttu-id="f1735-114">Pfad im JSON-Dokument zum Indizieren.</span><span class="sxs-lookup"><span data-stu-id="f1735-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="f1735-115">-Typ</span><span class="sxs-lookup"><span data-stu-id="f1735-115">-Type</span></span>
<span data-ttu-id="f1735-116">Array von Zeichenfolgen mit akzeptablen Werten: Point, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="f1735-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="f1735-117">Stellen Sie die Pfade räumlicher Typ dar.</span><span class="sxs-lookup"><span data-stu-id="f1735-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="f1735-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1735-118">CommonParameters</span></span>
<span data-ttu-id="f1735-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1735-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1735-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1735-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1735-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1735-121">INPUTS</span></span>

### <span data-ttu-id="f1735-122">Keine</span><span class="sxs-lookup"><span data-stu-id="f1735-122">None</span></span>

## <span data-ttu-id="f1735-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1735-123">OUTPUTS</span></span>

### <span data-ttu-id="f1735-124">Microsoft. Azure. Commands. CosmosDB. Models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="f1735-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="f1735-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1735-125">NOTES</span></span>

## <span data-ttu-id="f1735-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1735-126">RELATED LINKS</span></span>
