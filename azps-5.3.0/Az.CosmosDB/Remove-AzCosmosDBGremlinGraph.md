---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 560fcaa33e635eefd4ba94c5c7cbd05cba1cc304
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472794"
---
# <span data-ttu-id="36888-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="36888-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="36888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36888-102">SYNOPSIS</span></span>
<span data-ttu-id="36888-103">Löscht ein Unteredb-Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="36888-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="36888-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36888-104">SYNTAX</span></span>

### <span data-ttu-id="36888-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="36888-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36888-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36888-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36888-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36888-107">DESCRIPTION</span></span>
<span data-ttu-id="36888-108">Das **Cmdlet "Remove-AzCosmosDBGremlinGraph"** löscht ein Untermaindruck-Gremlin-Diagramm.</span><span class="sxs-lookup"><span data-stu-id="36888-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="36888-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36888-109">EXAMPLES</span></span>

### <span data-ttu-id="36888-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36888-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="36888-111">Das Cmdlet gibt ein Objekt vom Typ boolesch (wenn -PassThru übergeben wird) zurück, das wahr ist, wenn das Löschen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="36888-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="36888-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36888-112">PARAMETERS</span></span>

### <span data-ttu-id="36888-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="36888-113">-AccountName</span></span>
<span data-ttu-id="36888-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="36888-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="36888-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36888-115">-Confirm</span></span>
<span data-ttu-id="36888-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36888-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36888-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36888-117">-DatabaseName</span></span>
<span data-ttu-id="36888-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="36888-118">Database name.</span></span>

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

### <span data-ttu-id="36888-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36888-119">-DefaultProfile</span></span>
<span data-ttu-id="36888-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36888-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36888-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36888-121">-InputObject</span></span>
<span data-ttu-id="36888-122">Gremlin Graph-Objekt.</span><span class="sxs-lookup"><span data-stu-id="36888-122">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36888-123">-Name</span><span class="sxs-lookup"><span data-stu-id="36888-123">-Name</span></span>
<span data-ttu-id="36888-124">Gremlin Graph Name.</span><span class="sxs-lookup"><span data-stu-id="36888-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="36888-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36888-125">-PassThru</span></span>
<span data-ttu-id="36888-126">Wird auf "true" festgelegt, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="36888-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="36888-127">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war und andern falls nicht ein Fehler ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="36888-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="36888-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36888-128">-ResourceGroupName</span></span>
<span data-ttu-id="36888-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="36888-129">Name of resource group.</span></span>

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

### <span data-ttu-id="36888-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="36888-130">-WhatIf</span></span>
<span data-ttu-id="36888-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36888-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36888-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36888-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36888-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36888-133">CommonParameters</span></span>
<span data-ttu-id="36888-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36888-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36888-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36888-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36888-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36888-136">INPUTS</span></span>

### <span data-ttu-id="36888-137">Microsoft.Azure.Commands.DiesDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="36888-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="36888-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36888-138">OUTPUTS</span></span>

### <span data-ttu-id="36888-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="36888-139">System.Void</span></span>

### <span data-ttu-id="36888-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36888-140">System.Boolean</span></span>

## <span data-ttu-id="36888-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="36888-141">NOTES</span></span>

## <span data-ttu-id="36888-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="36888-142">RELATED LINKS</span></span>
