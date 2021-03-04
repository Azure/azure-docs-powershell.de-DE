---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: fb387adafa1a1a71d9a42b09b8c7255955eccd9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931987"
---
# <span data-ttu-id="befe2-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="befe2-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="befe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="befe2-102">SYNOPSIS</span></span>
<span data-ttu-id="befe2-103">Ruft einen CosmosDB-Kassandra-Schlüsselspace ab.</span><span class="sxs-lookup"><span data-stu-id="befe2-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="befe2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="befe2-104">SYNTAX</span></span>

### <span data-ttu-id="befe2-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="befe2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="befe2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="befe2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="befe2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="befe2-107">DESCRIPTION</span></span>
<span data-ttu-id="befe2-108">Das **Get-AzCosmosDBCassandraKeyspace-Cmdlet** erstellt ein neues oder aktualisiert einen vorhandenen CosmosDB-Kassandra-Keyspace.</span><span class="sxs-lookup"><span data-stu-id="befe2-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="befe2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="befe2-109">EXAMPLES</span></span>

### <span data-ttu-id="befe2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="befe2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="befe2-111">Get-AzCosmosDBCassandraKeyspace ruft die Eigenschaften eines vorhandenen "Cassisykeyspace" ab.</span><span class="sxs-lookup"><span data-stu-id="befe2-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="befe2-112">Sie können die Ressource erweitern, um die Eigenschaften _etag, _ts _rid zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="befe2-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="befe2-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="befe2-113">PARAMETERS</span></span>

### <span data-ttu-id="befe2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="befe2-114">-AccountName</span></span>
<span data-ttu-id="befe2-115">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="befe2-115">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="befe2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="befe2-116">-DefaultProfile</span></span>
<span data-ttu-id="befe2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="befe2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="befe2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="befe2-118">-Name</span></span>
<span data-ttu-id="befe2-119">Name des Kassa-Schlüsselbereichs.</span><span class="sxs-lookup"><span data-stu-id="befe2-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="befe2-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="befe2-120">-ParentObject</span></span>
<span data-ttu-id="befe2-121">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="befe2-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="befe2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="befe2-122">-ResourceGroupName</span></span>
<span data-ttu-id="befe2-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="befe2-123">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="befe2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="befe2-124">CommonParameters</span></span>
<span data-ttu-id="befe2-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="befe2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="befe2-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="befe2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="befe2-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="befe2-127">INPUTS</span></span>

### <span data-ttu-id="befe2-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="befe2-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="befe2-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="befe2-129">OUTPUTS</span></span>

### <span data-ttu-id="befe2-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="befe2-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="befe2-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="befe2-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="befe2-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="befe2-132">NOTES</span></span>

## <span data-ttu-id="befe2-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="befe2-133">RELATED LINKS</span></span>
