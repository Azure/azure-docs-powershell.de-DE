---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299451"
---
# <span data-ttu-id="6f6aa-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="6f6aa-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="6f6aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f6aa-102">SYNOPSIS</span></span>
<span data-ttu-id="6f6aa-103">Verwenden Sie diese Vorgehensweise, um den AutoScale-Durchsatz auf manuellen Durchsatz zu migrieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="6f6aa-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="6f6aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f6aa-104">SYNTAX</span></span>

### <span data-ttu-id="6f6aa-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f6aa-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f6aa-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f6aa-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f6aa-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f6aa-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f6aa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f6aa-108">DESCRIPTION</span></span>
<span data-ttu-id="6f6aa-109">ThroughpyteType Parameter definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6f6aa-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="6f6aa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f6aa-110">EXAMPLES</span></span>

### <span data-ttu-id="6f6aa-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6f6aa-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="6f6aa-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f6aa-112">PARAMETERS</span></span>

### <span data-ttu-id="6f6aa-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="6f6aa-113">-AccountName</span></span>
<span data-ttu-id="6f6aa-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="6f6aa-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6f6aa-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6f6aa-115">-Confirm</span></span>
<span data-ttu-id="6f6aa-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f6aa-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f6aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f6aa-117">-DefaultProfile</span></span>
<span data-ttu-id="6f6aa-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6f6aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f6aa-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6f6aa-119">-InputObject</span></span>
<span data-ttu-id="6f6aa-120">Cassandra-Keyspace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6f6aa-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="6f6aa-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6f6aa-121">-Name</span></span>
<span data-ttu-id="6f6aa-122">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="6f6aa-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="6f6aa-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6f6aa-123">-ParentObject</span></span>
<span data-ttu-id="6f6aa-124">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="6f6aa-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6f6aa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f6aa-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f6aa-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6f6aa-126">Name of resource group.</span></span>

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

### <span data-ttu-id="6f6aa-127">-Durchsatztyp</span><span class="sxs-lookup"><span data-stu-id="6f6aa-127">-ThroughputType</span></span>
<span data-ttu-id="6f6aa-128">Der durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f6aa-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="6f6aa-129">Mögliche Werte sind: AutoScale, manuell.</span><span class="sxs-lookup"><span data-stu-id="6f6aa-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="6f6aa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f6aa-130">-WhatIf</span></span>
<span data-ttu-id="6f6aa-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f6aa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f6aa-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f6aa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f6aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f6aa-133">CommonParameters</span></span>
<span data-ttu-id="6f6aa-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f6aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f6aa-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f6aa-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f6aa-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f6aa-136">INPUTS</span></span>

### <span data-ttu-id="6f6aa-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="6f6aa-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="6f6aa-138">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="6f6aa-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="6f6aa-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f6aa-139">OUTPUTS</span></span>

### <span data-ttu-id="6f6aa-140">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6f6aa-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6f6aa-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f6aa-141">NOTES</span></span>

## <span data-ttu-id="6f6aa-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f6aa-142">RELATED LINKS</span></span>
