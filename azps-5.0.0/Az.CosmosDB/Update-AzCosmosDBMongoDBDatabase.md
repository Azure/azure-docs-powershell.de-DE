---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299031"
---
# <span data-ttu-id="44a90-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="44a90-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="44a90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44a90-102">SYNOPSIS</span></span>
<span data-ttu-id="44a90-103">Aktualisiert die CosmosDB-MongoDB-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="44a90-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="44a90-104">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="44a90-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="44a90-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="44a90-105">SYNTAX</span></span>

### <span data-ttu-id="44a90-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="44a90-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44a90-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44a90-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44a90-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44a90-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44a90-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44a90-109">DESCRIPTION</span></span>
<span data-ttu-id="44a90-110">Aktualisiert die CosmosDB-MongoDB-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="44a90-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="44a90-111">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="44a90-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="44a90-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44a90-112">EXAMPLES</span></span>

### <span data-ttu-id="44a90-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="44a90-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="44a90-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="44a90-114">PARAMETERS</span></span>

### <span data-ttu-id="44a90-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="44a90-115">-AccountName</span></span>
<span data-ttu-id="44a90-116">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="44a90-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="44a90-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="44a90-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="44a90-118">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="44a90-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="44a90-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="44a90-119">-Confirm</span></span>
<span data-ttu-id="44a90-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44a90-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44a90-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44a90-121">-DefaultProfile</span></span>
<span data-ttu-id="44a90-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44a90-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44a90-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="44a90-123">-InputObject</span></span>
<span data-ttu-id="44a90-124">Mongo-Datenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="44a90-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a90-125">-Name</span><span class="sxs-lookup"><span data-stu-id="44a90-125">-Name</span></span>
<span data-ttu-id="44a90-126">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="44a90-126">Database name.</span></span>

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

### <span data-ttu-id="44a90-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="44a90-127">-ParentObject</span></span>
<span data-ttu-id="44a90-128">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="44a90-128">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a90-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44a90-129">-ResourceGroupName</span></span>
<span data-ttu-id="44a90-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="44a90-130">Name of resource group.</span></span>

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

### <span data-ttu-id="44a90-131">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="44a90-131">-Throughput</span></span>
<span data-ttu-id="44a90-132">Der Durchsatz der Mongo-Datenbank (ru/s).</span><span class="sxs-lookup"><span data-stu-id="44a90-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="44a90-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="44a90-133">Default value is 400.</span></span>

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

### <span data-ttu-id="44a90-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44a90-134">-WhatIf</span></span>
<span data-ttu-id="44a90-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44a90-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44a90-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44a90-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44a90-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a90-137">CommonParameters</span></span>
<span data-ttu-id="44a90-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44a90-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a90-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44a90-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a90-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44a90-140">INPUTS</span></span>

### <span data-ttu-id="44a90-141">Keine</span><span class="sxs-lookup"><span data-stu-id="44a90-141">None</span></span>

## <span data-ttu-id="44a90-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44a90-142">OUTPUTS</span></span>

### <span data-ttu-id="44a90-143">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="44a90-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="44a90-144">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="44a90-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="44a90-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="44a90-145">NOTES</span></span>

## <span data-ttu-id="44a90-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44a90-146">RELATED LINKS</span></span>
