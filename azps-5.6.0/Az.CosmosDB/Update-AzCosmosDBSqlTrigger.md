---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: bebf801316d18b29f6444b0b369833ae547e78d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947480"
---
# <span data-ttu-id="08af4-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="08af4-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="08af4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08af4-102">SYNOPSIS</span></span>
<span data-ttu-id="08af4-103">Aktualisiert den CosmosDB Sql Trigger.</span><span class="sxs-lookup"><span data-stu-id="08af4-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="08af4-104">Führt einen clientseitigen Patchvorgang durch Lesen des vorhandenen Triggers aus.</span><span class="sxs-lookup"><span data-stu-id="08af4-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="08af4-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08af4-105">SYNTAX</span></span>

### <span data-ttu-id="08af4-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="08af4-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08af4-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08af4-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08af4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08af4-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08af4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08af4-109">DESCRIPTION</span></span>
<span data-ttu-id="08af4-110">Aktualisiert den CosmosDB Sql Trigger.</span><span class="sxs-lookup"><span data-stu-id="08af4-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="08af4-111">Führt einen clientseitigen Patchvorgang durch Lesen des vorhandenen Triggers aus.</span><span class="sxs-lookup"><span data-stu-id="08af4-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="08af4-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="08af4-112">EXAMPLES</span></span>

### <span data-ttu-id="08af4-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08af4-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="08af4-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="08af4-114">PARAMETERS</span></span>

### <span data-ttu-id="08af4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="08af4-115">-AccountName</span></span>
<span data-ttu-id="08af4-116">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="08af4-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="08af4-117">-Body</span><span class="sxs-lookup"><span data-stu-id="08af4-117">-Body</span></span>
<span data-ttu-id="08af4-118">Der Textkörper des Triggers.</span><span class="sxs-lookup"><span data-stu-id="08af4-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="08af4-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08af4-119">-Confirm</span></span>
<span data-ttu-id="08af4-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08af4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08af4-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="08af4-121">-ContainerName</span></span>
<span data-ttu-id="08af4-122">Containername.</span><span class="sxs-lookup"><span data-stu-id="08af4-122">Container name.</span></span>

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

### <span data-ttu-id="08af4-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="08af4-123">-DatabaseName</span></span>
<span data-ttu-id="08af4-124">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="08af4-124">Database name.</span></span>

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

### <span data-ttu-id="08af4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08af4-125">-DefaultProfile</span></span>
<span data-ttu-id="08af4-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08af4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08af4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08af4-127">-InputObject</span></span>
<span data-ttu-id="08af4-128">Sql-Triggerobjekt</span><span class="sxs-lookup"><span data-stu-id="08af4-128">Sql trigger Object</span></span>

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

### <span data-ttu-id="08af4-129">-Name</span><span class="sxs-lookup"><span data-stu-id="08af4-129">-Name</span></span>
<span data-ttu-id="08af4-130">Triggername.</span><span class="sxs-lookup"><span data-stu-id="08af4-130">Trigger name.</span></span>

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

### <span data-ttu-id="08af4-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="08af4-131">-ParentObject</span></span>
<span data-ttu-id="08af4-132">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="08af4-132">Sql Container object.</span></span>

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

### <span data-ttu-id="08af4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08af4-133">-ResourceGroupName</span></span>
<span data-ttu-id="08af4-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="08af4-134">Name of resource group.</span></span>

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

### <span data-ttu-id="08af4-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="08af4-135">-TriggerOperation</span></span>
<span data-ttu-id="08af4-136">Der Vorgang, dem der Trigger zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="08af4-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="08af4-137">Mögliche Werte sind: "Alles", "Erstellen", "Aktualisieren", "Löschen", "Ersetzen"</span><span class="sxs-lookup"><span data-stu-id="08af4-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="08af4-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="08af4-138">-TriggerType</span></span>
<span data-ttu-id="08af4-139">Typ des Triggers.</span><span class="sxs-lookup"><span data-stu-id="08af4-139">Type of the Trigger.</span></span>
<span data-ttu-id="08af4-140">Mögliche Werte sind: "Pre", "Post"</span><span class="sxs-lookup"><span data-stu-id="08af4-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="08af4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08af4-141">-WhatIf</span></span>
<span data-ttu-id="08af4-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08af4-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08af4-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08af4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08af4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08af4-144">CommonParameters</span></span>
<span data-ttu-id="08af4-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08af4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08af4-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08af4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08af4-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="08af4-147">INPUTS</span></span>

### <span data-ttu-id="08af4-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="08af4-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="08af4-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="08af4-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="08af4-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="08af4-150">OUTPUTS</span></span>

### <span data-ttu-id="08af4-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="08af4-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="08af4-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="08af4-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="08af4-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="08af4-153">NOTES</span></span>

## <span data-ttu-id="08af4-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="08af4-154">RELATED LINKS</span></span>
