---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472782"
---
# <span data-ttu-id="91f3d-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="91f3d-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="91f3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="91f3d-103">Aktualisiert die Datenbank Destallen-Gremlin-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="91f3d-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="91f3d-104">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Datenbank gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="91f3d-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="91f3d-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91f3d-105">SYNTAX</span></span>

### <span data-ttu-id="91f3d-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="91f3d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91f3d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91f3d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91f3d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91f3d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91f3d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91f3d-109">DESCRIPTION</span></span>
<span data-ttu-id="91f3d-110">Aktualisiert die Datenbank Destallen-Gremlin-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="91f3d-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="91f3d-111">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Datenbank gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="91f3d-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="91f3d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="91f3d-112">EXAMPLES</span></span>

### <span data-ttu-id="91f3d-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="91f3d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="91f3d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91f3d-114">PARAMETERS</span></span>

### <span data-ttu-id="91f3d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="91f3d-115">-AccountName</span></span>
<span data-ttu-id="91f3d-116">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="91f3d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="91f3d-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="91f3d-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="91f3d-118">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="91f3d-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="91f3d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91f3d-119">-Confirm</span></span>
<span data-ttu-id="91f3d-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91f3d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91f3d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f3d-121">-DefaultProfile</span></span>
<span data-ttu-id="91f3d-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91f3d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91f3d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91f3d-123">-InputObject</span></span>
<span data-ttu-id="91f3d-124">Das Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="91f3d-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="91f3d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="91f3d-125">-Name</span></span>
<span data-ttu-id="91f3d-126">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="91f3d-126">Database name.</span></span>

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

### <span data-ttu-id="91f3d-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="91f3d-127">-ParentObject</span></span>
<span data-ttu-id="91f3d-128">Objekt "Buchhalterungskonto"</span><span class="sxs-lookup"><span data-stu-id="91f3d-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="91f3d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f3d-129">-ResourceGroupName</span></span>
<span data-ttu-id="91f3d-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="91f3d-130">Name of resource group.</span></span>

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

### <span data-ttu-id="91f3d-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="91f3d-131">-Throughput</span></span>
<span data-ttu-id="91f3d-132">Der Durchsatz von Gremlin Database (RU/s).</span><span class="sxs-lookup"><span data-stu-id="91f3d-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="91f3d-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="91f3d-133">Default value is 400.</span></span>

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

### <span data-ttu-id="91f3d-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="91f3d-134">-WhatIf</span></span>
<span data-ttu-id="91f3d-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91f3d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91f3d-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91f3d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91f3d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f3d-137">CommonParameters</span></span>
<span data-ttu-id="91f3d-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f3d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f3d-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91f3d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f3d-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="91f3d-140">INPUTS</span></span>

### <span data-ttu-id="91f3d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="91f3d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="91f3d-142">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="91f3d-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="91f3d-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="91f3d-143">OUTPUTS</span></span>

### <span data-ttu-id="91f3d-144">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="91f3d-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="91f3d-145">Microsoft.Azure.Commands.UmsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="91f3d-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="91f3d-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="91f3d-146">NOTES</span></span>

## <span data-ttu-id="91f3d-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="91f3d-147">RELATED LINKS</span></span>
