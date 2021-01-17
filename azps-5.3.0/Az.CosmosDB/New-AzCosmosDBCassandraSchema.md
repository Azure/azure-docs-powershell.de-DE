---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470736"
---
# <span data-ttu-id="69a65-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="69a65-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="69a65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69a65-102">SYNOPSIS</span></span>
<span data-ttu-id="69a65-103">Erstellt ein neues Schema aus Demkka.</span><span class="sxs-lookup"><span data-stu-id="69a65-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="69a65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69a65-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69a65-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69a65-105">DESCRIPTION</span></span>
<span data-ttu-id="69a65-106">Das **neue Schema "New-AzCosmosDBCassschema"** erstellt ein neues Schema".</span><span class="sxs-lookup"><span data-stu-id="69a65-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="69a65-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69a65-107">EXAMPLES</span></span>

### <span data-ttu-id="69a65-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69a65-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="69a65-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69a65-109">PARAMETERS</span></span>

### <span data-ttu-id="69a65-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="69a65-110">-ClusterKey</span></span>
<span data-ttu-id="69a65-111">Array von PSClusterKey-Objekten.</span><span class="sxs-lookup"><span data-stu-id="69a65-111">Array of PSClusterKey objects.</span></span>

```yaml
Type: PSClusterKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a65-112">-Column</span><span class="sxs-lookup"><span data-stu-id="69a65-112">-Column</span></span>
<span data-ttu-id="69a65-113">"PSColumn"-Objekt.</span><span class="sxs-lookup"><span data-stu-id="69a65-113">PSColumn object.</span></span>

```yaml
Type: PSColumn[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a65-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a65-114">-DefaultProfile</span></span>
<span data-ttu-id="69a65-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69a65-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69a65-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="69a65-116">-PartitionKey</span></span>
<span data-ttu-id="69a65-117">Array von Zeichenfolgen, die Partition Keys enthalten.</span><span class="sxs-lookup"><span data-stu-id="69a65-117">Array of strings containing Partition Keys.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a65-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a65-118">CommonParameters</span></span>
<span data-ttu-id="69a65-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69a65-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a65-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69a65-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a65-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69a65-121">INPUTS</span></span>

### <span data-ttu-id="69a65-122">Keine</span><span class="sxs-lookup"><span data-stu-id="69a65-122">None</span></span>

## <span data-ttu-id="69a65-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69a65-123">OUTPUTS</span></span>

### <span data-ttu-id="69a65-124">Microsoft.Azure.Commands.DiesDB.Models.PSCassschemaSchema</span><span class="sxs-lookup"><span data-stu-id="69a65-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="69a65-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="69a65-125">NOTES</span></span>

## <span data-ttu-id="69a65-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="69a65-126">RELATED LINKS</span></span>
