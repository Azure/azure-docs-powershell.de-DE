---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293909"
---
# <span data-ttu-id="d87bf-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="d87bf-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="d87bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d87bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d87bf-103">Erstellt eine neue Spalte des UnternamensDB.</span><span class="sxs-lookup"><span data-stu-id="d87bf-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="d87bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d87bf-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d87bf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d87bf-105">DESCRIPTION</span></span>
<span data-ttu-id="d87bf-106">Die **Neue-AzCosmosDBCassenColumn** erstellt eine neue Spalte aus Demmerz.</span><span class="sxs-lookup"><span data-stu-id="d87bf-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="d87bf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d87bf-107">EXAMPLES</span></span>

### <span data-ttu-id="d87bf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d87bf-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="d87bf-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d87bf-109">PARAMETERS</span></span>

### <span data-ttu-id="d87bf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d87bf-110">-DefaultProfile</span></span>
<span data-ttu-id="d87bf-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d87bf-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d87bf-112">-Name</span><span class="sxs-lookup"><span data-stu-id="d87bf-112">-Name</span></span>
<span data-ttu-id="d87bf-113">Name der Spalte "Spalte VonSpalte".</span><span class="sxs-lookup"><span data-stu-id="d87bf-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="d87bf-114">-Type</span><span class="sxs-lookup"><span data-stu-id="d87bf-114">-Type</span></span>
<span data-ttu-id="d87bf-115">Typ der Spalte "Spalte VonSpalte".</span><span class="sxs-lookup"><span data-stu-id="d87bf-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="d87bf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87bf-116">CommonParameters</span></span>
<span data-ttu-id="d87bf-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d87bf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87bf-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d87bf-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87bf-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d87bf-119">INPUTS</span></span>

### <span data-ttu-id="d87bf-120">Keine</span><span class="sxs-lookup"><span data-stu-id="d87bf-120">None</span></span>

## <span data-ttu-id="d87bf-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d87bf-121">OUTPUTS</span></span>

### <span data-ttu-id="d87bf-122">Microsoft.Azure.Commands.DiesDB.Models.PSColumn</span><span class="sxs-lookup"><span data-stu-id="d87bf-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="d87bf-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d87bf-123">NOTES</span></span>

## <span data-ttu-id="d87bf-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d87bf-124">RELATED LINKS</span></span>
