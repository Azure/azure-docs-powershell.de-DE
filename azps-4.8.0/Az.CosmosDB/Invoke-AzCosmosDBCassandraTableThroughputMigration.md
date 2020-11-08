---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: b6199720d9ac59c608482632518b47829a7c0b9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175299"
---
# <span data-ttu-id="ecf70-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="ecf70-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="ecf70-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecf70-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf70-103">Verwenden Sie diese Vorgehensweise, um den AutoScale-Durchsatz auf manuellen Durchsatz zu migrieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="ecf70-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="ecf70-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecf70-104">SYNTAX</span></span>

### <span data-ttu-id="ecf70-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ecf70-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf70-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecf70-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf70-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecf70-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecf70-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecf70-108">DESCRIPTION</span></span>
<span data-ttu-id="ecf70-109">ThroughpyteType Parameter definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ecf70-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="ecf70-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecf70-110">EXAMPLES</span></span>

### <span data-ttu-id="ecf70-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ecf70-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="ecf70-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecf70-112">PARAMETERS</span></span>

### <span data-ttu-id="ecf70-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="ecf70-113">-AccountName</span></span>
<span data-ttu-id="ecf70-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="ecf70-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ecf70-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ecf70-115">-Confirm</span></span>
<span data-ttu-id="ecf70-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ecf70-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecf70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf70-117">-DefaultProfile</span></span>
<span data-ttu-id="ecf70-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ecf70-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecf70-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ecf70-119">-InputObject</span></span>
<span data-ttu-id="ecf70-120">Cassandra-Tabellenobjekt.</span><span class="sxs-lookup"><span data-stu-id="ecf70-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="ecf70-121">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="ecf70-121">-KeyspaceName</span></span>
<span data-ttu-id="ecf70-122">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="ecf70-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="ecf70-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ecf70-123">-Name</span></span>
<span data-ttu-id="ecf70-124">Cassandra-Tabellen Name.</span><span class="sxs-lookup"><span data-stu-id="ecf70-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="ecf70-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ecf70-125">-ParentObject</span></span>
<span data-ttu-id="ecf70-126">Cassandra-Keyspace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ecf70-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="ecf70-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf70-127">-ResourceGroupName</span></span>
<span data-ttu-id="ecf70-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ecf70-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ecf70-129">-Durchsatztyp</span><span class="sxs-lookup"><span data-stu-id="ecf70-129">-ThroughputType</span></span>
<span data-ttu-id="ecf70-130">Der durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecf70-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="ecf70-131">Mögliche Werte sind: AutoScale, manuell.</span><span class="sxs-lookup"><span data-stu-id="ecf70-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="ecf70-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecf70-132">-WhatIf</span></span>
<span data-ttu-id="ecf70-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ecf70-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecf70-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ecf70-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecf70-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf70-135">CommonParameters</span></span>
<span data-ttu-id="ecf70-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecf70-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf70-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecf70-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf70-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecf70-138">INPUTS</span></span>

### <span data-ttu-id="ecf70-139">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="ecf70-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="ecf70-140">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="ecf70-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="ecf70-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecf70-141">OUTPUTS</span></span>

### <span data-ttu-id="ecf70-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ecf70-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ecf70-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecf70-143">NOTES</span></span>

## <span data-ttu-id="ecf70-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecf70-144">RELATED LINKS</span></span>
