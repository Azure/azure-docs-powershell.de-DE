---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: e5742cde3a39cb2bf7dc96b952b3129d353235f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935275"
---
# <span data-ttu-id="fc534-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="fc534-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="fc534-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc534-102">SYNOPSIS</span></span>
<span data-ttu-id="fc534-103">Erstellt ein neues Objekt vom Typ PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="fc534-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="fc534-104">Sie kann als Parameterwert für Set-AzCosmosDBSqlContainer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="fc534-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="fc534-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc534-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc534-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc534-106">DESCRIPTION</span></span>
<span data-ttu-id="fc534-107">Objekt, das der ConflictResolutionPolicy der Sql API entspricht.</span><span class="sxs-lookup"><span data-stu-id="fc534-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="fc534-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc534-108">EXAMPLES</span></span>

### <span data-ttu-id="fc534-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc534-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="fc534-110">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="fc534-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="fc534-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fc534-111">PARAMETERS</span></span>

### <span data-ttu-id="fc534-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="fc534-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="fc534-113">Soll bereitgestellt werden, wenn der Typ benutzerdefinierter ist.</span><span class="sxs-lookup"><span data-stu-id="fc534-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="fc534-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc534-114">-DefaultProfile</span></span>
<span data-ttu-id="fc534-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc534-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc534-116">-Path</span><span class="sxs-lookup"><span data-stu-id="fc534-116">-Path</span></span>
<span data-ttu-id="fc534-117">Wird bereitgestellt, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="fc534-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="fc534-118">-Type</span><span class="sxs-lookup"><span data-stu-id="fc534-118">-Type</span></span>
<span data-ttu-id="fc534-119">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="fc534-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="fc534-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc534-120">CommonParameters</span></span>
<span data-ttu-id="fc534-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc534-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc534-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc534-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc534-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc534-123">INPUTS</span></span>

### <span data-ttu-id="fc534-124">Keine</span><span class="sxs-lookup"><span data-stu-id="fc534-124">None</span></span>

## <span data-ttu-id="fc534-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc534-125">OUTPUTS</span></span>

### <span data-ttu-id="fc534-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="fc534-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="fc534-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fc534-127">NOTES</span></span>

## <span data-ttu-id="fc534-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fc534-128">RELATED LINKS</span></span>
