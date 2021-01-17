---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470671"
---
# <span data-ttu-id="5cca8-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="5cca8-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="5cca8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cca8-102">SYNOPSIS</span></span>
<span data-ttu-id="5cca8-103">Aktualisiert den Sql-Trigger" von "DessDB".</span><span class="sxs-lookup"><span data-stu-id="5cca8-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="5cca8-104">Führt einen clientseitigen Patchvorgang durch, indem der vorhandene Trigger gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="5cca8-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="5cca8-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5cca8-105">SYNTAX</span></span>

### <span data-ttu-id="5cca8-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5cca8-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cca8-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cca8-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cca8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cca8-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cca8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5cca8-109">DESCRIPTION</span></span>
<span data-ttu-id="5cca8-110">Aktualisiert den Sql-Trigger" von "DessDB".</span><span class="sxs-lookup"><span data-stu-id="5cca8-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="5cca8-111">Führt einen clientseitigen Patchvorgang durch, indem der vorhandene Trigger gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="5cca8-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="5cca8-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5cca8-112">EXAMPLES</span></span>

### <span data-ttu-id="5cca8-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5cca8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="5cca8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cca8-114">PARAMETERS</span></span>

### <span data-ttu-id="5cca8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5cca8-115">-AccountName</span></span>
<span data-ttu-id="5cca8-116">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="5cca8-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5cca8-117">-Body</span><span class="sxs-lookup"><span data-stu-id="5cca8-117">-Body</span></span>
<span data-ttu-id="5cca8-118">Der Textkörper des Triggers.</span><span class="sxs-lookup"><span data-stu-id="5cca8-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="5cca8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cca8-119">-Confirm</span></span>
<span data-ttu-id="5cca8-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5cca8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cca8-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="5cca8-121">-ContainerName</span></span>
<span data-ttu-id="5cca8-122">Containername.</span><span class="sxs-lookup"><span data-stu-id="5cca8-122">Container name.</span></span>

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

### <span data-ttu-id="5cca8-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5cca8-123">-DatabaseName</span></span>
<span data-ttu-id="5cca8-124">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="5cca8-124">Database name.</span></span>

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

### <span data-ttu-id="5cca8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cca8-125">-DefaultProfile</span></span>
<span data-ttu-id="5cca8-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5cca8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cca8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cca8-127">-InputObject</span></span>
<span data-ttu-id="5cca8-128">Sql trigger Object</span><span class="sxs-lookup"><span data-stu-id="5cca8-128">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cca8-129">-Name</span><span class="sxs-lookup"><span data-stu-id="5cca8-129">-Name</span></span>
<span data-ttu-id="5cca8-130">Triggername.</span><span class="sxs-lookup"><span data-stu-id="5cca8-130">Trigger name.</span></span>

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

### <span data-ttu-id="5cca8-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5cca8-131">-ParentObject</span></span>
<span data-ttu-id="5cca8-132">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5cca8-132">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cca8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cca8-133">-ResourceGroupName</span></span>
<span data-ttu-id="5cca8-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5cca8-134">Name of resource group.</span></span>

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

### <span data-ttu-id="5cca8-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="5cca8-135">-TriggerOperation</span></span>
<span data-ttu-id="5cca8-136">Der Vorgang, dem der Trigger zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5cca8-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="5cca8-137">Mögliche Werte sind: "Alle", "Erstellen", "Aktualisieren", "Löschen", "Ersetzen".</span><span class="sxs-lookup"><span data-stu-id="5cca8-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="5cca8-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="5cca8-138">-TriggerType</span></span>
<span data-ttu-id="5cca8-139">Typ des Triggers.</span><span class="sxs-lookup"><span data-stu-id="5cca8-139">Type of the Trigger.</span></span>
<span data-ttu-id="5cca8-140">Mögliche Werte sind: 'Pre', 'Post'</span><span class="sxs-lookup"><span data-stu-id="5cca8-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="5cca8-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5cca8-141">-WhatIf</span></span>
<span data-ttu-id="5cca8-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cca8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cca8-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5cca8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cca8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cca8-144">CommonParameters</span></span>
<span data-ttu-id="5cca8-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cca8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cca8-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cca8-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cca8-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5cca8-147">INPUTS</span></span>

### <span data-ttu-id="5cca8-148">Microsoft.Azure.Commands.ExesDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="5cca8-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="5cca8-149">Microsoft.Azure.Commands.ExesDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="5cca8-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="5cca8-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5cca8-150">OUTPUTS</span></span>

### <span data-ttu-id="5cca8-151">Microsoft.Azure.Commands.ExesDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="5cca8-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="5cca8-152">Microsoft.Azure.Commands.Abt. Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="5cca8-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="5cca8-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5cca8-153">NOTES</span></span>

## <span data-ttu-id="5cca8-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5cca8-154">RELATED LINKS</span></span>
