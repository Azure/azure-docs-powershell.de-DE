---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008581"
---
# <span data-ttu-id="bdb8d-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="bdb8d-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="bdb8d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bdb8d-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb8d-103">Erstellt einen neuen CosmosDB-MongoDB-Index.</span><span class="sxs-lookup"><span data-stu-id="bdb8d-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="bdb8d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdb8d-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdb8d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdb8d-105">DESCRIPTION</span></span>
<span data-ttu-id="bdb8d-106">Die **AzCosmosDBMongoDBIndex** erstellt einen neuen CosmosDB-MongoDB-Index.</span><span class="sxs-lookup"><span data-stu-id="bdb8d-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="bdb8d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdb8d-107">EXAMPLES</span></span>

### <span data-ttu-id="bdb8d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bdb8d-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="bdb8d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdb8d-109">PARAMETERS</span></span>

### <span data-ttu-id="bdb8d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb8d-110">-DefaultProfile</span></span>
<span data-ttu-id="bdb8d-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bdb8d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdb8d-112">-Taste</span><span class="sxs-lookup"><span data-stu-id="bdb8d-112">-Key</span></span>
<span data-ttu-id="bdb8d-113">Array von Schlüsselwerten als Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="bdb8d-113">Array of key values as strings.</span></span>

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

### <span data-ttu-id="bdb8d-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="bdb8d-114">-TtlInSeconds</span></span>
<span data-ttu-id="bdb8d-115">Die Anzahl der Sekunden, nach denen der Index abläuft.</span><span class="sxs-lookup"><span data-stu-id="bdb8d-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="bdb8d-116">– Eindeutig</span><span class="sxs-lookup"><span data-stu-id="bdb8d-116">-Unique</span></span>
<span data-ttu-id="bdb8d-117">Bool, um anzugeben, ob der Index eindeutig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="bdb8d-117">Bool to indicate if the index is unique or not.</span></span>

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

### <span data-ttu-id="bdb8d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb8d-118">CommonParameters</span></span>
<span data-ttu-id="bdb8d-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdb8d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb8d-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdb8d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb8d-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bdb8d-121">INPUTS</span></span>

### <span data-ttu-id="bdb8d-122">Keine</span><span class="sxs-lookup"><span data-stu-id="bdb8d-122">None</span></span>

## <span data-ttu-id="bdb8d-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bdb8d-123">OUTPUTS</span></span>

### <span data-ttu-id="bdb8d-124">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="bdb8d-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="bdb8d-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="bdb8d-125">NOTES</span></span>

## <span data-ttu-id="bdb8d-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bdb8d-126">RELATED LINKS</span></span>
