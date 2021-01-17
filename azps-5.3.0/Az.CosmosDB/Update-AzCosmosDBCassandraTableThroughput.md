---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470689"
---
# <span data-ttu-id="489cb-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="489cb-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="489cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="489cb-102">SYNOPSIS</span></span>
<span data-ttu-id="489cb-103">Aktualisiert den Durchsatzwert einer Tabelle vom 1.</span><span class="sxs-lookup"><span data-stu-id="489cb-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="489cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="489cb-104">SYNTAX</span></span>

### <span data-ttu-id="489cb-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="489cb-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="489cb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="489cb-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="489cb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="489cb-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="489cb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="489cb-108">DESCRIPTION</span></span>
<span data-ttu-id="489cb-109">Aktualisiert den Durchsatzwert einer Tabelle vom 1.</span><span class="sxs-lookup"><span data-stu-id="489cb-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="489cb-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="489cb-110">EXAMPLES</span></span>

### <span data-ttu-id="489cb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="489cb-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="489cb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="489cb-112">PARAMETERS</span></span>

### <span data-ttu-id="489cb-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="489cb-113">-AccountName</span></span>
<span data-ttu-id="489cb-114">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="489cb-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="489cb-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="489cb-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="489cb-116">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="489cb-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="489cb-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="489cb-117">-Confirm</span></span>
<span data-ttu-id="489cb-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="489cb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="489cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="489cb-119">-DefaultProfile</span></span>
<span data-ttu-id="489cb-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="489cb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="489cb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="489cb-121">-InputObject</span></span>
<span data-ttu-id="489cb-122">Dieses Keyspaceobjekt.</span><span class="sxs-lookup"><span data-stu-id="489cb-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="489cb-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="489cb-123">-KeyspaceName</span></span>
<span data-ttu-id="489cb-124">Der Name des Schlüsselraums.</span><span class="sxs-lookup"><span data-stu-id="489cb-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="489cb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="489cb-125">-Name</span></span>
<span data-ttu-id="489cb-126">DestgensEr Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="489cb-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="489cb-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="489cb-127">-ParentObject</span></span>
<span data-ttu-id="489cb-128">Dieses Keyspaceobjekt.</span><span class="sxs-lookup"><span data-stu-id="489cb-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="489cb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="489cb-129">-ResourceGroupName</span></span>
<span data-ttu-id="489cb-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="489cb-130">Name of resource group.</span></span>

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

### <span data-ttu-id="489cb-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="489cb-131">-Throughput</span></span>
<span data-ttu-id="489cb-132">Der Durchsatz von Tastaturschlüsselspaces (RU/s).</span><span class="sxs-lookup"><span data-stu-id="489cb-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="489cb-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="489cb-133">Default value is 400.</span></span>

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

### <span data-ttu-id="489cb-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="489cb-134">-WhatIf</span></span>
<span data-ttu-id="489cb-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="489cb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="489cb-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="489cb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="489cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="489cb-137">CommonParameters</span></span>
<span data-ttu-id="489cb-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="489cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="489cb-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="489cb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="489cb-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="489cb-140">INPUTS</span></span>

### <span data-ttu-id="489cb-141">Microsoft.Azure.Commands.ExesDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="489cb-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="489cb-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="489cb-142">OUTPUTS</span></span>

### <span data-ttu-id="489cb-143">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="489cb-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="489cb-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="489cb-144">NOTES</span></span>

## <span data-ttu-id="489cb-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="489cb-145">RELATED LINKS</span></span>
