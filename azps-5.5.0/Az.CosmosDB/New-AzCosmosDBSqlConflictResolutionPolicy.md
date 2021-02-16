---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166193"
---
# <span data-ttu-id="0b782-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b782-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="0b782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b782-102">SYNOPSIS</span></span>
<span data-ttu-id="0b782-103">Erstellt ein neues Objekt vom Typ "PSSqlConflictResolutionPolicy".</span><span class="sxs-lookup"><span data-stu-id="0b782-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="0b782-104">Sie kann als Parameterwert für "Set-AzCosmosDBSqlContainer" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="0b782-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="0b782-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b782-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b782-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b782-106">DESCRIPTION</span></span>
<span data-ttu-id="0b782-107">Objekt, das der ConflictResolutionPolicy-Funktion der Sql-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="0b782-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="0b782-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b782-108">EXAMPLES</span></span>

### <span data-ttu-id="0b782-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0b782-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="0b782-110">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="0b782-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="0b782-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b782-111">PARAMETERS</span></span>

### <span data-ttu-id="0b782-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="0b782-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="0b782-113">Wird bereitgestellt, wenn es sich um einen benutzerdefinierten Typ handelt.</span><span class="sxs-lookup"><span data-stu-id="0b782-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="0b782-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b782-114">-DefaultProfile</span></span>
<span data-ttu-id="0b782-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b782-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b782-116">-Path</span><span class="sxs-lookup"><span data-stu-id="0b782-116">-Path</span></span>
<span data-ttu-id="0b782-117">Wird bereitgestellt, wenn der Typ "LastWriterWins" ist.</span><span class="sxs-lookup"><span data-stu-id="0b782-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="0b782-118">-Type</span><span class="sxs-lookup"><span data-stu-id="0b782-118">-Type</span></span>
<span data-ttu-id="0b782-119">Kann die Werte haben: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="0b782-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="0b782-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b782-120">CommonParameters</span></span>
<span data-ttu-id="0b782-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b782-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b782-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b782-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b782-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b782-123">INPUTS</span></span>

### <span data-ttu-id="0b782-124">Keine</span><span class="sxs-lookup"><span data-stu-id="0b782-124">None</span></span>

## <span data-ttu-id="0b782-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b782-125">OUTPUTS</span></span>

### <span data-ttu-id="0b782-126">Microsoft.Azure.Commands.SkriptsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b782-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="0b782-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0b782-127">NOTES</span></span>

## <span data-ttu-id="0b782-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0b782-128">RELATED LINKS</span></span>
