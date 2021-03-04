---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 3a19e0c60b5a32e1d1083b1afba55a8bf3045fe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934419"
---
# <span data-ttu-id="93eb3-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="93eb3-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="93eb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="93eb3-103">Erstellt ein neues CosmosDB-Kassierenschema.</span><span class="sxs-lookup"><span data-stu-id="93eb3-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="93eb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93eb3-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93eb3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93eb3-105">DESCRIPTION</span></span>
<span data-ttu-id="93eb3-106">Das **New-AzCosmosDBCassandraSchema erstellt** ein neues CosmosDB-Kassierenschema.</span><span class="sxs-lookup"><span data-stu-id="93eb3-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="93eb3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="93eb3-107">EXAMPLES</span></span>

### <span data-ttu-id="93eb3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="93eb3-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="93eb3-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="93eb3-109">PARAMETERS</span></span>

### <span data-ttu-id="93eb3-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="93eb3-110">-ClusterKey</span></span>
<span data-ttu-id="93eb3-111">Array von PSClusterKey-Objekten.</span><span class="sxs-lookup"><span data-stu-id="93eb3-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="93eb3-112">-Column</span><span class="sxs-lookup"><span data-stu-id="93eb3-112">-Column</span></span>
<span data-ttu-id="93eb3-113">PSColumn-Objekt.</span><span class="sxs-lookup"><span data-stu-id="93eb3-113">PSColumn object.</span></span>

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

### <span data-ttu-id="93eb3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93eb3-114">-DefaultProfile</span></span>
<span data-ttu-id="93eb3-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93eb3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93eb3-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="93eb3-116">-PartitionKey</span></span>
<span data-ttu-id="93eb3-117">Array von Zeichenfolgen, die Partitionsschlüssel enthalten.</span><span class="sxs-lookup"><span data-stu-id="93eb3-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="93eb3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93eb3-118">CommonParameters</span></span>
<span data-ttu-id="93eb3-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93eb3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93eb3-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93eb3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93eb3-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="93eb3-121">INPUTS</span></span>

### <span data-ttu-id="93eb3-122">Keine</span><span class="sxs-lookup"><span data-stu-id="93eb3-122">None</span></span>

## <span data-ttu-id="93eb3-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="93eb3-123">OUTPUTS</span></span>

### <span data-ttu-id="93eb3-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="93eb3-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="93eb3-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="93eb3-125">NOTES</span></span>

## <span data-ttu-id="93eb3-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="93eb3-126">RELATED LINKS</span></span>
