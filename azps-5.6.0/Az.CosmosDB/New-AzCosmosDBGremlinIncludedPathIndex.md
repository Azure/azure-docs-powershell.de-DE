---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 6c84004ffb267a5bc429bb242d3bc7245775d69b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943059"
---
# <span data-ttu-id="70108-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="70108-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="70108-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70108-102">SYNOPSIS</span></span>
<span data-ttu-id="70108-103">Erstellt ein neues Objekt vom Typ PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="70108-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="70108-104">Sie kann als Parameterwert für Set-AzCosmosDBGremlinIncludedPath übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="70108-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="70108-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70108-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70108-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70108-106">DESCRIPTION</span></span>
<span data-ttu-id="70108-107">Objekt, das den Indizes von IncludedPath der Gremlin-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="70108-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="70108-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70108-108">EXAMPLES</span></span>

### <span data-ttu-id="70108-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70108-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="70108-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="70108-110">PARAMETERS</span></span>

### <span data-ttu-id="70108-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="70108-111">-DataType</span></span>
<span data-ttu-id="70108-112">Datentyp, auf den das Indizierungsverhalten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="70108-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="70108-113">Mögliche Werte sind: "Zeichenfolge", "Zahl", "Punkt", "Polygon", "LineString", "MultiPolygon"</span><span class="sxs-lookup"><span data-stu-id="70108-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="70108-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70108-114">-DefaultProfile</span></span>
<span data-ttu-id="70108-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70108-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70108-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="70108-116">-Kind</span></span>
<span data-ttu-id="70108-117">Gibt den Indextyp an.</span><span class="sxs-lookup"><span data-stu-id="70108-117">Indicates the type of index.</span></span>
<span data-ttu-id="70108-118">Mögliche Werte sind: "Hash", "Bereich", "Räumliche"</span><span class="sxs-lookup"><span data-stu-id="70108-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="70108-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="70108-119">-Precision</span></span>
<span data-ttu-id="70108-120">Die Genauigkeit des Indexes.</span><span class="sxs-lookup"><span data-stu-id="70108-120">The precision of the index.</span></span>
<span data-ttu-id="70108-121">-1 ist die maximale Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="70108-121">-1 is maximum precision.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70108-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70108-122">CommonParameters</span></span>
<span data-ttu-id="70108-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70108-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70108-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70108-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70108-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70108-125">INPUTS</span></span>

### <span data-ttu-id="70108-126">Keine</span><span class="sxs-lookup"><span data-stu-id="70108-126">None</span></span>

## <span data-ttu-id="70108-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70108-127">OUTPUTS</span></span>

### <span data-ttu-id="70108-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span><span class="sxs-lookup"><span data-stu-id="70108-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="70108-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="70108-129">NOTES</span></span>

## <span data-ttu-id="70108-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="70108-130">RELATED LINKS</span></span>
