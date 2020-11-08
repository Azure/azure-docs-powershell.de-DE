---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a67b2a665f763c32876177414a347270f557c914
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995252"
---
# <span data-ttu-id="f4b92-101">Set-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="f4b92-101">Set-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="f4b92-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4b92-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b92-103">Erstellt eine neue oder aktualisiert einen vorhandenen CosmosDB-SQL-Trigger.</span><span class="sxs-lookup"><span data-stu-id="f4b92-103">Creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="f4b92-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4b92-104">SYNTAX</span></span>

### <span data-ttu-id="f4b92-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4b92-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4b92-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4b92-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4b92-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4b92-107">DESCRIPTION</span></span>
<span data-ttu-id="f4b92-108">Das Cmdlet " **Satz-AzCosmosDBSqlTrigger** " erstellt ein neues oder aktualisiert einen vorhandenen CosmosDB SQL-Trigger.</span><span class="sxs-lookup"><span data-stu-id="f4b92-108">The **Set-AzCosmosDBSqlTrigger** cmdlet creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="f4b92-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4b92-109">EXAMPLES</span></span>

### <span data-ttu-id="f4b92-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4b92-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} -Body {sampleBody}

Name                   : {triggerName}
Id                     : {triggerId}
SqlTriggerGetResultsId :
Body                   :
TriggerType            :
TriggerOperation       :
_rid                   :
_ts                    :
_etag                  :
```

## <span data-ttu-id="f4b92-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4b92-111">PARAMETERS</span></span>

### <span data-ttu-id="f4b92-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="f4b92-112">-AccountName</span></span>
<span data-ttu-id="f4b92-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="f4b92-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f4b92-114">-Body</span><span class="sxs-lookup"><span data-stu-id="f4b92-114">-Body</span></span>
<span data-ttu-id="f4b92-115">Der Text des Triggers.</span><span class="sxs-lookup"><span data-stu-id="f4b92-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="f4b92-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4b92-116">-Confirm</span></span>
<span data-ttu-id="f4b92-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4b92-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4b92-118">-Containername</span><span class="sxs-lookup"><span data-stu-id="f4b92-118">-ContainerName</span></span>
<span data-ttu-id="f4b92-119">Container Name.</span><span class="sxs-lookup"><span data-stu-id="f4b92-119">Container name.</span></span>

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

### <span data-ttu-id="f4b92-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4b92-120">-DatabaseName</span></span>
<span data-ttu-id="f4b92-121">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="f4b92-121">Database name.</span></span>

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

### <span data-ttu-id="f4b92-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b92-122">-DefaultProfile</span></span>
<span data-ttu-id="f4b92-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4b92-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4b92-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f4b92-124">-InputObject</span></span>
<span data-ttu-id="f4b92-125">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="f4b92-125">Sql Container object.</span></span>

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

### <span data-ttu-id="f4b92-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f4b92-126">-Name</span></span>
<span data-ttu-id="f4b92-127">Name des Triggers</span><span class="sxs-lookup"><span data-stu-id="f4b92-127">Trigger name.</span></span>

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

### <span data-ttu-id="f4b92-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4b92-128">-ResourceGroupName</span></span>
<span data-ttu-id="f4b92-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f4b92-129">Name of resource group.</span></span>

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

### <span data-ttu-id="f4b92-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="f4b92-130">-TriggerOperation</span></span>
<span data-ttu-id="f4b92-131">Der Vorgang, dem der Trigger zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f4b92-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="f4b92-132">Mögliche Werte sind: "alle", "erstellen", "Aktualisieren", "Löschen", "ersetzen"</span><span class="sxs-lookup"><span data-stu-id="f4b92-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="f4b92-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="f4b92-133">-TriggerType</span></span>
<span data-ttu-id="f4b92-134">Der Typ des Triggers.</span><span class="sxs-lookup"><span data-stu-id="f4b92-134">Type of the Trigger.</span></span>
<span data-ttu-id="f4b92-135">Mögliche Werte sind: ' Pre ', ' Post '</span><span class="sxs-lookup"><span data-stu-id="f4b92-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="f4b92-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4b92-136">-WhatIf</span></span>
<span data-ttu-id="f4b92-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4b92-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4b92-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4b92-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4b92-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b92-139">CommonParameters</span></span>
<span data-ttu-id="f4b92-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4b92-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b92-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4b92-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b92-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4b92-142">INPUTS</span></span>

### <span data-ttu-id="f4b92-143">Keine</span><span class="sxs-lookup"><span data-stu-id="f4b92-143">None</span></span>

## <span data-ttu-id="f4b92-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4b92-144">OUTPUTS</span></span>

### <span data-ttu-id="f4b92-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="f4b92-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="f4b92-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4b92-146">NOTES</span></span>

## <span data-ttu-id="f4b92-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4b92-147">RELATED LINKS</span></span>
