---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470716"
---
# <span data-ttu-id="d251e-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="d251e-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="d251e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d251e-102">SYNOPSIS</span></span>
<span data-ttu-id="d251e-103">Erstellt ein neues Objekt vom Typ "PSCompositePath".</span><span class="sxs-lookup"><span data-stu-id="d251e-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="d251e-104">Sie kann als Parameterwert für "Set-AzCosmosDBSqlContainer" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="d251e-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="d251e-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d251e-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d251e-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d251e-106">DESCRIPTION</span></span>
<span data-ttu-id="d251e-107">Objekt, das dem ZusammengesetztPath-Objekt der Sql-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="d251e-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="d251e-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d251e-108">EXAMPLES</span></span>

### <span data-ttu-id="d251e-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d251e-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="d251e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d251e-110">PARAMETERS</span></span>

### <span data-ttu-id="d251e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d251e-111">-DefaultProfile</span></span>
<span data-ttu-id="d251e-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d251e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d251e-113">-Order</span><span class="sxs-lookup"><span data-stu-id="d251e-113">-Order</span></span>
<span data-ttu-id="d251e-114">Ruft die Sortierreihenfolge für zusammengesetzte Pfade ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="d251e-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="d251e-115">Mögliche Werte sind: 'Ascending', 'Descending'</span><span class="sxs-lookup"><span data-stu-id="d251e-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="d251e-116">-Path</span><span class="sxs-lookup"><span data-stu-id="d251e-116">-Path</span></span>
<span data-ttu-id="d251e-117">Der Pfad, für den das Indizierungsverhalten gilt.</span><span class="sxs-lookup"><span data-stu-id="d251e-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="d251e-118">Indexpfade beginnen normalerweise mit Stamm und Ende mit Platzhalterzeichen (/Pfad/\*).</span><span class="sxs-lookup"><span data-stu-id="d251e-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="d251e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d251e-119">CommonParameters</span></span>
<span data-ttu-id="d251e-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d251e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d251e-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d251e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d251e-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d251e-122">INPUTS</span></span>

### <span data-ttu-id="d251e-123">Keine</span><span class="sxs-lookup"><span data-stu-id="d251e-123">None</span></span>

## <span data-ttu-id="d251e-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d251e-124">OUTPUTS</span></span>

### <span data-ttu-id="d251e-125">Microsoft.Azure.Commands.DiesDB.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="d251e-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="d251e-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d251e-126">NOTES</span></span>

## <span data-ttu-id="d251e-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d251e-127">RELATED LINKS</span></span>
