---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: 65b1cbaebdf4118b5e22a7d1f9672273281ba55b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939635"
---
# <span data-ttu-id="40ed5-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="40ed5-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="40ed5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="40ed5-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skalierung in den manuellen Durchsatz zu migrieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="40ed5-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="40ed5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40ed5-104">SYNTAX</span></span>

### <span data-ttu-id="40ed5-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="40ed5-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ed5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40ed5-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ed5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40ed5-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40ed5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40ed5-108">DESCRIPTION</span></span>
<span data-ttu-id="40ed5-109">ThroughpyteType-Paramter definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="40ed5-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="40ed5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40ed5-110">EXAMPLES</span></span>

### <span data-ttu-id="40ed5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40ed5-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="40ed5-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="40ed5-112">PARAMETERS</span></span>

### <span data-ttu-id="40ed5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40ed5-113">-AccountName</span></span>
<span data-ttu-id="40ed5-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="40ed5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="40ed5-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="40ed5-115">-Confirm</span></span>
<span data-ttu-id="40ed5-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40ed5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40ed5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ed5-117">-DefaultProfile</span></span>
<span data-ttu-id="40ed5-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40ed5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40ed5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40ed5-119">-InputObject</span></span>
<span data-ttu-id="40ed5-120">Das Objekt "Kassandratabelle".</span><span class="sxs-lookup"><span data-stu-id="40ed5-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="40ed5-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="40ed5-121">-KeyspaceName</span></span>
<span data-ttu-id="40ed5-122">Name des Kassa-Schlüsselbereichs.</span><span class="sxs-lookup"><span data-stu-id="40ed5-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="40ed5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="40ed5-123">-Name</span></span>
<span data-ttu-id="40ed5-124">Name der Tabelle "Kassandra".</span><span class="sxs-lookup"><span data-stu-id="40ed5-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="40ed5-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="40ed5-125">-ParentObject</span></span>
<span data-ttu-id="40ed5-126">Das Objekt "Kassandra-Keyspace".</span><span class="sxs-lookup"><span data-stu-id="40ed5-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="40ed5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40ed5-127">-ResourceGroupName</span></span>
<span data-ttu-id="40ed5-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="40ed5-128">Name of resource group.</span></span>

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

### <span data-ttu-id="40ed5-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="40ed5-129">-ThroughputType</span></span>
<span data-ttu-id="40ed5-130">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="40ed5-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="40ed5-131">Mögliche Werte sind: Automatische Skalierung, Manuell.</span><span class="sxs-lookup"><span data-stu-id="40ed5-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="40ed5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40ed5-132">-WhatIf</span></span>
<span data-ttu-id="40ed5-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40ed5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40ed5-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40ed5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40ed5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ed5-135">CommonParameters</span></span>
<span data-ttu-id="40ed5-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40ed5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ed5-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40ed5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ed5-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40ed5-138">INPUTS</span></span>

### <span data-ttu-id="40ed5-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="40ed5-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="40ed5-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="40ed5-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="40ed5-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40ed5-141">OUTPUTS</span></span>

### <span data-ttu-id="40ed5-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="40ed5-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="40ed5-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="40ed5-143">NOTES</span></span>

## <span data-ttu-id="40ed5-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="40ed5-144">RELATED LINKS</span></span>
