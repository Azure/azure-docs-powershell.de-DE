---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: c67627068ef2fc90f8322b2e8b63dd6cd68acbe3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946600"
---
# <span data-ttu-id="f7551-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7551-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="f7551-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7551-102">SYNOPSIS</span></span>
<span data-ttu-id="f7551-103">Erstellt ein neues Objekt vom Typ PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f7551-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="f7551-104">Sie kann als Parameterwert für Set-AzCosmosDBGremlinGraph übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="f7551-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="f7551-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7551-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7551-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7551-106">DESCRIPTION</span></span>
<span data-ttu-id="f7551-107">Objekt, das der ConflictResolutionPolicy der Gremlin-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="f7551-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="f7551-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7551-108">EXAMPLES</span></span>

### <span data-ttu-id="f7551-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7551-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="f7551-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f7551-110">PARAMETERS</span></span>

### <span data-ttu-id="f7551-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="f7551-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="f7551-112">Soll bereitgestellt werden, wenn der Typ benutzerdefinierter ist.</span><span class="sxs-lookup"><span data-stu-id="f7551-112">To be provided when the type is custom.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7551-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7551-113">-DefaultProfile</span></span>
<span data-ttu-id="f7551-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7551-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7551-115">-Path</span><span class="sxs-lookup"><span data-stu-id="f7551-115">-Path</span></span>
<span data-ttu-id="f7551-116">Wird bereitgestellt, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="f7551-116">To be provided when the type is LastWriterWins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7551-117">-Type</span><span class="sxs-lookup"><span data-stu-id="f7551-117">-Type</span></span>
<span data-ttu-id="f7551-118">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="f7551-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7551-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7551-119">CommonParameters</span></span>
<span data-ttu-id="f7551-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7551-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7551-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7551-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7551-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7551-122">INPUTS</span></span>

### <span data-ttu-id="f7551-123">Keine</span><span class="sxs-lookup"><span data-stu-id="f7551-123">None</span></span>

## <span data-ttu-id="f7551-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7551-124">OUTPUTS</span></span>

### <span data-ttu-id="f7551-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7551-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="f7551-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f7551-126">NOTES</span></span>

## <span data-ttu-id="f7551-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f7551-127">RELATED LINKS</span></span>
