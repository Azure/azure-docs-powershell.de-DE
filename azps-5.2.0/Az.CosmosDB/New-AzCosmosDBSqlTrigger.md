---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366973"
---
# <span data-ttu-id="e1749-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="e1749-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="e1749-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1749-102">SYNOPSIS</span></span>
<span data-ttu-id="e1749-103">Erstellt einen neuen SkriptsDB-Sql-Trigger.</span><span class="sxs-lookup"><span data-stu-id="e1749-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="e1749-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1749-104">SYNTAX</span></span>

### <span data-ttu-id="e1749-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1749-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1749-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1749-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1749-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1749-107">DESCRIPTION</span></span>
<span data-ttu-id="e1749-108">Erstellt einen neuen SkriptsDB-Sql-Trigger.</span><span class="sxs-lookup"><span data-stu-id="e1749-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="e1749-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1749-109">EXAMPLES</span></span>

### <span data-ttu-id="e1749-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1749-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="e1749-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1749-111">PARAMETERS</span></span>

### <span data-ttu-id="e1749-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e1749-112">-AccountName</span></span>
<span data-ttu-id="e1749-113">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="e1749-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e1749-114">-Body</span><span class="sxs-lookup"><span data-stu-id="e1749-114">-Body</span></span>
<span data-ttu-id="e1749-115">Der Textkörper des Triggers.</span><span class="sxs-lookup"><span data-stu-id="e1749-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="e1749-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1749-116">-Confirm</span></span>
<span data-ttu-id="e1749-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1749-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1749-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="e1749-118">-ContainerName</span></span>
<span data-ttu-id="e1749-119">Containername.</span><span class="sxs-lookup"><span data-stu-id="e1749-119">Container name.</span></span>

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

### <span data-ttu-id="e1749-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1749-120">-DatabaseName</span></span>
<span data-ttu-id="e1749-121">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="e1749-121">Database name.</span></span>

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

### <span data-ttu-id="e1749-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1749-122">-DefaultProfile</span></span>
<span data-ttu-id="e1749-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1749-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1749-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e1749-124">-Name</span></span>
<span data-ttu-id="e1749-125">Triggername.</span><span class="sxs-lookup"><span data-stu-id="e1749-125">Trigger name.</span></span>

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

### <span data-ttu-id="e1749-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e1749-126">-ParentObject</span></span>
<span data-ttu-id="e1749-127">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e1749-127">Sql Container object.</span></span>

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

### <span data-ttu-id="e1749-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1749-128">-ResourceGroupName</span></span>
<span data-ttu-id="e1749-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e1749-129">Name of resource group.</span></span>

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

### <span data-ttu-id="e1749-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="e1749-130">-TriggerOperation</span></span>
<span data-ttu-id="e1749-131">Der Vorgang, dem der Trigger zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e1749-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="e1749-132">Mögliche Werte sind: "Alle", "Erstellen", "Aktualisieren", "Löschen", "Ersetzen".</span><span class="sxs-lookup"><span data-stu-id="e1749-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="e1749-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="e1749-133">-TriggerType</span></span>
<span data-ttu-id="e1749-134">Typ des Triggers.</span><span class="sxs-lookup"><span data-stu-id="e1749-134">Type of the Trigger.</span></span>
<span data-ttu-id="e1749-135">Mögliche Werte sind: 'Pre', 'Post'</span><span class="sxs-lookup"><span data-stu-id="e1749-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="e1749-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e1749-136">-WhatIf</span></span>
<span data-ttu-id="e1749-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1749-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1749-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1749-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1749-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1749-139">CommonParameters</span></span>
<span data-ttu-id="e1749-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1749-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1749-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1749-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1749-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1749-142">INPUTS</span></span>

### <span data-ttu-id="e1749-143">Microsoft.Azure.Commands.ExesDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e1749-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="e1749-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1749-144">OUTPUTS</span></span>

### <span data-ttu-id="e1749-145">Microsoft.Azure.Commands.ExesDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="e1749-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="e1749-146">Microsoft.Azure.Commands.DiesDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="e1749-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="e1749-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e1749-147">NOTES</span></span>

## <span data-ttu-id="e1749-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e1749-148">RELATED LINKS</span></span>
