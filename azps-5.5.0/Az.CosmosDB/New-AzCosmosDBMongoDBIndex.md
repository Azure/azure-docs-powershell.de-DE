---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164009"
---
# <span data-ttu-id="b80aa-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="b80aa-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="b80aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b80aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b80aa-103">Erstellt einen neuenDb MongoDB Index.</span><span class="sxs-lookup"><span data-stu-id="b80aa-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="b80aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b80aa-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b80aa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b80aa-105">DESCRIPTION</span></span>
<span data-ttu-id="b80aa-106">Der **Neue-AzCosmosDBMongoDBIndex** erstellt einen neuen DadurchsDB-MongoDB-Index.</span><span class="sxs-lookup"><span data-stu-id="b80aa-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="b80aa-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b80aa-107">EXAMPLES</span></span>

### <span data-ttu-id="b80aa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b80aa-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="b80aa-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b80aa-109">PARAMETERS</span></span>

### <span data-ttu-id="b80aa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b80aa-110">-DefaultProfile</span></span>
<span data-ttu-id="b80aa-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b80aa-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b80aa-112">-Key</span><span class="sxs-lookup"><span data-stu-id="b80aa-112">-Key</span></span>
<span data-ttu-id="b80aa-113">Array von Schlüsselwerten als Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="b80aa-113">Array of key values as strings.</span></span>

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

### <span data-ttu-id="b80aa-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="b80aa-114">-TtlInSeconds</span></span>
<span data-ttu-id="b80aa-115">Die Anzahl von Sekunden, nach der der Index abläuft.</span><span class="sxs-lookup"><span data-stu-id="b80aa-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="b80aa-116">-Eindeutig</span><span class="sxs-lookup"><span data-stu-id="b80aa-116">-Unique</span></span>
<span data-ttu-id="b80aa-117">Bool, um anzugeben, ob der Index eindeutig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="b80aa-117">Bool to indicate if the index is unique or not.</span></span>

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

### <span data-ttu-id="b80aa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b80aa-118">CommonParameters</span></span>
<span data-ttu-id="b80aa-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b80aa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b80aa-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b80aa-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b80aa-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b80aa-121">INPUTS</span></span>

### <span data-ttu-id="b80aa-122">Keine</span><span class="sxs-lookup"><span data-stu-id="b80aa-122">None</span></span>

## <span data-ttu-id="b80aa-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b80aa-123">OUTPUTS</span></span>

### <span data-ttu-id="b80aa-124">Microsoft.Azure.Commands.DiesDB.Models.PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="b80aa-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="b80aa-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b80aa-125">NOTES</span></span>

## <span data-ttu-id="b80aa-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b80aa-126">RELATED LINKS</span></span>
