---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470730"
---
# <span data-ttu-id="21a91-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="21a91-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="21a91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21a91-102">SYNOPSIS</span></span>
<span data-ttu-id="21a91-103">Erstellt ein neues Objekt vom Typ "PSIncludedPath".</span><span class="sxs-lookup"><span data-stu-id="21a91-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="21a91-104">Sie kann als Parameterwert für Set-AzCosmosDBGremlinGraph übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="21a91-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="21a91-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21a91-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21a91-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21a91-106">DESCRIPTION</span></span>
<span data-ttu-id="21a91-107">Objekt, das dem IncludedPath-Objekt der Gremlin-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="21a91-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="21a91-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21a91-108">EXAMPLES</span></span>

### <span data-ttu-id="21a91-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="21a91-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="21a91-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21a91-110">PARAMETERS</span></span>

### <span data-ttu-id="21a91-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a91-111">-DefaultProfile</span></span>
<span data-ttu-id="21a91-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21a91-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21a91-113">-Index</span><span class="sxs-lookup"><span data-stu-id="21a91-113">-Index</span></span>
<span data-ttu-id="21a91-114">Liste der Indizes für diesen Pfad</span><span class="sxs-lookup"><span data-stu-id="21a91-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="21a91-115">-Path</span><span class="sxs-lookup"><span data-stu-id="21a91-115">-Path</span></span>
<span data-ttu-id="21a91-116">Der Pfad, für den das Indizierungsverhalten gilt.</span><span class="sxs-lookup"><span data-stu-id="21a91-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="21a91-117">Indexpfade beginnen normalerweise mit Stamm und Ende mit Platzhalterzeichen (/Pfad/\*).</span><span class="sxs-lookup"><span data-stu-id="21a91-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="21a91-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a91-118">CommonParameters</span></span>
<span data-ttu-id="21a91-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a91-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a91-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21a91-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a91-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21a91-121">INPUTS</span></span>

### <span data-ttu-id="21a91-122">Keine</span><span class="sxs-lookup"><span data-stu-id="21a91-122">None</span></span>

## <span data-ttu-id="21a91-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21a91-123">OUTPUTS</span></span>

### <span data-ttu-id="21a91-124">Microsoft.Azure.Commands.DiesDB.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="21a91-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="21a91-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="21a91-125">NOTES</span></span>

## <span data-ttu-id="21a91-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="21a91-126">RELATED LINKS</span></span>
