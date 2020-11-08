---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167082"
---
# <span data-ttu-id="181f2-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="181f2-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="181f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="181f2-102">SYNOPSIS</span></span>
<span data-ttu-id="181f2-103">Erstellt ein neues Objekt vom Typ PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="181f2-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="181f2-104">Sie kann als Parameterwert für "AzCosmosDBGremlinGraph" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="181f2-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="181f2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="181f2-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="181f2-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="181f2-106">DESCRIPTION</span></span>
<span data-ttu-id="181f2-107">Das Objekt, das dem ConflictResolutionPolicy der Gremlin-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="181f2-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="181f2-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="181f2-108">EXAMPLES</span></span>

### <span data-ttu-id="181f2-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="181f2-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="181f2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="181f2-110">PARAMETERS</span></span>

### <span data-ttu-id="181f2-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="181f2-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="181f2-112">, Die bereitgestellt werden soll, wenn der Typ Benutzerdefiniert ist.</span><span class="sxs-lookup"><span data-stu-id="181f2-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="181f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181f2-113">-DefaultProfile</span></span>
<span data-ttu-id="181f2-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="181f2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="181f2-115">-Path</span><span class="sxs-lookup"><span data-stu-id="181f2-115">-Path</span></span>
<span data-ttu-id="181f2-116">, Die bereitgestellt werden soll, wenn der Typ LastWriterWins ist.</span><span class="sxs-lookup"><span data-stu-id="181f2-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="181f2-117">-Typ</span><span class="sxs-lookup"><span data-stu-id="181f2-117">-Type</span></span>
<span data-ttu-id="181f2-118">Kann die Werte haben: LastWriterWins, Benutzerdefiniert, manuell.</span><span class="sxs-lookup"><span data-stu-id="181f2-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="181f2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181f2-119">CommonParameters</span></span>
<span data-ttu-id="181f2-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="181f2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181f2-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="181f2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181f2-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="181f2-122">INPUTS</span></span>

### <span data-ttu-id="181f2-123">Keine</span><span class="sxs-lookup"><span data-stu-id="181f2-123">None</span></span>

## <span data-ttu-id="181f2-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="181f2-124">OUTPUTS</span></span>

### <span data-ttu-id="181f2-125">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="181f2-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="181f2-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="181f2-126">NOTES</span></span>

## <span data-ttu-id="181f2-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="181f2-127">RELATED LINKS</span></span>
