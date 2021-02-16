---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144452"
---
# <span data-ttu-id="f5b5d-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="f5b5d-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="f5b5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="f5b5d-103">Aktualisiert den Keyspace".</span><span class="sxs-lookup"><span data-stu-id="f5b5d-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="f5b5d-104">Führt einen clientseitigen Patchvorgang durch, indem der vorhandene Keyspace gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="f5b5d-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5b5d-105">SYNTAX</span></span>

### <span data-ttu-id="f5b5d-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f5b5d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5b5d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5b5d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5b5d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5b5d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5b5d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5b5d-109">DESCRIPTION</span></span>
<span data-ttu-id="f5b5d-110">Aktualisiert den Keyspace".</span><span class="sxs-lookup"><span data-stu-id="f5b5d-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="f5b5d-111">Führt einen clientseitigen Patchvorgang durch, indem der vorhandene Keyspace gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="f5b5d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f5b5d-112">EXAMPLES</span></span>

### <span data-ttu-id="f5b5d-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f5b5d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="f5b5d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5b5d-114">PARAMETERS</span></span>

### <span data-ttu-id="f5b5d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5b5d-115">-AccountName</span></span>
<span data-ttu-id="f5b5d-116">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f5b5d-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f5b5d-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f5b5d-118">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f5b5d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5b5d-119">-Confirm</span></span>
<span data-ttu-id="f5b5d-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5b5d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5b5d-121">-DefaultProfile</span></span>
<span data-ttu-id="f5b5d-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5b5d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5b5d-123">-InputObject</span></span>
<span data-ttu-id="f5b5d-124">Dieses Keyspaceobjekt.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="f5b5d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f5b5d-125">-Name</span></span>
<span data-ttu-id="f5b5d-126">Der Name des Schlüsselraums.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="f5b5d-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f5b5d-127">-ParentObject</span></span>
<span data-ttu-id="f5b5d-128">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="f5b5d-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f5b5d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5b5d-129">-ResourceGroupName</span></span>
<span data-ttu-id="f5b5d-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-130">Name of resource group.</span></span>

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

### <span data-ttu-id="f5b5d-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f5b5d-131">-Throughput</span></span>
<span data-ttu-id="f5b5d-132">Der Durchsatz von Tastaturschlüsselspaces (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f5b5d-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="f5b5d-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-133">Default value is 400.</span></span>

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

### <span data-ttu-id="f5b5d-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f5b5d-134">-WhatIf</span></span>
<span data-ttu-id="f5b5d-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5b5d-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5b5d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5b5d-137">CommonParameters</span></span>
<span data-ttu-id="f5b5d-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5b5d-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5b5d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5b5d-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f5b5d-140">INPUTS</span></span>

### <span data-ttu-id="f5b5d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f5b5d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="f5b5d-142">Microsoft.Azure.Commands.ExesDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="f5b5d-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="f5b5d-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f5b5d-143">OUTPUTS</span></span>

### <span data-ttu-id="f5b5d-144">Microsoft.Azure.Commands.ExesDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="f5b5d-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="f5b5d-145">Microsoft.Azure.Commands.UmsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f5b5d-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f5b5d-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f5b5d-146">NOTES</span></span>

## <span data-ttu-id="f5b5d-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f5b5d-147">RELATED LINKS</span></span>
