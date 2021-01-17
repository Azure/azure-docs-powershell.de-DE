---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368457"
---
# <span data-ttu-id="8d7f4-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="8d7f4-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="8d7f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d7f4-102">SYNOPSIS</span></span>
<span data-ttu-id="8d7f4-103">Erstellt ein neues Schema aus Demkka.</span><span class="sxs-lookup"><span data-stu-id="8d7f4-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="8d7f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d7f4-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d7f4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d7f4-105">DESCRIPTION</span></span>
<span data-ttu-id="8d7f4-106">Das **neue Schema "New-AzCosmosDBCassschema"** erstellt ein neues Schema aus "DessDB Schema".</span><span class="sxs-lookup"><span data-stu-id="8d7f4-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="8d7f4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8d7f4-107">EXAMPLES</span></span>

### <span data-ttu-id="8d7f4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8d7f4-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="8d7f4-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d7f4-109">PARAMETERS</span></span>

### <span data-ttu-id="8d7f4-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="8d7f4-110">-ClusterKey</span></span>
<span data-ttu-id="8d7f4-111">Array von PSClusterKey-Objekten.</span><span class="sxs-lookup"><span data-stu-id="8d7f4-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="8d7f4-112">-Column</span><span class="sxs-lookup"><span data-stu-id="8d7f4-112">-Column</span></span>
<span data-ttu-id="8d7f4-113">"PSColumn"-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8d7f4-113">PSColumn object.</span></span>

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

### <span data-ttu-id="8d7f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d7f4-114">-DefaultProfile</span></span>
<span data-ttu-id="8d7f4-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d7f4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d7f4-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="8d7f4-116">-PartitionKey</span></span>
<span data-ttu-id="8d7f4-117">Array von Zeichenfolgen, die Partition Keys enthalten.</span><span class="sxs-lookup"><span data-stu-id="8d7f4-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="8d7f4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d7f4-118">CommonParameters</span></span>
<span data-ttu-id="8d7f4-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d7f4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d7f4-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d7f4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d7f4-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8d7f4-121">INPUTS</span></span>

### <span data-ttu-id="8d7f4-122">Keine</span><span class="sxs-lookup"><span data-stu-id="8d7f4-122">None</span></span>

## <span data-ttu-id="8d7f4-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8d7f4-123">OUTPUTS</span></span>

### <span data-ttu-id="8d7f4-124">Microsoft.Azure.Commands.DiesDB.Models.PSCassschemaSchema</span><span class="sxs-lookup"><span data-stu-id="8d7f4-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="8d7f4-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8d7f4-125">NOTES</span></span>

## <span data-ttu-id="8d7f4-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8d7f4-126">RELATED LINKS</span></span>
