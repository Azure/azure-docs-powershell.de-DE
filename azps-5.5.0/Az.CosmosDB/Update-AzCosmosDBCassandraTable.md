---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166164"
---
# <span data-ttu-id="39299-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="39299-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="39299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39299-102">SYNOPSIS</span></span>
<span data-ttu-id="39299-103">Aktualisiert die Tabelle "AktualisierungenSDB Untern"</span><span class="sxs-lookup"><span data-stu-id="39299-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="39299-104">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Tabelle gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="39299-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="39299-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39299-105">SYNTAX</span></span>

### <span data-ttu-id="39299-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="39299-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39299-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39299-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39299-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39299-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39299-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39299-109">DESCRIPTION</span></span>
<span data-ttu-id="39299-110">Aktualisiert die Tabelle "AktualisierungenDB 1844".</span><span class="sxs-lookup"><span data-stu-id="39299-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="39299-111">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Tabelle gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="39299-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="39299-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39299-112">EXAMPLES</span></span>

### <span data-ttu-id="39299-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39299-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="39299-114">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="39299-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="39299-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39299-115">PARAMETERS</span></span>

### <span data-ttu-id="39299-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="39299-116">-AccountName</span></span>
<span data-ttu-id="39299-117">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="39299-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="39299-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="39299-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="39299-119">Analytical Storage TTL.</span><span class="sxs-lookup"><span data-stu-id="39299-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="39299-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="39299-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="39299-121">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="39299-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="39299-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39299-122">-Confirm</span></span>
<span data-ttu-id="39299-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39299-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39299-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39299-124">-DefaultProfile</span></span>
<span data-ttu-id="39299-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39299-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39299-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39299-126">-InputObject</span></span>
<span data-ttu-id="39299-127">Das Objekt "Tabelle" aus Untere Tabelle.</span><span class="sxs-lookup"><span data-stu-id="39299-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="39299-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="39299-128">-KeyspaceName</span></span>
<span data-ttu-id="39299-129">Der Name des Schlüsselraums.</span><span class="sxs-lookup"><span data-stu-id="39299-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="39299-130">-Name</span><span class="sxs-lookup"><span data-stu-id="39299-130">-Name</span></span>
<span data-ttu-id="39299-131">DestgensEr Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="39299-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="39299-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="39299-132">-ParentObject</span></span>
<span data-ttu-id="39299-133">Dieses Keyspaceobjekt.</span><span class="sxs-lookup"><span data-stu-id="39299-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="39299-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39299-134">-ResourceGroupName</span></span>
<span data-ttu-id="39299-135">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="39299-135">Name of resource group.</span></span>

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

### <span data-ttu-id="39299-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="39299-136">-Schema</span></span>
<span data-ttu-id="39299-137">PSCasstypSchema-Objekt.</span><span class="sxs-lookup"><span data-stu-id="39299-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="39299-138">Verwenden sie New-AzCosmosDBCassandraSchema, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39299-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="39299-139">-Throughput</span><span class="sxs-lookup"><span data-stu-id="39299-139">-Throughput</span></span>
<span data-ttu-id="39299-140">Der Durchsatz von Tastaturschlüsselspaces (RU/s).</span><span class="sxs-lookup"><span data-stu-id="39299-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="39299-141">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="39299-141">Default value is 400.</span></span>

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

### <span data-ttu-id="39299-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="39299-142">-TtlInSeconds</span></span>
<span data-ttu-id="39299-143">Standard-Ttl in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="39299-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="39299-144">Wenn der Wert fehlt oder auf -1 festgelegt ist, laufen die Elemente nicht ab.</span><span class="sxs-lookup"><span data-stu-id="39299-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="39299-145">Wenn der Wert auf "n" festgelegt ist, laufen die Elemente n Sekunden nach der letzten Änderung ab.</span><span class="sxs-lookup"><span data-stu-id="39299-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="39299-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="39299-146">-WhatIf</span></span>
<span data-ttu-id="39299-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39299-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39299-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39299-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39299-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39299-149">CommonParameters</span></span>
<span data-ttu-id="39299-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39299-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39299-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39299-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39299-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39299-152">INPUTS</span></span>

### <span data-ttu-id="39299-153">Microsoft.Azure.Commands.DiesDB.Models.PSCassschemaSchema</span><span class="sxs-lookup"><span data-stu-id="39299-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="39299-154">Microsoft.Azure.Commands.ExesDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="39299-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="39299-155">Microsoft.Azure.Commands.CassDB.Models.PSCassistenTableGetResults</span><span class="sxs-lookup"><span data-stu-id="39299-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="39299-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39299-156">OUTPUTS</span></span>

### <span data-ttu-id="39299-157">Microsoft.Azure.Commands.CassDB.Models.PSCassistenTableGetResults</span><span class="sxs-lookup"><span data-stu-id="39299-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="39299-158">Microsoft.Azure.Commands.UmsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="39299-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="39299-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="39299-159">NOTES</span></span>

## <span data-ttu-id="39299-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="39299-160">RELATED LINKS</span></span>
