---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: dbffec52b5c1b30f6b00febbc2e6c952beda669e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931259"
---
# <span data-ttu-id="52a5a-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="52a5a-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="52a5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="52a5a-103">Aktualisiert die CosmosDB-MongoDB-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="52a5a-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="52a5a-104">Führt einen clientseitigen Patchvorgang durch Lesen der vorhandenen Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="52a5a-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="52a5a-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52a5a-105">SYNTAX</span></span>

### <span data-ttu-id="52a5a-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="52a5a-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52a5a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52a5a-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52a5a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52a5a-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52a5a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52a5a-109">DESCRIPTION</span></span>
<span data-ttu-id="52a5a-110">Aktualisiert die CosmosDB-MongoDB-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="52a5a-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="52a5a-111">Führt einen clientseitigen Patchvorgang durch Lesen der vorhandenen Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="52a5a-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="52a5a-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="52a5a-112">EXAMPLES</span></span>

### <span data-ttu-id="52a5a-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="52a5a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="52a5a-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="52a5a-114">PARAMETERS</span></span>

### <span data-ttu-id="52a5a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="52a5a-115">-AccountName</span></span>
<span data-ttu-id="52a5a-116">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="52a5a-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="52a5a-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="52a5a-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="52a5a-118">Maximaler Durchsatzwert, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="52a5a-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="52a5a-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="52a5a-119">-Confirm</span></span>
<span data-ttu-id="52a5a-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="52a5a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52a5a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a5a-121">-DefaultProfile</span></span>
<span data-ttu-id="52a5a-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52a5a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52a5a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52a5a-123">-InputObject</span></span>
<span data-ttu-id="52a5a-124">Mongo-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="52a5a-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="52a5a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="52a5a-125">-Name</span></span>
<span data-ttu-id="52a5a-126">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="52a5a-126">Database name.</span></span>

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

### <span data-ttu-id="52a5a-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="52a5a-127">-ParentObject</span></span>
<span data-ttu-id="52a5a-128">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="52a5a-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="52a5a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a5a-129">-ResourceGroupName</span></span>
<span data-ttu-id="52a5a-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="52a5a-130">Name of resource group.</span></span>

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

### <span data-ttu-id="52a5a-131">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="52a5a-131">-Throughput</span></span>
<span data-ttu-id="52a5a-132">Der Durchsatz der Mongo-Datenbank (RU/s).</span><span class="sxs-lookup"><span data-stu-id="52a5a-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="52a5a-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="52a5a-133">Default value is 400.</span></span>

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

### <span data-ttu-id="52a5a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a5a-134">-WhatIf</span></span>
<span data-ttu-id="52a5a-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52a5a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52a5a-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52a5a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52a5a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a5a-137">CommonParameters</span></span>
<span data-ttu-id="52a5a-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52a5a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a5a-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52a5a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a5a-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="52a5a-140">INPUTS</span></span>

### <span data-ttu-id="52a5a-141">Keine</span><span class="sxs-lookup"><span data-stu-id="52a5a-141">None</span></span>

## <span data-ttu-id="52a5a-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="52a5a-142">OUTPUTS</span></span>

### <span data-ttu-id="52a5a-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="52a5a-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="52a5a-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="52a5a-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="52a5a-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="52a5a-145">NOTES</span></span>

## <span data-ttu-id="52a5a-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="52a5a-146">RELATED LINKS</span></span>
