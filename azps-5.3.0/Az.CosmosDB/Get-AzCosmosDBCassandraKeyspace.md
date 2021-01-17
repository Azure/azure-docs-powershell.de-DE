---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472868"
---
# <span data-ttu-id="f7c37-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="f7c37-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="f7c37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7c37-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c37-103">Ruft einen Ausrinnen-Keyspace ab.</span><span class="sxs-lookup"><span data-stu-id="f7c37-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="f7c37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7c37-104">SYNTAX</span></span>

### <span data-ttu-id="f7c37-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7c37-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7c37-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7c37-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7c37-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7c37-107">DESCRIPTION</span></span>
<span data-ttu-id="f7c37-108">Das **Cmdlet "Get-AzCosmosDBCasskeyspace"** erstellt ein neues oder aktualisiert einen vorhandenen Durchlauftastenschlüssel.</span><span class="sxs-lookup"><span data-stu-id="f7c37-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="f7c37-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7c37-109">EXAMPLES</span></span>

### <span data-ttu-id="f7c37-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7c37-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="f7c37-111">Get-AzCosmosDBCassandraKeyspace ruft die Eigenschaften eines vorhandenen Tastaturschlüsselspaces ab.</span><span class="sxs-lookup"><span data-stu-id="f7c37-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="f7c37-112">Sie können die Ressource erweitern, um die Eigenschaften _etag, _ts und _rid zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f7c37-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="f7c37-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7c37-113">PARAMETERS</span></span>

### <span data-ttu-id="f7c37-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f7c37-114">-AccountName</span></span>
<span data-ttu-id="f7c37-115">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="f7c37-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f7c37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c37-116">-DefaultProfile</span></span>
<span data-ttu-id="f7c37-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7c37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7c37-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f7c37-118">-Name</span></span>
<span data-ttu-id="f7c37-119">Der Name des Schlüsselraums.</span><span class="sxs-lookup"><span data-stu-id="f7c37-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="f7c37-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f7c37-120">-ParentObject</span></span>
<span data-ttu-id="f7c37-121">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="f7c37-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f7c37-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7c37-122">-ResourceGroupName</span></span>
<span data-ttu-id="f7c37-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f7c37-123">Name of resource group.</span></span>

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

### <span data-ttu-id="f7c37-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c37-124">CommonParameters</span></span>
<span data-ttu-id="f7c37-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7c37-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c37-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7c37-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c37-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7c37-127">INPUTS</span></span>

### <span data-ttu-id="f7c37-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f7c37-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="f7c37-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7c37-129">OUTPUTS</span></span>

### <span data-ttu-id="f7c37-130">Microsoft.Azure.Commands.UmsDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="f7c37-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="f7c37-131">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f7c37-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f7c37-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7c37-132">NOTES</span></span>

## <span data-ttu-id="f7c37-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7c37-133">RELATED LINKS</span></span>
