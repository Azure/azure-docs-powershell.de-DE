---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003850"
---
# <span data-ttu-id="a88d2-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="a88d2-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="a88d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a88d2-102">SYNOPSIS</span></span>
<span data-ttu-id="a88d2-103">Erstellt ein neues Objekt vom Typ PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="a88d2-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="a88d2-104">Sie kann als Parameterwert für "AzCosmosDBSqlContainer" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="a88d2-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="a88d2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a88d2-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a88d2-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a88d2-106">DESCRIPTION</span></span>
<span data-ttu-id="a88d2-107">Das Objekt, das dem CompositePath der SQL-API entspricht.</span><span class="sxs-lookup"><span data-stu-id="a88d2-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="a88d2-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a88d2-108">EXAMPLES</span></span>

### <span data-ttu-id="a88d2-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a88d2-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="a88d2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a88d2-110">PARAMETERS</span></span>

### <span data-ttu-id="a88d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a88d2-111">-DefaultProfile</span></span>
<span data-ttu-id="a88d2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a88d2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a88d2-113">-Bestellung</span><span class="sxs-lookup"><span data-stu-id="a88d2-113">-Order</span></span>
<span data-ttu-id="a88d2-114">Ruft die Sortierreihenfolge für zusammengesetzte Pfade ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="a88d2-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="a88d2-115">Mögliche Werte sind: "Aufsteigend", "absteigend"</span><span class="sxs-lookup"><span data-stu-id="a88d2-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="a88d2-116">-Path</span><span class="sxs-lookup"><span data-stu-id="a88d2-116">-Path</span></span>
<span data-ttu-id="a88d2-117">Der Pfad, auf den das Indizierungs Verhalten angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a88d2-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="a88d2-118">Index Pfade beginnen in der Regel mit "root" und enden mit Platzhalter (/Pfad/\*).</span><span class="sxs-lookup"><span data-stu-id="a88d2-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="a88d2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a88d2-119">CommonParameters</span></span>
<span data-ttu-id="a88d2-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a88d2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a88d2-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a88d2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a88d2-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a88d2-122">INPUTS</span></span>

### <span data-ttu-id="a88d2-123">Keine</span><span class="sxs-lookup"><span data-stu-id="a88d2-123">None</span></span>

## <span data-ttu-id="a88d2-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a88d2-124">OUTPUTS</span></span>

### <span data-ttu-id="a88d2-125">Microsoft. Azure. Commands. CosmosDB. Models. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="a88d2-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="a88d2-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="a88d2-126">NOTES</span></span>

## <span data-ttu-id="a88d2-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a88d2-127">RELATED LINKS</span></span>
