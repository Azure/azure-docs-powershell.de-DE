---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 4838a2de4a61d0c00371ab018d441dcd52bec699
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928267"
---
# <span data-ttu-id="1542e-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="1542e-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="1542e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1542e-102">SYNOPSIS</span></span>
<span data-ttu-id="1542e-103">Löscht ein CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="1542e-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="1542e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1542e-104">SYNTAX</span></span>

### <span data-ttu-id="1542e-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1542e-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1542e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1542e-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1542e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1542e-107">DESCRIPTION</span></span>
<span data-ttu-id="1542e-108">Das **Cmdlet Remove-AzCosmosDBGremlinGraph** löscht ein CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="1542e-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="1542e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1542e-109">EXAMPLES</span></span>

### <span data-ttu-id="1542e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1542e-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="1542e-111">Das Cmdlet gibt ein Objekt vom Typ bool(wenn -PassThru übergeben wird) zurück, das wahr ist, wenn das Löschen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1542e-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="1542e-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1542e-112">PARAMETERS</span></span>

### <span data-ttu-id="1542e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1542e-113">-AccountName</span></span>
<span data-ttu-id="1542e-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="1542e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1542e-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1542e-115">-Confirm</span></span>
<span data-ttu-id="1542e-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1542e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1542e-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1542e-117">-DatabaseName</span></span>
<span data-ttu-id="1542e-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="1542e-118">Database name.</span></span>

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

### <span data-ttu-id="1542e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1542e-119">-DefaultProfile</span></span>
<span data-ttu-id="1542e-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1542e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1542e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1542e-121">-InputObject</span></span>
<span data-ttu-id="1542e-122">Gremlin Graph-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1542e-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="1542e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1542e-123">-Name</span></span>
<span data-ttu-id="1542e-124">Gremlin Graph Name.</span><span class="sxs-lookup"><span data-stu-id="1542e-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="1542e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1542e-125">-PassThru</span></span>
<span data-ttu-id="1542e-126">Um auf true festgelegt zu sein, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="1542e-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="1542e-127">Die Ausgabe ist true, wenn der Vorgang erfolgreich war und ein Fehler ausgelöst wird, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="1542e-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="1542e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1542e-128">-ResourceGroupName</span></span>
<span data-ttu-id="1542e-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1542e-129">Name of resource group.</span></span>

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

### <span data-ttu-id="1542e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1542e-130">-WhatIf</span></span>
<span data-ttu-id="1542e-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1542e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1542e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1542e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1542e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1542e-133">CommonParameters</span></span>
<span data-ttu-id="1542e-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1542e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1542e-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1542e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1542e-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1542e-136">INPUTS</span></span>

### <span data-ttu-id="1542e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="1542e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="1542e-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1542e-138">OUTPUTS</span></span>

### <span data-ttu-id="1542e-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="1542e-139">System.Void</span></span>

### <span data-ttu-id="1542e-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1542e-140">System.Boolean</span></span>

## <span data-ttu-id="1542e-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1542e-141">NOTES</span></span>

## <span data-ttu-id="1542e-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1542e-142">RELATED LINKS</span></span>
