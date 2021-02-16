---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 43dcbd97047ef72104a3b000f760b49aa3dfaab6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144449"
---
# <span data-ttu-id="1a744-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="1a744-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="1a744-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a744-102">SYNOPSIS</span></span>
<span data-ttu-id="1a744-103">Aktualisiert den Durchsatzwert einesSpacesDB-Schlüsselspaces.</span><span class="sxs-lookup"><span data-stu-id="1a744-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1a744-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a744-104">SYNTAX</span></span>

### <span data-ttu-id="1a744-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1a744-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a744-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a744-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a744-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a744-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a744-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a744-108">DESCRIPTION</span></span>
<span data-ttu-id="1a744-109">Aktualisiert den Durchsatzwert einesSpacesDB-Schlüsselspaces.</span><span class="sxs-lookup"><span data-stu-id="1a744-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1a744-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a744-110">EXAMPLES</span></span>

### <span data-ttu-id="1a744-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1a744-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="1a744-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a744-112">PARAMETERS</span></span>

### <span data-ttu-id="1a744-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1a744-113">-AccountName</span></span>
<span data-ttu-id="1a744-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="1a744-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1a744-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="1a744-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1a744-116">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1a744-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1a744-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a744-117">-Confirm</span></span>
<span data-ttu-id="1a744-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a744-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a744-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a744-119">-DefaultProfile</span></span>
<span data-ttu-id="1a744-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a744-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a744-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a744-121">-InputObject</span></span>
<span data-ttu-id="1a744-122">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="1a744-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1a744-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1a744-123">-Name</span></span>
<span data-ttu-id="1a744-124">Der Name des Schlüsselraums.</span><span class="sxs-lookup"><span data-stu-id="1a744-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="1a744-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1a744-125">-ParentObject</span></span>
<span data-ttu-id="1a744-126">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="1a744-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1a744-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a744-127">-ResourceGroupName</span></span>
<span data-ttu-id="1a744-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1a744-128">Name of resource group.</span></span>

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

### <span data-ttu-id="1a744-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="1a744-129">-Throughput</span></span>
<span data-ttu-id="1a744-130">Der Durchsatz von Tastaturschlüsselspaces (RU/s).</span><span class="sxs-lookup"><span data-stu-id="1a744-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="1a744-131">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="1a744-131">Default value is 400.</span></span>

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

### <span data-ttu-id="1a744-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1a744-132">-WhatIf</span></span>
<span data-ttu-id="1a744-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a744-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a744-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a744-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a744-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a744-135">CommonParameters</span></span>
<span data-ttu-id="1a744-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a744-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a744-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a744-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a744-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a744-138">INPUTS</span></span>

### <span data-ttu-id="1a744-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1a744-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="1a744-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a744-140">OUTPUTS</span></span>

### <span data-ttu-id="1a744-141">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1a744-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1a744-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1a744-142">NOTES</span></span>

## <span data-ttu-id="1a744-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1a744-143">RELATED LINKS</span></span>
