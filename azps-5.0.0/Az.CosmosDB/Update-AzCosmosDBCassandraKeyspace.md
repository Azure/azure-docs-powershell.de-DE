---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299091"
---
# <span data-ttu-id="04543-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="04543-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="04543-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04543-102">SYNOPSIS</span></span>
<span data-ttu-id="04543-103">Aktualisiert den CosmosDB Cassandra-Keyspace.</span><span class="sxs-lookup"><span data-stu-id="04543-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="04543-104">Führt einen clientseitigen Patch-Vorgang durch, indem der vorhandene Keyspace gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="04543-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="04543-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04543-105">SYNTAX</span></span>

### <span data-ttu-id="04543-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="04543-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04543-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04543-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04543-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04543-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04543-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04543-109">DESCRIPTION</span></span>
<span data-ttu-id="04543-110">Aktualisiert den CosmosDB Cassandra-Keyspace.</span><span class="sxs-lookup"><span data-stu-id="04543-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="04543-111">Führt einen clientseitigen Patch-Vorgang durch, indem der vorhandene Keyspace gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="04543-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="04543-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04543-112">EXAMPLES</span></span>

### <span data-ttu-id="04543-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="04543-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="04543-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="04543-114">PARAMETERS</span></span>

### <span data-ttu-id="04543-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="04543-115">-AccountName</span></span>
<span data-ttu-id="04543-116">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="04543-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="04543-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="04543-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="04543-118">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="04543-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="04543-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="04543-119">-Confirm</span></span>
<span data-ttu-id="04543-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04543-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04543-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04543-121">-DefaultProfile</span></span>
<span data-ttu-id="04543-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="04543-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04543-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="04543-123">-InputObject</span></span>
<span data-ttu-id="04543-124">Cassandra-Keyspace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="04543-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="04543-125">-Name</span><span class="sxs-lookup"><span data-stu-id="04543-125">-Name</span></span>
<span data-ttu-id="04543-126">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="04543-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="04543-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="04543-127">-ParentObject</span></span>
<span data-ttu-id="04543-128">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="04543-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="04543-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04543-129">-ResourceGroupName</span></span>
<span data-ttu-id="04543-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="04543-130">Name of resource group.</span></span>

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

### <span data-ttu-id="04543-131">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="04543-131">-Throughput</span></span>
<span data-ttu-id="04543-132">Der Durchsatz des Cassandra-Keyspace (ru/s).</span><span class="sxs-lookup"><span data-stu-id="04543-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="04543-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="04543-133">Default value is 400.</span></span>

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

### <span data-ttu-id="04543-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04543-134">-WhatIf</span></span>
<span data-ttu-id="04543-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04543-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04543-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04543-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04543-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04543-137">CommonParameters</span></span>
<span data-ttu-id="04543-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04543-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04543-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04543-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04543-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04543-140">INPUTS</span></span>

### <span data-ttu-id="04543-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="04543-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="04543-142">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="04543-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="04543-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04543-143">OUTPUTS</span></span>

### <span data-ttu-id="04543-144">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="04543-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="04543-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="04543-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="04543-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="04543-146">NOTES</span></span>

## <span data-ttu-id="04543-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04543-147">RELATED LINKS</span></span>
