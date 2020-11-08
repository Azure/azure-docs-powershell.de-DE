---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995615"
---
# <span data-ttu-id="3f5b6-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="3f5b6-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="3f5b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f5b6-102">SYNOPSIS</span></span>
<span data-ttu-id="3f5b6-103">Erstellt ein neues CosmosDB-UniqueKeyPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3f5b6-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="3f5b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f5b6-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f5b6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f5b6-105">DESCRIPTION</span></span>
<span data-ttu-id="3f5b6-106">Das Cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** erstellt ein neues Objekt vom Typ PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="3f5b6-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="3f5b6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f5b6-107">EXAMPLES</span></span>

### <span data-ttu-id="3f5b6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3f5b6-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="3f5b6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f5b6-109">PARAMETERS</span></span>

### <span data-ttu-id="3f5b6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5b6-110">-DefaultProfile</span></span>
<span data-ttu-id="3f5b6-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f5b6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f5b6-112">-Path</span><span class="sxs-lookup"><span data-stu-id="3f5b6-112">-Path</span></span>
<span data-ttu-id="3f5b6-113">Array mit einer Zeichenfolge von Path-Werten</span><span class="sxs-lookup"><span data-stu-id="3f5b6-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5b6-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5b6-114">CommonParameters</span></span>
<span data-ttu-id="3f5b6-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f5b6-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5b6-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f5b6-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5b6-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f5b6-117">INPUTS</span></span>

### <span data-ttu-id="3f5b6-118">Keine</span><span class="sxs-lookup"><span data-stu-id="3f5b6-118">None</span></span>

## <span data-ttu-id="3f5b6-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f5b6-119">OUTPUTS</span></span>

### <span data-ttu-id="3f5b6-120">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="3f5b6-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="3f5b6-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f5b6-121">NOTES</span></span>

## <span data-ttu-id="3f5b6-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f5b6-122">RELATED LINKS</span></span>
