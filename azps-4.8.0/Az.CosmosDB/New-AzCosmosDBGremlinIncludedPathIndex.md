---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 5d85baaa308b3a0c58f09f40797c3bb2dca4fabe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009946"
---
# <span data-ttu-id="1c264-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="1c264-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="1c264-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c264-102">SYNOPSIS</span></span>
<span data-ttu-id="1c264-103">Erstellt ein neues Objekt vom Typ PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="1c264-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="1c264-104">Sie kann als Parameterwert für "AzCosmosDBGremlinIncludedPath" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1c264-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="1c264-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c264-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c264-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c264-106">DESCRIPTION</span></span>
<span data-ttu-id="1c264-107">Das Objekt, das den IncludedPath's-Indizes der Gremlin-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="1c264-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="1c264-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c264-108">EXAMPLES</span></span>

### <span data-ttu-id="1c264-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1c264-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="1c264-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c264-110">PARAMETERS</span></span>

### <span data-ttu-id="1c264-111">-Datentyp</span><span class="sxs-lookup"><span data-stu-id="1c264-111">-DataType</span></span>
<span data-ttu-id="1c264-112">Der Datentyp, auf den das Indizierungs Verhalten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c264-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="1c264-113">Mögliche Werte sind: ' Zeichenfolge ', ' Zahl ', ' Punkt ', ' Polygon ', ' LineString ', ' MultiPolygon '</span><span class="sxs-lookup"><span data-stu-id="1c264-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="1c264-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c264-114">-DefaultProfile</span></span>
<span data-ttu-id="1c264-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1c264-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c264-116">-Art</span><span class="sxs-lookup"><span data-stu-id="1c264-116">-Kind</span></span>
<span data-ttu-id="1c264-117">Gibt den Typ des Indexes an.</span><span class="sxs-lookup"><span data-stu-id="1c264-117">Indicates the type of index.</span></span>
<span data-ttu-id="1c264-118">Mögliche Werte sind: "Hash", "Bereich", "räumlich"</span><span class="sxs-lookup"><span data-stu-id="1c264-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="1c264-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="1c264-119">-Precision</span></span>
<span data-ttu-id="1c264-120">Die Genauigkeit des Indexes.</span><span class="sxs-lookup"><span data-stu-id="1c264-120">The precision of the index.</span></span>
<span data-ttu-id="1c264-121">-1 ist die maximale Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="1c264-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="1c264-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c264-122">CommonParameters</span></span>
<span data-ttu-id="1c264-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c264-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c264-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c264-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c264-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c264-125">INPUTS</span></span>

### <span data-ttu-id="1c264-126">Keine</span><span class="sxs-lookup"><span data-stu-id="1c264-126">None</span></span>

## <span data-ttu-id="1c264-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c264-127">OUTPUTS</span></span>

### <span data-ttu-id="1c264-128">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexes</span><span class="sxs-lookup"><span data-stu-id="1c264-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="1c264-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c264-129">NOTES</span></span>

## <span data-ttu-id="1c264-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c264-130">RELATED LINKS</span></span>
