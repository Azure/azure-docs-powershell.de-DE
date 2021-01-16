---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290008"
---
# <span data-ttu-id="e31ab-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="e31ab-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="e31ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e31ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e31ab-103">Aktualisiert die Datenbank "DessDB Gremlin".</span><span class="sxs-lookup"><span data-stu-id="e31ab-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="e31ab-104">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Datenbank gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="e31ab-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="e31ab-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e31ab-105">SYNTAX</span></span>

### <span data-ttu-id="e31ab-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e31ab-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e31ab-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e31ab-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e31ab-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e31ab-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e31ab-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e31ab-109">DESCRIPTION</span></span>
<span data-ttu-id="e31ab-110">Aktualisiert die Datenbank "DessDB Gremlin".</span><span class="sxs-lookup"><span data-stu-id="e31ab-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="e31ab-111">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Datenbank gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="e31ab-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="e31ab-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e31ab-112">EXAMPLES</span></span>

### <span data-ttu-id="e31ab-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e31ab-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="e31ab-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e31ab-114">PARAMETERS</span></span>

### <span data-ttu-id="e31ab-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e31ab-115">-AccountName</span></span>
<span data-ttu-id="e31ab-116">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="e31ab-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e31ab-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e31ab-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e31ab-118">Maximaler Durchsatzwert, wenn die Autoskala aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e31ab-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e31ab-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e31ab-119">-Confirm</span></span>
<span data-ttu-id="e31ab-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e31ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e31ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e31ab-121">-DefaultProfile</span></span>
<span data-ttu-id="e31ab-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e31ab-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e31ab-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e31ab-123">-InputObject</span></span>
<span data-ttu-id="e31ab-124">Das Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="e31ab-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e31ab-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e31ab-125">-Name</span></span>
<span data-ttu-id="e31ab-126">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="e31ab-126">Database name.</span></span>

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

### <span data-ttu-id="e31ab-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e31ab-127">-ParentObject</span></span>
<span data-ttu-id="e31ab-128">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="e31ab-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e31ab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e31ab-129">-ResourceGroupName</span></span>
<span data-ttu-id="e31ab-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e31ab-130">Name of resource group.</span></span>

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

### <span data-ttu-id="e31ab-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="e31ab-131">-Throughput</span></span>
<span data-ttu-id="e31ab-132">Der Durchsatz von Gremlin Database (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e31ab-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="e31ab-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="e31ab-133">Default value is 400.</span></span>

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

### <span data-ttu-id="e31ab-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e31ab-134">-WhatIf</span></span>
<span data-ttu-id="e31ab-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e31ab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e31ab-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e31ab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e31ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e31ab-137">CommonParameters</span></span>
<span data-ttu-id="e31ab-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e31ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e31ab-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e31ab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e31ab-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e31ab-140">INPUTS</span></span>

### <span data-ttu-id="e31ab-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e31ab-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="e31ab-142">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e31ab-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="e31ab-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e31ab-143">OUTPUTS</span></span>

### <span data-ttu-id="e31ab-144">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e31ab-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="e31ab-145">Microsoft.Azure.Commands.Abt. Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="e31ab-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="e31ab-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e31ab-146">NOTES</span></span>

## <span data-ttu-id="e31ab-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e31ab-147">RELATED LINKS</span></span>
