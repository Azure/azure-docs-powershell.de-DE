---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 8aca11c8ce56c42842e96fa1e3623979612ffec7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170987"
---
# <span data-ttu-id="5d3fe-101">Remove-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="5d3fe-101">Remove-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="5d3fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="5d3fe-103">Löscht den Auslöser für Sql-SkriptsDB.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-103">Deletes the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="5d3fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d3fe-104">SYNTAX</span></span>

### <span data-ttu-id="5d3fe-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3fe-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3fe-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3fe-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -InputObject <PSSqlTriggerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d3fe-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d3fe-107">DESCRIPTION</span></span>
<span data-ttu-id="5d3fe-108">Das **Cmdlet "Remove-AzCosmosDBSqlTrigger"** löscht den SkriptsDB-Sql-Trigger, der dem angegebenen ResourceGroupName, AccountName und DatabaseName entspricht.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-108">The **Remove-AzCosmosDBSqlTrigger** cmdlet deletes the CosmosDB Sql Trigger corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="5d3fe-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5d3fe-109">EXAMPLES</span></span>

### <span data-ttu-id="5d3fe-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d3fe-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlTrigger -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {triggerName}
```

## <span data-ttu-id="5d3fe-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d3fe-111">PARAMETERS</span></span>

### <span data-ttu-id="5d3fe-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5d3fe-112">-AccountName</span></span>
<span data-ttu-id="5d3fe-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5d3fe-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d3fe-114">-Confirm</span></span>
<span data-ttu-id="5d3fe-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d3fe-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="5d3fe-116">-ContainerName</span></span>
<span data-ttu-id="5d3fe-117">Containername.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-117">Container name.</span></span>

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

### <span data-ttu-id="5d3fe-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5d3fe-118">-DatabaseName</span></span>
<span data-ttu-id="5d3fe-119">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-119">Database name.</span></span>

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

### <span data-ttu-id="5d3fe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d3fe-120">-DefaultProfile</span></span>
<span data-ttu-id="5d3fe-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d3fe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d3fe-122">-InputObject</span></span>
<span data-ttu-id="5d3fe-123">Sql trigger Object</span><span class="sxs-lookup"><span data-stu-id="5d3fe-123">Sql trigger Object</span></span>

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

### <span data-ttu-id="5d3fe-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5d3fe-124">-Name</span></span>
<span data-ttu-id="5d3fe-125">Triggername.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-125">Trigger name.</span></span>

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

### <span data-ttu-id="5d3fe-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d3fe-126">-PassThru</span></span>
<span data-ttu-id="5d3fe-127">Soll auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="5d3fe-128">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war, und andern falls nicht, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3fe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d3fe-129">-ResourceGroupName</span></span>
<span data-ttu-id="5d3fe-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-130">Name of resource group.</span></span>

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

### <span data-ttu-id="5d3fe-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5d3fe-131">-WhatIf</span></span>
<span data-ttu-id="5d3fe-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d3fe-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d3fe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d3fe-134">CommonParameters</span></span>
<span data-ttu-id="5d3fe-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d3fe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d3fe-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d3fe-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d3fe-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5d3fe-137">INPUTS</span></span>

### <span data-ttu-id="5d3fe-138">Keine</span><span class="sxs-lookup"><span data-stu-id="5d3fe-138">None</span></span>

## <span data-ttu-id="5d3fe-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5d3fe-139">OUTPUTS</span></span>

### <span data-ttu-id="5d3fe-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="5d3fe-140">System.Void</span></span>

### <span data-ttu-id="5d3fe-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d3fe-141">System.Boolean</span></span>

## <span data-ttu-id="5d3fe-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5d3fe-142">NOTES</span></span>

## <span data-ttu-id="5d3fe-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5d3fe-143">RELATED LINKS</span></span>
