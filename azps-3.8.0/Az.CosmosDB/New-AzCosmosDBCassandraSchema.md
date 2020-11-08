---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995260"
---
# <span data-ttu-id="3428a-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="3428a-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="3428a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3428a-102">SYNOPSIS</span></span>
<span data-ttu-id="3428a-103">Erstellt ein neues CosmosDB-Cassandra-Schema.</span><span class="sxs-lookup"><span data-stu-id="3428a-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="3428a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3428a-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3428a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3428a-105">DESCRIPTION</span></span>
<span data-ttu-id="3428a-106">Das **New-AzCosmosDBCassandraSchema** erstellt ein neues CosmosDB-Cassandra-Schema.</span><span class="sxs-lookup"><span data-stu-id="3428a-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="3428a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3428a-107">EXAMPLES</span></span>

### <span data-ttu-id="3428a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3428a-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="3428a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3428a-109">PARAMETERS</span></span>

### <span data-ttu-id="3428a-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="3428a-110">-ClusterKey</span></span>
<span data-ttu-id="3428a-111">Array von PSClusterKey-Objekten.</span><span class="sxs-lookup"><span data-stu-id="3428a-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="3428a-112">-Column</span><span class="sxs-lookup"><span data-stu-id="3428a-112">-Column</span></span>
<span data-ttu-id="3428a-113">PSColumn-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3428a-113">PSColumn object.</span></span>

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

### <span data-ttu-id="3428a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3428a-114">-DefaultProfile</span></span>
<span data-ttu-id="3428a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3428a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3428a-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="3428a-116">-PartitionKey</span></span>
<span data-ttu-id="3428a-117">Array von Zeichenfolgen mit Partitions Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="3428a-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="3428a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3428a-118">CommonParameters</span></span>
<span data-ttu-id="3428a-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3428a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3428a-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3428a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3428a-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3428a-121">INPUTS</span></span>

### <span data-ttu-id="3428a-122">Keine</span><span class="sxs-lookup"><span data-stu-id="3428a-122">None</span></span>

## <span data-ttu-id="3428a-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3428a-123">OUTPUTS</span></span>

### <span data-ttu-id="3428a-124">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="3428a-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="3428a-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="3428a-125">NOTES</span></span>

## <span data-ttu-id="3428a-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3428a-126">RELATED LINKS</span></span>
