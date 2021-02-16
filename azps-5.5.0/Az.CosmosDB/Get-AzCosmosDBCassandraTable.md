---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166281"
---
# <span data-ttu-id="5680d-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="5680d-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="5680d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5680d-102">SYNOPSIS</span></span>
<span data-ttu-id="5680d-103">Ruft eine Tabelle aus Unterndb Untertrat ab.</span><span class="sxs-lookup"><span data-stu-id="5680d-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="5680d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5680d-104">SYNTAX</span></span>

### <span data-ttu-id="5680d-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5680d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5680d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5680d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5680d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5680d-107">DESCRIPTION</span></span>
<span data-ttu-id="5680d-108">Das **Cmdlet "Get-AzCosmosDBCasstable"** erstellt ein neues oder aktualisiert einen vorhandenen Durchlauftastespace.</span><span class="sxs-lookup"><span data-stu-id="5680d-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5680d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5680d-109">EXAMPLES</span></span>

### <span data-ttu-id="5680d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5680d-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="5680d-111">{{ Get-AzCosmosDBCassandraTable ruft die Eigenschaften eines vorhandenen Tastaturschlüsselspaces ab.</span><span class="sxs-lookup"><span data-stu-id="5680d-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="5680d-112">Sie können die Ressource erweitern, um die Eigenschaften DefaultTtl, Schema, _etag, _ts, _rid zu erhalten.}}</span><span class="sxs-lookup"><span data-stu-id="5680d-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="5680d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5680d-113">PARAMETERS</span></span>

### <span data-ttu-id="5680d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5680d-114">-AccountName</span></span>
<span data-ttu-id="5680d-115">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="5680d-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5680d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5680d-116">-DefaultProfile</span></span>
<span data-ttu-id="5680d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5680d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5680d-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="5680d-118">-KeyspaceName</span></span>
<span data-ttu-id="5680d-119">Der Name des Schlüsselraums.</span><span class="sxs-lookup"><span data-stu-id="5680d-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5680d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5680d-120">-Name</span></span>
<span data-ttu-id="5680d-121">DestgensEr Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="5680d-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="5680d-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5680d-122">-ParentObject</span></span>
<span data-ttu-id="5680d-123">Dieses Keyspaceobjekt.</span><span class="sxs-lookup"><span data-stu-id="5680d-123">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5680d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5680d-124">-ResourceGroupName</span></span>
<span data-ttu-id="5680d-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5680d-125">Name of resource group.</span></span>

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

### <span data-ttu-id="5680d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5680d-126">CommonParameters</span></span>
<span data-ttu-id="5680d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5680d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5680d-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5680d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5680d-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5680d-129">INPUTS</span></span>

### <span data-ttu-id="5680d-130">Microsoft.Azure.Commands.ExesDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="5680d-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="5680d-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5680d-131">OUTPUTS</span></span>

### <span data-ttu-id="5680d-132">Microsoft.Azure.Commands.CassDB.Models.PSCassistenTableGetResults</span><span class="sxs-lookup"><span data-stu-id="5680d-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="5680d-133">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5680d-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5680d-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5680d-134">NOTES</span></span>

## <span data-ttu-id="5680d-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5680d-135">RELATED LINKS</span></span>
