---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: c3022ea8f2ddbfbf0fc2a51bfd63706c4a8ea884
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921344"
---
# <span data-ttu-id="3ee00-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="3ee00-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="3ee00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ee00-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee00-103">Erstellt ein neues Objekt vom Typ PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="3ee00-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="3ee00-104">Sie kann als Parameterwert für Set-AzCosmosDBGremlinGraph übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="3ee00-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="3ee00-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ee00-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ee00-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ee00-106">DESCRIPTION</span></span>
<span data-ttu-id="3ee00-107">Objekt, das dem IncludedPath der Gremlin-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="3ee00-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="3ee00-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ee00-108">EXAMPLES</span></span>

### <span data-ttu-id="3ee00-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ee00-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="3ee00-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3ee00-110">PARAMETERS</span></span>

### <span data-ttu-id="3ee00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee00-111">-DefaultProfile</span></span>
<span data-ttu-id="3ee00-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ee00-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ee00-113">-Index</span><span class="sxs-lookup"><span data-stu-id="3ee00-113">-Index</span></span>
<span data-ttu-id="3ee00-114">Liste der Indizes für diesen Pfad</span><span class="sxs-lookup"><span data-stu-id="3ee00-114">List of indexes for this path</span></span>

```yaml
Type: PSIndexes[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee00-115">-Path</span><span class="sxs-lookup"><span data-stu-id="3ee00-115">-Path</span></span>
<span data-ttu-id="3ee00-116">Der Pfad, für den das Indizierungsverhalten gilt.</span><span class="sxs-lookup"><span data-stu-id="3ee00-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="3ee00-117">Indexpfade beginnen in der Regel mit Stamm und Enden mit Platzhalterzeichen (/pfad/\*)</span><span class="sxs-lookup"><span data-stu-id="3ee00-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="3ee00-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee00-118">CommonParameters</span></span>
<span data-ttu-id="3ee00-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee00-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee00-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ee00-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee00-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ee00-121">INPUTS</span></span>

### <span data-ttu-id="3ee00-122">Keine</span><span class="sxs-lookup"><span data-stu-id="3ee00-122">None</span></span>

## <span data-ttu-id="3ee00-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ee00-123">OUTPUTS</span></span>

### <span data-ttu-id="3ee00-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="3ee00-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="3ee00-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3ee00-125">NOTES</span></span>

## <span data-ttu-id="3ee00-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3ee00-126">RELATED LINKS</span></span>
