---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: 6ef9e9b4fe2332af22bb8bdab1334096860f53ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936224"
---
# <span data-ttu-id="fd4c7-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="fd4c7-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="fd4c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd4c7-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4c7-103">Erstellt ein neues CosmosDB SqlUniqueKeyPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fd4c7-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="fd4c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd4c7-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd4c7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd4c7-105">DESCRIPTION</span></span>
<span data-ttu-id="fd4c7-106">Das **Cmdlet New-AzCosmosDBSqlUniqueKeyPolicy** erstellt ein neues Objekt vom Typ PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="fd4c7-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="fd4c7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd4c7-107">EXAMPLES</span></span>

### <span data-ttu-id="fd4c7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd4c7-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="fd4c7-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fd4c7-109">PARAMETERS</span></span>

### <span data-ttu-id="fd4c7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd4c7-110">-DefaultProfile</span></span>
<span data-ttu-id="fd4c7-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd4c7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd4c7-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="fd4c7-112">-UniqueKey</span></span>
<span data-ttu-id="fd4c7-113">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="fd4c7-113">Database name.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd4c7-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4c7-114">CommonParameters</span></span>
<span data-ttu-id="fd4c7-115">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd4c7-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4c7-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd4c7-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4c7-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd4c7-117">INPUTS</span></span>

### <span data-ttu-id="fd4c7-118">Keine</span><span class="sxs-lookup"><span data-stu-id="fd4c7-118">None</span></span>

## <span data-ttu-id="fd4c7-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd4c7-119">OUTPUTS</span></span>

### <span data-ttu-id="fd4c7-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="fd4c7-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="fd4c7-121">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fd4c7-121">NOTES</span></span>

## <span data-ttu-id="fd4c7-122">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fd4c7-122">RELATED LINKS</span></span>
