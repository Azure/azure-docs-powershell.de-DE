---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472803"
---
# <span data-ttu-id="3a1b4-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="3a1b4-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="3a1b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a1b4-102">SYNOPSIS</span></span>
<span data-ttu-id="3a1b4-103">Erstellt ein neues SqlUniqueKeyPolicy-Objekt aus".</span><span class="sxs-lookup"><span data-stu-id="3a1b4-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="3a1b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a1b4-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a1b4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a1b4-105">DESCRIPTION</span></span>
<span data-ttu-id="3a1b4-106">Das **Cmdlet "New-AzCosmosDBSqlUniqueKeyPolicy"** erstellt ein neues Objekt vom Typ "PSSqlUniqueKeyPolicy".</span><span class="sxs-lookup"><span data-stu-id="3a1b4-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="3a1b4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a1b4-107">EXAMPLES</span></span>

### <span data-ttu-id="3a1b4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3a1b4-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="3a1b4-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a1b4-109">PARAMETERS</span></span>

### <span data-ttu-id="3a1b4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a1b4-110">-DefaultProfile</span></span>
<span data-ttu-id="3a1b4-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a1b4-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="3a1b4-112">-UniqueKey</span></span>
<span data-ttu-id="3a1b4-113">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-113">Database name.</span></span>

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

### <span data-ttu-id="3a1b4-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a1b4-114">CommonParameters</span></span>
<span data-ttu-id="3a1b4-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a1b4-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a1b4-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a1b4-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a1b4-117">INPUTS</span></span>

### <span data-ttu-id="3a1b4-118">Keine</span><span class="sxs-lookup"><span data-stu-id="3a1b4-118">None</span></span>

## <span data-ttu-id="3a1b4-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a1b4-119">OUTPUTS</span></span>

### <span data-ttu-id="3a1b4-120">Microsoft.Azure.Commands.DiesDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="3a1b4-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="3a1b4-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3a1b4-121">NOTES</span></span>

## <span data-ttu-id="3a1b4-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3a1b4-122">RELATED LINKS</span></span>
