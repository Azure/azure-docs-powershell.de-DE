---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: a9d77cc76521eca1e99dac630673ef3825d1155b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923832"
---
# <span data-ttu-id="919bf-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="919bf-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="919bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="919bf-102">SYNOPSIS</span></span>
<span data-ttu-id="919bf-103">Erstellt ein neues Objekt vom Typ PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="919bf-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="919bf-104">Sie kann als Parameterwert für Set-AzCosmosDBSqlContainer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="919bf-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="919bf-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="919bf-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="919bf-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="919bf-106">DESCRIPTION</span></span>
<span data-ttu-id="919bf-107">Objekt, das dem IncludedPath der Sql-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="919bf-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="919bf-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="919bf-108">EXAMPLES</span></span>

### <span data-ttu-id="919bf-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="919bf-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="919bf-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="919bf-110">PARAMETERS</span></span>

### <span data-ttu-id="919bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="919bf-111">-DefaultProfile</span></span>
<span data-ttu-id="919bf-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="919bf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="919bf-113">-Index</span><span class="sxs-lookup"><span data-stu-id="919bf-113">-Index</span></span>
<span data-ttu-id="919bf-114">Liste der Indizes für diesen Pfad</span><span class="sxs-lookup"><span data-stu-id="919bf-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="919bf-115">-Path</span><span class="sxs-lookup"><span data-stu-id="919bf-115">-Path</span></span>
<span data-ttu-id="919bf-116">Der Pfad, für den das Indizierungsverhalten gilt.</span><span class="sxs-lookup"><span data-stu-id="919bf-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="919bf-117">Indexpfade beginnen in der Regel mit Stamm und Enden mit Platzhalterzeichen (/pfad/\*)</span><span class="sxs-lookup"><span data-stu-id="919bf-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="919bf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919bf-118">CommonParameters</span></span>
<span data-ttu-id="919bf-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="919bf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="919bf-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="919bf-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919bf-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="919bf-121">INPUTS</span></span>

### <span data-ttu-id="919bf-122">Keine</span><span class="sxs-lookup"><span data-stu-id="919bf-122">None</span></span>

## <span data-ttu-id="919bf-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="919bf-123">OUTPUTS</span></span>

### <span data-ttu-id="919bf-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="919bf-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="919bf-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="919bf-125">NOTES</span></span>

## <span data-ttu-id="919bf-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="919bf-126">RELATED LINKS</span></span>
