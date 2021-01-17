---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472780"
---
# <span data-ttu-id="1a05b-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="1a05b-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="1a05b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a05b-102">SYNOPSIS</span></span>
<span data-ttu-id="1a05b-103">Aktualisiert die Tabelle "AktualisierungenSDB Untern"</span><span class="sxs-lookup"><span data-stu-id="1a05b-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="1a05b-104">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Tabelle gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="1a05b-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="1a05b-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a05b-105">SYNTAX</span></span>

### <span data-ttu-id="1a05b-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1a05b-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a05b-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a05b-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a05b-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a05b-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a05b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a05b-109">DESCRIPTION</span></span>
<span data-ttu-id="1a05b-110">Aktualisiert die Tabelle "AktualisierungenSDB Untern"</span><span class="sxs-lookup"><span data-stu-id="1a05b-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="1a05b-111">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Tabelle gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="1a05b-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="1a05b-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a05b-112">EXAMPLES</span></span>

### <span data-ttu-id="1a05b-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1a05b-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="1a05b-114">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="1a05b-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="1a05b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a05b-115">PARAMETERS</span></span>

### <span data-ttu-id="1a05b-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1a05b-116">-AccountName</span></span>
<span data-ttu-id="1a05b-117">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="1a05b-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1a05b-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="1a05b-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="1a05b-119">Analytical Storage TTL.</span><span class="sxs-lookup"><span data-stu-id="1a05b-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="1a05b-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="1a05b-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1a05b-121">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1a05b-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1a05b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a05b-122">-Confirm</span></span>
<span data-ttu-id="1a05b-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a05b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a05b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a05b-124">-DefaultProfile</span></span>
<span data-ttu-id="1a05b-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a05b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a05b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a05b-126">-InputObject</span></span>
<span data-ttu-id="1a05b-127">Das Tabellenobjekt "Untere Tabelle".</span><span class="sxs-lookup"><span data-stu-id="1a05b-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="1a05b-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="1a05b-128">-KeyspaceName</span></span>
<span data-ttu-id="1a05b-129">Name des Tastaturschlüssels.</span><span class="sxs-lookup"><span data-stu-id="1a05b-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="1a05b-130">-Name</span><span class="sxs-lookup"><span data-stu-id="1a05b-130">-Name</span></span>
<span data-ttu-id="1a05b-131">DestgensEr Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="1a05b-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="1a05b-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1a05b-132">-ParentObject</span></span>
<span data-ttu-id="1a05b-133">Dieses Keyspaceobjekt.</span><span class="sxs-lookup"><span data-stu-id="1a05b-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="1a05b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a05b-134">-ResourceGroupName</span></span>
<span data-ttu-id="1a05b-135">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1a05b-135">Name of resource group.</span></span>

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

### <span data-ttu-id="1a05b-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="1a05b-136">-Schema</span></span>
<span data-ttu-id="1a05b-137">PSCasstypSchema-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1a05b-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="1a05b-138">Verwenden sie New-AzCosmosDBCassandraSchema, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a05b-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a05b-139">-Throughput</span><span class="sxs-lookup"><span data-stu-id="1a05b-139">-Throughput</span></span>
<span data-ttu-id="1a05b-140">Der Durchsatz von Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="1a05b-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="1a05b-141">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="1a05b-141">Default value is 400.</span></span>

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

### <span data-ttu-id="1a05b-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="1a05b-142">-TtlInSeconds</span></span>
<span data-ttu-id="1a05b-143">Standard-Ttl in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="1a05b-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="1a05b-144">Wenn der Wert fehlt oder auf -1 festgelegt ist, laufen die Elemente nicht ab.</span><span class="sxs-lookup"><span data-stu-id="1a05b-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="1a05b-145">Wenn der Wert auf "n" festgelegt ist, laufen die Elemente n Sekunden nach der letzten Änderung ab.</span><span class="sxs-lookup"><span data-stu-id="1a05b-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="1a05b-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1a05b-146">-WhatIf</span></span>
<span data-ttu-id="1a05b-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a05b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a05b-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a05b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a05b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a05b-149">CommonParameters</span></span>
<span data-ttu-id="1a05b-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a05b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a05b-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a05b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a05b-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a05b-152">INPUTS</span></span>

### <span data-ttu-id="1a05b-153">Microsoft.Azure.Commands.DiesDB.Models.PSCassschemaSchema</span><span class="sxs-lookup"><span data-stu-id="1a05b-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="1a05b-154">Microsoft.Azure.Commands.UmsDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="1a05b-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="1a05b-155">Microsoft.Azure.Commands.CassDB.Models.PSCassistenTableGetResults</span><span class="sxs-lookup"><span data-stu-id="1a05b-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="1a05b-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a05b-156">OUTPUTS</span></span>

### <span data-ttu-id="1a05b-157">Microsoft.Azure.Commands.CassDB.Models.PSCassistenTableGetResults</span><span class="sxs-lookup"><span data-stu-id="1a05b-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="1a05b-158">Microsoft.Azure.Commands.Abt. Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="1a05b-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="1a05b-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1a05b-159">NOTES</span></span>

## <span data-ttu-id="1a05b-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1a05b-160">RELATED LINKS</span></span>
