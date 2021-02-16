---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166196"
---
# <span data-ttu-id="a7713-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7713-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="a7713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7713-102">SYNOPSIS</span></span>
<span data-ttu-id="a7713-103">Erstellt ein neues Objekt vom Typ "PSConflictResolutionPolicy".</span><span class="sxs-lookup"><span data-stu-id="a7713-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="a7713-104">Sie kann als Parameterwert für "Set-AzCosmosDBGremlinGraph" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="a7713-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="a7713-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7713-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7713-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7713-106">DESCRIPTION</span></span>
<span data-ttu-id="a7713-107">Objekt, das dem ConflictResolutionPolicy-Objekt der Gremlin-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="a7713-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="a7713-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7713-108">EXAMPLES</span></span>

### <span data-ttu-id="a7713-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a7713-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="a7713-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7713-110">PARAMETERS</span></span>

### <span data-ttu-id="a7713-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="a7713-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="a7713-112">Wird bereitgestellt, wenn es sich um einen benutzerdefinierten Typ handelt.</span><span class="sxs-lookup"><span data-stu-id="a7713-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="a7713-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7713-113">-DefaultProfile</span></span>
<span data-ttu-id="a7713-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7713-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7713-115">-Path</span><span class="sxs-lookup"><span data-stu-id="a7713-115">-Path</span></span>
<span data-ttu-id="a7713-116">Wird bereitgestellt, wenn der Typ "LastWriterWins" ist.</span><span class="sxs-lookup"><span data-stu-id="a7713-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="a7713-117">-Type</span><span class="sxs-lookup"><span data-stu-id="a7713-117">-Type</span></span>
<span data-ttu-id="a7713-118">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="a7713-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="a7713-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7713-119">CommonParameters</span></span>
<span data-ttu-id="a7713-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7713-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7713-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7713-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7713-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7713-122">INPUTS</span></span>

### <span data-ttu-id="a7713-123">Keine</span><span class="sxs-lookup"><span data-stu-id="a7713-123">None</span></span>

## <span data-ttu-id="a7713-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7713-124">OUTPUTS</span></span>

### <span data-ttu-id="a7713-125">Microsoft.Azure.Commands.DiesDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7713-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="a7713-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a7713-126">NOTES</span></span>

## <span data-ttu-id="a7713-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a7713-127">RELATED LINKS</span></span>
