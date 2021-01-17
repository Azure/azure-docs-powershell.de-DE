---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302547"
---
# <span data-ttu-id="4c324-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="4c324-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="4c324-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c324-102">SYNOPSIS</span></span>
<span data-ttu-id="4c324-103">Erstellt einen neuen Clusterschlüssel aus Unternall.</span><span class="sxs-lookup"><span data-stu-id="4c324-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="4c324-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c324-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c324-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c324-105">DESCRIPTION</span></span>
<span data-ttu-id="4c324-106">Der **Neue-AzCosmosDBCasskonfigurationsclusterKey** erstellt einen neuen Clusterschlüssel aus Demkka.</span><span class="sxs-lookup"><span data-stu-id="4c324-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="4c324-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4c324-107">EXAMPLES</span></span>

### <span data-ttu-id="4c324-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4c324-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="4c324-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c324-109">PARAMETERS</span></span>

### <span data-ttu-id="4c324-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c324-110">-DefaultProfile</span></span>
<span data-ttu-id="4c324-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c324-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c324-112">-Name</span><span class="sxs-lookup"><span data-stu-id="4c324-112">-Name</span></span>
<span data-ttu-id="4c324-113">Name des Sternclusterschlüssels.</span><span class="sxs-lookup"><span data-stu-id="4c324-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="4c324-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="4c324-114">-OrderBy</span></span>
<span data-ttu-id="4c324-115">Sortierung des Clusterschlüssels aus Untereing.</span><span class="sxs-lookup"><span data-stu-id="4c324-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="4c324-116">Mögliche Werte sind: 'Asc', 'Desc'</span><span class="sxs-lookup"><span data-stu-id="4c324-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="4c324-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c324-117">CommonParameters</span></span>
<span data-ttu-id="4c324-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c324-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c324-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c324-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c324-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4c324-120">INPUTS</span></span>

### <span data-ttu-id="4c324-121">Keine</span><span class="sxs-lookup"><span data-stu-id="4c324-121">None</span></span>

## <span data-ttu-id="4c324-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4c324-122">OUTPUTS</span></span>

### <span data-ttu-id="4c324-123">Microsoft.Azure.Commands.UmsDB.Models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="4c324-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="4c324-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4c324-124">NOTES</span></span>

## <span data-ttu-id="4c324-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4c324-125">RELATED LINKS</span></span>
