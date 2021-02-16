---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148540"
---
# <span data-ttu-id="495df-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="495df-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="495df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="495df-102">SYNOPSIS</span></span>
<span data-ttu-id="495df-103">Erstellt ein neues Objekt vom Typ "PSCompositePath".</span><span class="sxs-lookup"><span data-stu-id="495df-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="495df-104">Sie kann als Parameterwert für "Set-AzCosmosDBSqlContainer" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="495df-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="495df-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="495df-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="495df-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="495df-106">DESCRIPTION</span></span>
<span data-ttu-id="495df-107">Objekt, das dem ZusammengesetztPath-Objekt der Sql-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="495df-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="495df-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="495df-108">EXAMPLES</span></span>

### <span data-ttu-id="495df-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="495df-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="495df-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="495df-110">PARAMETERS</span></span>

### <span data-ttu-id="495df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495df-111">-DefaultProfile</span></span>
<span data-ttu-id="495df-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="495df-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="495df-113">-Order</span><span class="sxs-lookup"><span data-stu-id="495df-113">-Order</span></span>
<span data-ttu-id="495df-114">Ruft die Sortierreihenfolge für zusammengesetzte Pfade ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="495df-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="495df-115">Mögliche Werte sind: 'Ascending', 'Descending'</span><span class="sxs-lookup"><span data-stu-id="495df-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="495df-116">-Path</span><span class="sxs-lookup"><span data-stu-id="495df-116">-Path</span></span>
<span data-ttu-id="495df-117">Der Pfad, für den das Indizierungsverhalten gilt.</span><span class="sxs-lookup"><span data-stu-id="495df-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="495df-118">Indexpfade beginnen normalerweise mit Stamm und Ende mit Platzhalterzeichen (/Pfad/\*).</span><span class="sxs-lookup"><span data-stu-id="495df-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="495df-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495df-119">CommonParameters</span></span>
<span data-ttu-id="495df-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="495df-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495df-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="495df-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495df-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="495df-122">INPUTS</span></span>

### <span data-ttu-id="495df-123">Keine</span><span class="sxs-lookup"><span data-stu-id="495df-123">None</span></span>

## <span data-ttu-id="495df-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="495df-124">OUTPUTS</span></span>

### <span data-ttu-id="495df-125">Microsoft.Azure.Commands.DiesDB.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="495df-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="495df-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="495df-126">NOTES</span></span>

## <span data-ttu-id="495df-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="495df-127">RELATED LINKS</span></span>
