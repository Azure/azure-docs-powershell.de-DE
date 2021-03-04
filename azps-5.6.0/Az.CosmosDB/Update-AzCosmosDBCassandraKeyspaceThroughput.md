---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 34401fb2e6b18e2b4f68e15eb004e440f99a3858
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931336"
---
# <span data-ttu-id="955f3-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="955f3-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="955f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="955f3-102">SYNOPSIS</span></span>
<span data-ttu-id="955f3-103">Aktualisiert den Durchsatzwert eines CosmosDB-Kassandra-Schlüsselspaces.</span><span class="sxs-lookup"><span data-stu-id="955f3-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="955f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="955f3-104">SYNTAX</span></span>

### <span data-ttu-id="955f3-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="955f3-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955f3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="955f3-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955f3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="955f3-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="955f3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="955f3-108">DESCRIPTION</span></span>
<span data-ttu-id="955f3-109">Aktualisiert den Durchsatzwert eines CosmosDB-Kassandra-Schlüsselspaces.</span><span class="sxs-lookup"><span data-stu-id="955f3-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="955f3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="955f3-110">EXAMPLES</span></span>

### <span data-ttu-id="955f3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="955f3-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="955f3-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="955f3-112">PARAMETERS</span></span>

### <span data-ttu-id="955f3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="955f3-113">-AccountName</span></span>
<span data-ttu-id="955f3-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="955f3-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="955f3-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="955f3-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="955f3-116">Maximaler Durchsatzwert, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="955f3-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="955f3-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="955f3-117">-Confirm</span></span>
<span data-ttu-id="955f3-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="955f3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="955f3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="955f3-119">-DefaultProfile</span></span>
<span data-ttu-id="955f3-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="955f3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="955f3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="955f3-121">-InputObject</span></span>
<span data-ttu-id="955f3-122">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="955f3-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="955f3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="955f3-123">-Name</span></span>
<span data-ttu-id="955f3-124">Name des Kassa-Schlüsselbereichs.</span><span class="sxs-lookup"><span data-stu-id="955f3-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="955f3-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="955f3-125">-ParentObject</span></span>
<span data-ttu-id="955f3-126">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="955f3-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="955f3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="955f3-127">-ResourceGroupName</span></span>
<span data-ttu-id="955f3-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="955f3-128">Name of resource group.</span></span>

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

### <span data-ttu-id="955f3-129">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="955f3-129">-Throughput</span></span>
<span data-ttu-id="955f3-130">Der Durchsatz von Cassisy Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="955f3-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="955f3-131">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="955f3-131">Default value is 400.</span></span>

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

### <span data-ttu-id="955f3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="955f3-132">-WhatIf</span></span>
<span data-ttu-id="955f3-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="955f3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="955f3-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="955f3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="955f3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="955f3-135">CommonParameters</span></span>
<span data-ttu-id="955f3-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="955f3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="955f3-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="955f3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="955f3-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="955f3-138">INPUTS</span></span>

### <span data-ttu-id="955f3-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="955f3-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="955f3-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="955f3-140">OUTPUTS</span></span>

### <span data-ttu-id="955f3-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="955f3-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="955f3-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="955f3-142">NOTES</span></span>

## <span data-ttu-id="955f3-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="955f3-143">RELATED LINKS</span></span>
