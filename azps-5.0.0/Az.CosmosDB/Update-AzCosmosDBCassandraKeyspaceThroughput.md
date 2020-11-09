---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 43dcbd97047ef72104a3b000f760b49aa3dfaab6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299085"
---
# <span data-ttu-id="d919b-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="d919b-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="d919b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d919b-102">SYNOPSIS</span></span>
<span data-ttu-id="d919b-103">Aktualisiert den Durchsatz eines CosmosDB Cassandra-keyspaces.</span><span class="sxs-lookup"><span data-stu-id="d919b-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d919b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d919b-104">SYNTAX</span></span>

### <span data-ttu-id="d919b-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d919b-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d919b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d919b-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d919b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d919b-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d919b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d919b-108">DESCRIPTION</span></span>
<span data-ttu-id="d919b-109">Aktualisiert den Durchsatz eines CosmosDB Cassandra-keyspaces.</span><span class="sxs-lookup"><span data-stu-id="d919b-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d919b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d919b-110">EXAMPLES</span></span>

### <span data-ttu-id="d919b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d919b-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="d919b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d919b-112">PARAMETERS</span></span>

### <span data-ttu-id="d919b-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="d919b-113">-AccountName</span></span>
<span data-ttu-id="d919b-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="d919b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d919b-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d919b-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d919b-116">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d919b-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d919b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d919b-117">-Confirm</span></span>
<span data-ttu-id="d919b-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d919b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d919b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d919b-119">-DefaultProfile</span></span>
<span data-ttu-id="d919b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d919b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d919b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d919b-121">-InputObject</span></span>
<span data-ttu-id="d919b-122">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="d919b-122">CosmosDB Account object</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d919b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d919b-123">-Name</span></span>
<span data-ttu-id="d919b-124">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="d919b-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="d919b-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d919b-125">-ParentObject</span></span>
<span data-ttu-id="d919b-126">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="d919b-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d919b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d919b-127">-ResourceGroupName</span></span>
<span data-ttu-id="d919b-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d919b-128">Name of resource group.</span></span>

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

### <span data-ttu-id="d919b-129">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="d919b-129">-Throughput</span></span>
<span data-ttu-id="d919b-130">Der Durchsatz des Cassandra-Keyspace (ru/s).</span><span class="sxs-lookup"><span data-stu-id="d919b-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="d919b-131">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="d919b-131">Default value is 400.</span></span>

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

### <span data-ttu-id="d919b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d919b-132">-WhatIf</span></span>
<span data-ttu-id="d919b-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d919b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d919b-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d919b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d919b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d919b-135">CommonParameters</span></span>
<span data-ttu-id="d919b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d919b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d919b-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d919b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d919b-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d919b-138">INPUTS</span></span>

### <span data-ttu-id="d919b-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d919b-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d919b-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d919b-140">OUTPUTS</span></span>

### <span data-ttu-id="d919b-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d919b-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d919b-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="d919b-142">NOTES</span></span>

## <span data-ttu-id="d919b-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d919b-143">RELATED LINKS</span></span>
