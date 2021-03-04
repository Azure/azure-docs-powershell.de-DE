---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 989035c1478228eb8895a2f99779129c605b2f36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931323"
---
# <span data-ttu-id="e88ef-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="e88ef-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="e88ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e88ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e88ef-103">Aktualisiert den Durchsatzwert einer CosmosDB-Kassandratabelle.</span><span class="sxs-lookup"><span data-stu-id="e88ef-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="e88ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e88ef-104">SYNTAX</span></span>

### <span data-ttu-id="e88ef-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e88ef-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e88ef-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e88ef-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e88ef-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e88ef-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e88ef-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e88ef-108">DESCRIPTION</span></span>
<span data-ttu-id="e88ef-109">Aktualisiert den Durchsatzwert einer CosmosDB-Kassandratabelle.</span><span class="sxs-lookup"><span data-stu-id="e88ef-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="e88ef-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e88ef-110">EXAMPLES</span></span>

### <span data-ttu-id="e88ef-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e88ef-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="e88ef-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e88ef-112">PARAMETERS</span></span>

### <span data-ttu-id="e88ef-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e88ef-113">-AccountName</span></span>
<span data-ttu-id="e88ef-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="e88ef-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e88ef-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e88ef-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e88ef-116">Maximaler Durchsatzwert, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e88ef-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88ef-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e88ef-117">-Confirm</span></span>
<span data-ttu-id="e88ef-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e88ef-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88ef-119">-DefaultProfile</span></span>
<span data-ttu-id="e88ef-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e88ef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e88ef-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e88ef-121">-InputObject</span></span>
<span data-ttu-id="e88ef-122">Das Objekt "Kassandra-Keyspace".</span><span class="sxs-lookup"><span data-stu-id="e88ef-122">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e88ef-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="e88ef-123">-KeyspaceName</span></span>
<span data-ttu-id="e88ef-124">Name des Kassa-Schlüsselbereichs.</span><span class="sxs-lookup"><span data-stu-id="e88ef-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="e88ef-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e88ef-125">-Name</span></span>
<span data-ttu-id="e88ef-126">Name der Tabelle "Kassandra".</span><span class="sxs-lookup"><span data-stu-id="e88ef-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="e88ef-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e88ef-127">-ParentObject</span></span>
<span data-ttu-id="e88ef-128">Das Objekt "Kassandra-Keyspace".</span><span class="sxs-lookup"><span data-stu-id="e88ef-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="e88ef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e88ef-129">-ResourceGroupName</span></span>
<span data-ttu-id="e88ef-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e88ef-130">Name of resource group.</span></span>

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

### <span data-ttu-id="e88ef-131">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="e88ef-131">-Throughput</span></span>
<span data-ttu-id="e88ef-132">Der Durchsatz von Cassisy Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e88ef-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="e88ef-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="e88ef-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88ef-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e88ef-134">-WhatIf</span></span>
<span data-ttu-id="e88ef-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e88ef-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e88ef-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e88ef-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88ef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88ef-137">CommonParameters</span></span>
<span data-ttu-id="e88ef-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e88ef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88ef-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e88ef-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88ef-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e88ef-140">INPUTS</span></span>

### <span data-ttu-id="e88ef-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="e88ef-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="e88ef-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e88ef-142">OUTPUTS</span></span>

### <span data-ttu-id="e88ef-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e88ef-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e88ef-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e88ef-144">NOTES</span></span>

## <span data-ttu-id="e88ef-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e88ef-145">RELATED LINKS</span></span>
