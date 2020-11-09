---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299325"
---
# <span data-ttu-id="1ebc9-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="1ebc9-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="1ebc9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ebc9-102">SYNOPSIS</span></span>
<span data-ttu-id="1ebc9-103">Erstellt ein neues Objekt vom Typ PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="1ebc9-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="1ebc9-104">Sie kann als Parameterwert für "AzCosmosDBGremlinGraph" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1ebc9-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="1ebc9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ebc9-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ebc9-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ebc9-106">DESCRIPTION</span></span>
<span data-ttu-id="1ebc9-107">Das Objekt, das dem IncludedPath der Gremlin-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="1ebc9-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="1ebc9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ebc9-108">EXAMPLES</span></span>

### <span data-ttu-id="1ebc9-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1ebc9-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="1ebc9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ebc9-110">PARAMETERS</span></span>

### <span data-ttu-id="1ebc9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ebc9-111">-DefaultProfile</span></span>
<span data-ttu-id="1ebc9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ebc9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ebc9-113">-Index</span><span class="sxs-lookup"><span data-stu-id="1ebc9-113">-Index</span></span>
<span data-ttu-id="1ebc9-114">Liste der Indizes für diesen Pfad</span><span class="sxs-lookup"><span data-stu-id="1ebc9-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="1ebc9-115">-Path</span><span class="sxs-lookup"><span data-stu-id="1ebc9-115">-Path</span></span>
<span data-ttu-id="1ebc9-116">Der Pfad, auf den das Indizierungs Verhalten angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ebc9-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="1ebc9-117">Index Pfade beginnen in der Regel mit "root" und enden mit Platzhalter (/Pfad/\*).</span><span class="sxs-lookup"><span data-stu-id="1ebc9-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="1ebc9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ebc9-118">CommonParameters</span></span>
<span data-ttu-id="1ebc9-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ebc9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ebc9-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ebc9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ebc9-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ebc9-121">INPUTS</span></span>

### <span data-ttu-id="1ebc9-122">Keine</span><span class="sxs-lookup"><span data-stu-id="1ebc9-122">None</span></span>

## <span data-ttu-id="1ebc9-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ebc9-123">OUTPUTS</span></span>

### <span data-ttu-id="1ebc9-124">Microsoft. Azure. Commands. CosmosDB. Models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="1ebc9-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="1ebc9-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ebc9-125">NOTES</span></span>

## <span data-ttu-id="1ebc9-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ebc9-126">RELATED LINKS</span></span>
