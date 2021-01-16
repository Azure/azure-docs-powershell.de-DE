---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: b6199720d9ac59c608482632518b47829a7c0b9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301787"
---
# <span data-ttu-id="0a20f-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="0a20f-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="0a20f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a20f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a20f-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skala in den manuellen Durchsatz und umgekehrt zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="0a20f-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="0a20f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a20f-104">SYNTAX</span></span>

### <span data-ttu-id="0a20f-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0a20f-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a20f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a20f-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a20f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a20f-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a20f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a20f-108">DESCRIPTION</span></span>
<span data-ttu-id="0a20f-109">Der ThroughpyteType-Parameterer definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0a20f-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="0a20f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0a20f-110">EXAMPLES</span></span>

### <span data-ttu-id="0a20f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a20f-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="0a20f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a20f-112">PARAMETERS</span></span>

### <span data-ttu-id="0a20f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0a20f-113">-AccountName</span></span>
<span data-ttu-id="0a20f-114">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="0a20f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0a20f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a20f-115">-Confirm</span></span>
<span data-ttu-id="0a20f-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a20f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a20f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a20f-117">-DefaultProfile</span></span>
<span data-ttu-id="0a20f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a20f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a20f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a20f-119">-InputObject</span></span>
<span data-ttu-id="0a20f-120">Das Objekt "Tabelle" aus Untere Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0a20f-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="0a20f-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="0a20f-121">-KeyspaceName</span></span>
<span data-ttu-id="0a20f-122">Name des Tastaturschlüssels.</span><span class="sxs-lookup"><span data-stu-id="0a20f-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="0a20f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0a20f-123">-Name</span></span>
<span data-ttu-id="0a20f-124">DestgensEr Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="0a20f-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="0a20f-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0a20f-125">-ParentObject</span></span>
<span data-ttu-id="0a20f-126">Dieses Keyspaceobjekt.</span><span class="sxs-lookup"><span data-stu-id="0a20f-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="0a20f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a20f-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a20f-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0a20f-128">Name of resource group.</span></span>

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

### <span data-ttu-id="0a20f-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="0a20f-129">-ThroughputType</span></span>
<span data-ttu-id="0a20f-130">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a20f-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="0a20f-131">Mögliche Werte sind: Autoskalieren, Manuell.</span><span class="sxs-lookup"><span data-stu-id="0a20f-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="0a20f-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0a20f-132">-WhatIf</span></span>
<span data-ttu-id="0a20f-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a20f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a20f-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a20f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a20f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a20f-135">CommonParameters</span></span>
<span data-ttu-id="0a20f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a20f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a20f-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a20f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a20f-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0a20f-138">INPUTS</span></span>

### <span data-ttu-id="0a20f-139">Microsoft.Azure.Commands.ExesDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="0a20f-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="0a20f-140">Microsoft.Azure.Commands.CassDB.Models.PSCassistenTableGetResults</span><span class="sxs-lookup"><span data-stu-id="0a20f-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="0a20f-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0a20f-141">OUTPUTS</span></span>

### <span data-ttu-id="0a20f-142">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0a20f-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0a20f-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0a20f-143">NOTES</span></span>

## <span data-ttu-id="0a20f-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0a20f-144">RELATED LINKS</span></span>
