---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175278"
---
# <span data-ttu-id="74d8d-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="74d8d-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="74d8d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="74d8d-103">Aktualisiert den CosmosDB-SQL-Trigger.</span><span class="sxs-lookup"><span data-stu-id="74d8d-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="74d8d-104">Führt einen clientseitigen Patch-Vorgang durchlesen des vorhandenen Triggers aus.</span><span class="sxs-lookup"><span data-stu-id="74d8d-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="74d8d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="74d8d-105">SYNTAX</span></span>

### <span data-ttu-id="74d8d-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="74d8d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d8d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d8d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d8d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d8d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74d8d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74d8d-109">DESCRIPTION</span></span>
<span data-ttu-id="74d8d-110">Aktualisiert den CosmosDB-SQL-Trigger.</span><span class="sxs-lookup"><span data-stu-id="74d8d-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="74d8d-111">Führt einen clientseitigen Patch-Vorgang durchlesen des vorhandenen Triggers aus.</span><span class="sxs-lookup"><span data-stu-id="74d8d-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="74d8d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74d8d-112">EXAMPLES</span></span>

### <span data-ttu-id="74d8d-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74d8d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="74d8d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="74d8d-114">PARAMETERS</span></span>

### <span data-ttu-id="74d8d-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="74d8d-115">-AccountName</span></span>
<span data-ttu-id="74d8d-116">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="74d8d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="74d8d-117">-Body</span><span class="sxs-lookup"><span data-stu-id="74d8d-117">-Body</span></span>
<span data-ttu-id="74d8d-118">Der Text des Triggers.</span><span class="sxs-lookup"><span data-stu-id="74d8d-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="74d8d-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="74d8d-119">-Confirm</span></span>
<span data-ttu-id="74d8d-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74d8d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d8d-121">-Containername</span><span class="sxs-lookup"><span data-stu-id="74d8d-121">-ContainerName</span></span>
<span data-ttu-id="74d8d-122">Container Name.</span><span class="sxs-lookup"><span data-stu-id="74d8d-122">Container name.</span></span>

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

### <span data-ttu-id="74d8d-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="74d8d-123">-DatabaseName</span></span>
<span data-ttu-id="74d8d-124">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="74d8d-124">Database name.</span></span>

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

### <span data-ttu-id="74d8d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d8d-125">-DefaultProfile</span></span>
<span data-ttu-id="74d8d-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74d8d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74d8d-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="74d8d-127">-InputObject</span></span>
<span data-ttu-id="74d8d-128">SQL Trigger-Objekt</span><span class="sxs-lookup"><span data-stu-id="74d8d-128">Sql trigger Object</span></span>

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

### <span data-ttu-id="74d8d-129">-Name</span><span class="sxs-lookup"><span data-stu-id="74d8d-129">-Name</span></span>
<span data-ttu-id="74d8d-130">Name des Triggers</span><span class="sxs-lookup"><span data-stu-id="74d8d-130">Trigger name.</span></span>

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

### <span data-ttu-id="74d8d-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="74d8d-131">-ParentObject</span></span>
<span data-ttu-id="74d8d-132">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="74d8d-132">Sql Container object.</span></span>

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

### <span data-ttu-id="74d8d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74d8d-133">-ResourceGroupName</span></span>
<span data-ttu-id="74d8d-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="74d8d-134">Name of resource group.</span></span>

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

### <span data-ttu-id="74d8d-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="74d8d-135">-TriggerOperation</span></span>
<span data-ttu-id="74d8d-136">Der Vorgang, dem der Trigger zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="74d8d-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="74d8d-137">Mögliche Werte sind: "alle", "erstellen", "Aktualisieren", "Löschen", "ersetzen"</span><span class="sxs-lookup"><span data-stu-id="74d8d-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="74d8d-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="74d8d-138">-TriggerType</span></span>
<span data-ttu-id="74d8d-139">Der Typ des Triggers.</span><span class="sxs-lookup"><span data-stu-id="74d8d-139">Type of the Trigger.</span></span>
<span data-ttu-id="74d8d-140">Mögliche Werte sind: ' Pre ', ' Post '</span><span class="sxs-lookup"><span data-stu-id="74d8d-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="74d8d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d8d-141">-WhatIf</span></span>
<span data-ttu-id="74d8d-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74d8d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74d8d-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74d8d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d8d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d8d-144">CommonParameters</span></span>
<span data-ttu-id="74d8d-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d8d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d8d-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74d8d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d8d-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74d8d-147">INPUTS</span></span>

### <span data-ttu-id="74d8d-148">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="74d8d-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="74d8d-149">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="74d8d-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="74d8d-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74d8d-150">OUTPUTS</span></span>

### <span data-ttu-id="74d8d-151">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="74d8d-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="74d8d-152">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="74d8d-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="74d8d-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="74d8d-153">NOTES</span></span>

## <span data-ttu-id="74d8d-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74d8d-154">RELATED LINKS</span></span>
