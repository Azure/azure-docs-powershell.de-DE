---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299379"
---
# <span data-ttu-id="5e6f2-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="5e6f2-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="5e6f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="5e6f2-103">Erstellt einen neuen CosmosDB Cassandra-Keyspace.</span><span class="sxs-lookup"><span data-stu-id="5e6f2-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5e6f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e6f2-104">SYNTAX</span></span>

### <span data-ttu-id="5e6f2-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e6f2-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e6f2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e6f2-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e6f2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e6f2-107">DESCRIPTION</span></span>
<span data-ttu-id="5e6f2-108">Erstellt einen neuen CosmosDB Cassandra-Keyspace.</span><span class="sxs-lookup"><span data-stu-id="5e6f2-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5e6f2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e6f2-109">EXAMPLES</span></span>

### <span data-ttu-id="5e6f2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e6f2-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="5e6f2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e6f2-111">PARAMETERS</span></span>

### <span data-ttu-id="5e6f2-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="5e6f2-112">-AccountName</span></span>
<span data-ttu-id="5e6f2-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="5e6f2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5e6f2-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5e6f2-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5e6f2-115">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5e6f2-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5e6f2-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e6f2-116">-Confirm</span></span>
<span data-ttu-id="5e6f2-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e6f2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e6f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e6f2-118">-DefaultProfile</span></span>
<span data-ttu-id="5e6f2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e6f2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e6f2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5e6f2-120">-Name</span></span>
<span data-ttu-id="5e6f2-121">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="5e6f2-121">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e6f2-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e6f2-122">-ParentObject</span></span>
<span data-ttu-id="5e6f2-123">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="5e6f2-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5e6f2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e6f2-124">-ResourceGroupName</span></span>
<span data-ttu-id="5e6f2-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e6f2-125">Name of resource group.</span></span>

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

### <span data-ttu-id="5e6f2-126">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="5e6f2-126">-Throughput</span></span>
<span data-ttu-id="5e6f2-127">Der Durchsatz des Cassandra-Keyspace (ru/s).</span><span class="sxs-lookup"><span data-stu-id="5e6f2-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="5e6f2-128">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="5e6f2-128">Default value is 400.</span></span>

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

### <span data-ttu-id="5e6f2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e6f2-129">-WhatIf</span></span>
<span data-ttu-id="5e6f2-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e6f2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e6f2-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e6f2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e6f2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e6f2-132">CommonParameters</span></span>
<span data-ttu-id="5e6f2-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e6f2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e6f2-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e6f2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e6f2-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e6f2-135">INPUTS</span></span>

### <span data-ttu-id="5e6f2-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5e6f2-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5e6f2-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e6f2-137">OUTPUTS</span></span>

### <span data-ttu-id="5e6f2-138">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="5e6f2-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="5e6f2-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="5e6f2-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="5e6f2-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e6f2-140">NOTES</span></span>

## <span data-ttu-id="5e6f2-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e6f2-141">RELATED LINKS</span></span>
