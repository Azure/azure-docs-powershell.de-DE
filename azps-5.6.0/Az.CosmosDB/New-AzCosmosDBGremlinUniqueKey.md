---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: b2984ffc8b2c268f5298d88e9dc64e0729798e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943040"
---
# <span data-ttu-id="529ce-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="529ce-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="529ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="529ce-102">SYNOPSIS</span></span>
<span data-ttu-id="529ce-103">Erstellt ein neues CosmosDB UniqueKeyPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="529ce-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="529ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="529ce-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="529ce-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="529ce-105">DESCRIPTION</span></span>
<span data-ttu-id="529ce-106">Das **Cmdlet New-AzCosmosDBGremlinUniqueKeyPolicy** erstellt ein neues Objekt vom Typ PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="529ce-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="529ce-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="529ce-107">EXAMPLES</span></span>

### <span data-ttu-id="529ce-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="529ce-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="529ce-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="529ce-109">PARAMETERS</span></span>

### <span data-ttu-id="529ce-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="529ce-110">-DefaultProfile</span></span>
<span data-ttu-id="529ce-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="529ce-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="529ce-112">-Path</span><span class="sxs-lookup"><span data-stu-id="529ce-112">-Path</span></span>
<span data-ttu-id="529ce-113">Array von Zeichenfolgen von Pfadwerten</span><span class="sxs-lookup"><span data-stu-id="529ce-113">Array of string of path values</span></span>

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

### <span data-ttu-id="529ce-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="529ce-114">CommonParameters</span></span>
<span data-ttu-id="529ce-115">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="529ce-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="529ce-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="529ce-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="529ce-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="529ce-117">INPUTS</span></span>

### <span data-ttu-id="529ce-118">Keine</span><span class="sxs-lookup"><span data-stu-id="529ce-118">None</span></span>

## <span data-ttu-id="529ce-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="529ce-119">OUTPUTS</span></span>

### <span data-ttu-id="529ce-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="529ce-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="529ce-121">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="529ce-121">NOTES</span></span>

## <span data-ttu-id="529ce-122">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="529ce-122">RELATED LINKS</span></span>
