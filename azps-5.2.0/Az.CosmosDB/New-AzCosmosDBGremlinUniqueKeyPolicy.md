---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303728"
---
# <span data-ttu-id="156c2-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="156c2-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="156c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="156c2-102">SYNOPSIS</span></span>
<span data-ttu-id="156c2-103">Erstellt ein neues "DessDB UniqueKeyPolicy"-Objekt.</span><span class="sxs-lookup"><span data-stu-id="156c2-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="156c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="156c2-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="156c2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="156c2-105">DESCRIPTION</span></span>
<span data-ttu-id="156c2-106">Das **Cmdlet "New-AzCosmosDBGremlinUniqueKeyPolicy"** erstellt ein neues Objekt vom Typ "PSUniqueKeyPolicy".</span><span class="sxs-lookup"><span data-stu-id="156c2-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="156c2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="156c2-107">EXAMPLES</span></span>

### <span data-ttu-id="156c2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="156c2-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="156c2-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="156c2-109">PARAMETERS</span></span>

### <span data-ttu-id="156c2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="156c2-110">-DefaultProfile</span></span>
<span data-ttu-id="156c2-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="156c2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="156c2-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="156c2-112">-UniqueKey</span></span>
<span data-ttu-id="156c2-113">Array von Objekten vom Typ PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="156c2-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="156c2-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156c2-114">CommonParameters</span></span>
<span data-ttu-id="156c2-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="156c2-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156c2-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="156c2-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156c2-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="156c2-117">INPUTS</span></span>

### <span data-ttu-id="156c2-118">Keine</span><span class="sxs-lookup"><span data-stu-id="156c2-118">None</span></span>

## <span data-ttu-id="156c2-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="156c2-119">OUTPUTS</span></span>

### <span data-ttu-id="156c2-120">Microsoft.Azure.Commands.UmsDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="156c2-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="156c2-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="156c2-121">NOTES</span></span>

## <span data-ttu-id="156c2-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="156c2-122">RELATED LINKS</span></span>
