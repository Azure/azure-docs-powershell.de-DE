---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003848"
---
# <span data-ttu-id="16680-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="16680-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="16680-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16680-102">SYNOPSIS</span></span>
<span data-ttu-id="16680-103">Erstellt ein neues Objekt vom Typ PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="16680-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="16680-104">Sie kann als Parameterwert für "AzCosmosDBSqlContainer" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="16680-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="16680-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="16680-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16680-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16680-106">DESCRIPTION</span></span>
<span data-ttu-id="16680-107">Das Objekt, das dem ConflictResolutionPolicy der SQL-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="16680-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="16680-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16680-108">EXAMPLES</span></span>

### <span data-ttu-id="16680-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16680-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="16680-110">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="16680-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="16680-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="16680-111">PARAMETERS</span></span>

### <span data-ttu-id="16680-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="16680-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="16680-113">, Die bereitgestellt werden soll, wenn der Typ Benutzerdefiniert ist.</span><span class="sxs-lookup"><span data-stu-id="16680-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="16680-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16680-114">-DefaultProfile</span></span>
<span data-ttu-id="16680-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16680-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16680-116">-Path</span><span class="sxs-lookup"><span data-stu-id="16680-116">-Path</span></span>
<span data-ttu-id="16680-117">, Die bereitgestellt werden soll, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="16680-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="16680-118">-Typ</span><span class="sxs-lookup"><span data-stu-id="16680-118">-Type</span></span>
<span data-ttu-id="16680-119">Kann die Werte haben: LastWriterWins, Benutzerdefiniert, manuell.</span><span class="sxs-lookup"><span data-stu-id="16680-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="16680-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16680-120">CommonParameters</span></span>
<span data-ttu-id="16680-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16680-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16680-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16680-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16680-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16680-123">INPUTS</span></span>

### <span data-ttu-id="16680-124">Keine</span><span class="sxs-lookup"><span data-stu-id="16680-124">None</span></span>

## <span data-ttu-id="16680-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16680-125">OUTPUTS</span></span>

### <span data-ttu-id="16680-126">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="16680-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="16680-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="16680-127">NOTES</span></span>

## <span data-ttu-id="16680-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16680-128">RELATED LINKS</span></span>
