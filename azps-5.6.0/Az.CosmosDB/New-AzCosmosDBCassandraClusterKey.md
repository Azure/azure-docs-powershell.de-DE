---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: 9afcffc281c48e0235c814b352e65ae47e5f4337
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947488"
---
# <span data-ttu-id="c756f-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="c756f-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="c756f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c756f-102">SYNOPSIS</span></span>
<span data-ttu-id="c756f-103">Erstellt einen neuen CosmosDB-Kassandra-Clusterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="c756f-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="c756f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c756f-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c756f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c756f-105">DESCRIPTION</span></span>
<span data-ttu-id="c756f-106">Der **New-AzCosmosDBCassandraClusterKey** erstellt einen neuen CosmosDB-Kassandra-Clusterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="c756f-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="c756f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c756f-107">EXAMPLES</span></span>

### <span data-ttu-id="c756f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c756f-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="c756f-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c756f-109">PARAMETERS</span></span>

### <span data-ttu-id="c756f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c756f-110">-DefaultProfile</span></span>
<span data-ttu-id="c756f-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c756f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c756f-112">-Name</span><span class="sxs-lookup"><span data-stu-id="c756f-112">-Name</span></span>
<span data-ttu-id="c756f-113">Name des Kassandra-Clusterschlüssels.</span><span class="sxs-lookup"><span data-stu-id="c756f-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="c756f-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="c756f-114">-OrderBy</span></span>
<span data-ttu-id="c756f-115">Bestellung des Schlüssels für den Kassandra-Cluster.</span><span class="sxs-lookup"><span data-stu-id="c756f-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="c756f-116">Mögliche Werte sind: "Asc", "Desc"</span><span class="sxs-lookup"><span data-stu-id="c756f-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="c756f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c756f-117">CommonParameters</span></span>
<span data-ttu-id="c756f-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c756f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c756f-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c756f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c756f-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c756f-120">INPUTS</span></span>

### <span data-ttu-id="c756f-121">Keine</span><span class="sxs-lookup"><span data-stu-id="c756f-121">None</span></span>

## <span data-ttu-id="c756f-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c756f-122">OUTPUTS</span></span>

### <span data-ttu-id="c756f-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="c756f-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="c756f-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c756f-124">NOTES</span></span>

## <span data-ttu-id="c756f-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c756f-125">RELATED LINKS</span></span>
