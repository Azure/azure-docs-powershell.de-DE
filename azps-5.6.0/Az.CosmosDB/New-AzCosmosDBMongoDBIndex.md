---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: a086705465aea30480a4f41f6981a47d8fcc612c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938843"
---
# <span data-ttu-id="5693c-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="5693c-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="5693c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5693c-102">SYNOPSIS</span></span>
<span data-ttu-id="5693c-103">Erstellt einen neuen CosmosDB-MongoDB-Index.</span><span class="sxs-lookup"><span data-stu-id="5693c-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="5693c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5693c-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5693c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5693c-105">DESCRIPTION</span></span>
<span data-ttu-id="5693c-106">Der **New-AzCosmosDBMongoDBIndex** erstellt einen neuen CosmosDB-MongoDB-Index.</span><span class="sxs-lookup"><span data-stu-id="5693c-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="5693c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5693c-107">EXAMPLES</span></span>

### <span data-ttu-id="5693c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5693c-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="5693c-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5693c-109">PARAMETERS</span></span>

### <span data-ttu-id="5693c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5693c-110">-DefaultProfile</span></span>
<span data-ttu-id="5693c-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5693c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5693c-112">-Key</span><span class="sxs-lookup"><span data-stu-id="5693c-112">-Key</span></span>
<span data-ttu-id="5693c-113">Array von Schlüsselwerten als Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="5693c-113">Array of key values as strings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5693c-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="5693c-114">-TtlInSeconds</span></span>
<span data-ttu-id="5693c-115">Anzahl der Sekunden, nach denen der Index abläuft.</span><span class="sxs-lookup"><span data-stu-id="5693c-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="5693c-116">-Eindeutig</span><span class="sxs-lookup"><span data-stu-id="5693c-116">-Unique</span></span>
<span data-ttu-id="5693c-117">Bool, um anzugeben, ob der Index eindeutig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="5693c-117">Bool to indicate if the index is unique or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5693c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5693c-118">CommonParameters</span></span>
<span data-ttu-id="5693c-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5693c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5693c-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5693c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5693c-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5693c-121">INPUTS</span></span>

### <span data-ttu-id="5693c-122">Keine</span><span class="sxs-lookup"><span data-stu-id="5693c-122">None</span></span>

## <span data-ttu-id="5693c-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5693c-123">OUTPUTS</span></span>

### <span data-ttu-id="5693c-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="5693c-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="5693c-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5693c-125">NOTES</span></span>

## <span data-ttu-id="5693c-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5693c-126">RELATED LINKS</span></span>
