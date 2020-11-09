---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299277"
---
# <span data-ttu-id="840dc-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="840dc-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="840dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="840dc-102">SYNOPSIS</span></span>
<span data-ttu-id="840dc-103">Erstellt einen neuen CosmosDB-MongoDB-Index.</span><span class="sxs-lookup"><span data-stu-id="840dc-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="840dc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="840dc-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="840dc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="840dc-105">DESCRIPTION</span></span>
<span data-ttu-id="840dc-106">Die **AzCosmosDBMongoDBIndex** erstellt einen neuen CosmosDB-MongoDB-Index.</span><span class="sxs-lookup"><span data-stu-id="840dc-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="840dc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="840dc-107">EXAMPLES</span></span>

### <span data-ttu-id="840dc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="840dc-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="840dc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="840dc-109">PARAMETERS</span></span>

### <span data-ttu-id="840dc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="840dc-110">-DefaultProfile</span></span>
<span data-ttu-id="840dc-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="840dc-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="840dc-112">-Taste</span><span class="sxs-lookup"><span data-stu-id="840dc-112">-Key</span></span>
<span data-ttu-id="840dc-113">Array von Schlüsselwerten als Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="840dc-113">Array of key values as strings.</span></span>

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

### <span data-ttu-id="840dc-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="840dc-114">-TtlInSeconds</span></span>
<span data-ttu-id="840dc-115">Die Anzahl der Sekunden, nach denen der Index abläuft.</span><span class="sxs-lookup"><span data-stu-id="840dc-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="840dc-116">– Eindeutig</span><span class="sxs-lookup"><span data-stu-id="840dc-116">-Unique</span></span>
<span data-ttu-id="840dc-117">Bool, um anzugeben, ob der Index eindeutig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="840dc-117">Bool to indicate if the index is unique or not.</span></span>

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

### <span data-ttu-id="840dc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="840dc-118">CommonParameters</span></span>
<span data-ttu-id="840dc-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="840dc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="840dc-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="840dc-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="840dc-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="840dc-121">INPUTS</span></span>

### <span data-ttu-id="840dc-122">Keine</span><span class="sxs-lookup"><span data-stu-id="840dc-122">None</span></span>

## <span data-ttu-id="840dc-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="840dc-123">OUTPUTS</span></span>

### <span data-ttu-id="840dc-124">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="840dc-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="840dc-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="840dc-125">NOTES</span></span>

## <span data-ttu-id="840dc-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="840dc-126">RELATED LINKS</span></span>
