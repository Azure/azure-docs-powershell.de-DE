---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 54f7a1cb17413fe9d6703dbd0e909555e0c3926a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921336"
---
# <span data-ttu-id="34ab0-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="34ab0-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="34ab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="34ab0-103">Erstellt ein neues CosmosDB UniqueKeyPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="34ab0-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="34ab0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34ab0-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34ab0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34ab0-105">DESCRIPTION</span></span>
<span data-ttu-id="34ab0-106">Das **Cmdlet New-AzCosmosDBGremlinUniqueKeyPolicy** erstellt ein neues Objekt vom Typ PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="34ab0-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="34ab0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="34ab0-107">EXAMPLES</span></span>

### <span data-ttu-id="34ab0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="34ab0-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="34ab0-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="34ab0-109">PARAMETERS</span></span>

### <span data-ttu-id="34ab0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ab0-110">-DefaultProfile</span></span>
<span data-ttu-id="34ab0-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34ab0-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34ab0-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="34ab0-112">-UniqueKey</span></span>
<span data-ttu-id="34ab0-113">Array von Objekten vom Typ PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="34ab0-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="34ab0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ab0-114">CommonParameters</span></span>
<span data-ttu-id="34ab0-115">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34ab0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ab0-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34ab0-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ab0-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="34ab0-117">INPUTS</span></span>

### <span data-ttu-id="34ab0-118">Keine</span><span class="sxs-lookup"><span data-stu-id="34ab0-118">None</span></span>

## <span data-ttu-id="34ab0-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="34ab0-119">OUTPUTS</span></span>

### <span data-ttu-id="34ab0-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="34ab0-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="34ab0-121">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="34ab0-121">NOTES</span></span>

## <span data-ttu-id="34ab0-122">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="34ab0-122">RELATED LINKS</span></span>
