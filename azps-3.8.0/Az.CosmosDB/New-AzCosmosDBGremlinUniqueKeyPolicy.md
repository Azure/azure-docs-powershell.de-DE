---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 593e299a6d7a1aa8131848f6de5f6c7aec8bd8c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003851"
---
# <span data-ttu-id="7ae6a-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="7ae6a-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="7ae6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ae6a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae6a-103">Erstellt ein neues CosmosDB-UniqueKeyPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7ae6a-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="7ae6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ae6a-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ae6a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ae6a-105">DESCRIPTION</span></span>
<span data-ttu-id="7ae6a-106">Das Cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** erstellt ein neues Objekt vom Typ PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="7ae6a-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="7ae6a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ae6a-107">EXAMPLES</span></span>

### <span data-ttu-id="7ae6a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ae6a-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="7ae6a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ae6a-109">PARAMETERS</span></span>

### <span data-ttu-id="7ae6a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae6a-110">-DefaultProfile</span></span>
<span data-ttu-id="7ae6a-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ae6a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ae6a-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="7ae6a-112">-UniqueKey</span></span>
<span data-ttu-id="7ae6a-113">Array von Objekten vom Typ PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="7ae6a-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae6a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae6a-114">CommonParameters</span></span>
<span data-ttu-id="7ae6a-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae6a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae6a-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ae6a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae6a-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ae6a-117">INPUTS</span></span>

### <span data-ttu-id="7ae6a-118">Keine</span><span class="sxs-lookup"><span data-stu-id="7ae6a-118">None</span></span>

## <span data-ttu-id="7ae6a-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ae6a-119">OUTPUTS</span></span>

### <span data-ttu-id="7ae6a-120">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="7ae6a-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="7ae6a-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ae6a-121">NOTES</span></span>

## <span data-ttu-id="7ae6a-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ae6a-122">RELATED LINKS</span></span>
