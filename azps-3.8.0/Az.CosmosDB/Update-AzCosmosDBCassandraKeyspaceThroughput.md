---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 0c104573fe0ecfb710f37c9c2fe898a6777f49e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995244"
---
# <span data-ttu-id="80b60-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="80b60-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="80b60-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80b60-102">SYNOPSIS</span></span>
<span data-ttu-id="80b60-103">Aktualisiert den Durchsatz eines CosmosDB Cassandra-keyspaces.</span><span class="sxs-lookup"><span data-stu-id="80b60-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="80b60-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80b60-104">SYNTAX</span></span>

### <span data-ttu-id="80b60-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="80b60-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80b60-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80b60-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80b60-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80b60-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80b60-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80b60-108">EXAMPLES</span></span>

### <span data-ttu-id="80b60-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="80b60-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="80b60-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="80b60-110">PARAMETERS</span></span>

### <span data-ttu-id="80b60-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="80b60-111">-AccountName</span></span>
<span data-ttu-id="80b60-112">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="80b60-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="80b60-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="80b60-113">-Confirm</span></span>
<span data-ttu-id="80b60-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80b60-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80b60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b60-115">-DefaultProfile</span></span>
<span data-ttu-id="80b60-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80b60-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80b60-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="80b60-117">-InputObject</span></span>
<span data-ttu-id="80b60-118">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="80b60-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="80b60-119">-Name</span><span class="sxs-lookup"><span data-stu-id="80b60-119">-Name</span></span>
<span data-ttu-id="80b60-120">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="80b60-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="80b60-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="80b60-121">-ParentObject</span></span>
<span data-ttu-id="80b60-122">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="80b60-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80b60-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b60-123">-ResourceGroupName</span></span>
<span data-ttu-id="80b60-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="80b60-124">Name of resource group.</span></span>

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

### <span data-ttu-id="80b60-125">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="80b60-125">-Throughput</span></span>
<span data-ttu-id="80b60-126">Der Durchsatz des Cassandra-Keyspace (ru/s).</span><span class="sxs-lookup"><span data-stu-id="80b60-126">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="80b60-127">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="80b60-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b60-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80b60-128">-WhatIf</span></span>
<span data-ttu-id="80b60-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80b60-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80b60-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80b60-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80b60-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b60-131">CommonParameters</span></span>
<span data-ttu-id="80b60-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b60-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b60-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80b60-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b60-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80b60-134">INPUTS</span></span>

### <span data-ttu-id="80b60-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="80b60-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="80b60-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80b60-136">OUTPUTS</span></span>

### <span data-ttu-id="80b60-137">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="80b60-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="80b60-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="80b60-138">NOTES</span></span>

## <span data-ttu-id="80b60-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80b60-139">RELATED LINKS</span></span>
