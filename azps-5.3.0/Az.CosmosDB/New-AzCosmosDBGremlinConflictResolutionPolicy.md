---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472830"
---
# <span data-ttu-id="7ba9a-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ba9a-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="7ba9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ba9a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba9a-103">Erstellt ein neues Objekt vom Typ "PSConflictResolutionPolicy".</span><span class="sxs-lookup"><span data-stu-id="7ba9a-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="7ba9a-104">Sie kann als Parameterwert für "Set-AzCosmosDBGremlinGraph" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="7ba9a-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="7ba9a-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ba9a-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ba9a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ba9a-106">DESCRIPTION</span></span>
<span data-ttu-id="7ba9a-107">Objekt, das dem ConflictResolutionPolicy-Objekt der Gremlin-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="7ba9a-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="7ba9a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ba9a-108">EXAMPLES</span></span>

### <span data-ttu-id="7ba9a-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ba9a-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="7ba9a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ba9a-110">PARAMETERS</span></span>

### <span data-ttu-id="7ba9a-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="7ba9a-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="7ba9a-112">Wird bereitgestellt, wenn es sich um einen benutzerdefinierten Typ handelt.</span><span class="sxs-lookup"><span data-stu-id="7ba9a-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="7ba9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba9a-113">-DefaultProfile</span></span>
<span data-ttu-id="7ba9a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ba9a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ba9a-115">-Path</span><span class="sxs-lookup"><span data-stu-id="7ba9a-115">-Path</span></span>
<span data-ttu-id="7ba9a-116">Wird bereitgestellt, wenn der Typ "LastWriterWins" ist.</span><span class="sxs-lookup"><span data-stu-id="7ba9a-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="7ba9a-117">-Type</span><span class="sxs-lookup"><span data-stu-id="7ba9a-117">-Type</span></span>
<span data-ttu-id="7ba9a-118">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="7ba9a-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="7ba9a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba9a-119">CommonParameters</span></span>
<span data-ttu-id="7ba9a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba9a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba9a-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ba9a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba9a-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ba9a-122">INPUTS</span></span>

### <span data-ttu-id="7ba9a-123">Keine</span><span class="sxs-lookup"><span data-stu-id="7ba9a-123">None</span></span>

## <span data-ttu-id="7ba9a-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ba9a-124">OUTPUTS</span></span>

### <span data-ttu-id="7ba9a-125">Microsoft.Azure.Commands.Durchsdb.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ba9a-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="7ba9a-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7ba9a-126">NOTES</span></span>

## <span data-ttu-id="7ba9a-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7ba9a-127">RELATED LINKS</span></span>
