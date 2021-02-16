---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 5c3150e2bdb81c8864116bc521b9f07f2ea43e1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166169"
---
# <span data-ttu-id="63870-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="63870-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="63870-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63870-102">SYNOPSIS</span></span>
<span data-ttu-id="63870-103">Löscht eine Datenbank des Unterndb-Gremlin-Kontos.</span><span class="sxs-lookup"><span data-stu-id="63870-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="63870-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63870-104">SYNTAX</span></span>

### <span data-ttu-id="63870-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="63870-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63870-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63870-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63870-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63870-107">DESCRIPTION</span></span>
<span data-ttu-id="63870-108">Das **Cmdlet "Remove-AzCosmosDBGremlinDatabase"** löscht eine Datenbank des Ordners".</span><span class="sxs-lookup"><span data-stu-id="63870-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="63870-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="63870-109">EXAMPLES</span></span>

### <span data-ttu-id="63870-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="63870-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="63870-111">Das Cmdlet gibt ein Objekt vom Typ boolesch (wenn -PassThru übergeben wird) zurück, das "true" ist, wenn das Löschen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="63870-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="63870-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63870-112">PARAMETERS</span></span>

### <span data-ttu-id="63870-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="63870-113">-AccountName</span></span>
<span data-ttu-id="63870-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="63870-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="63870-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63870-115">-Confirm</span></span>
<span data-ttu-id="63870-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63870-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63870-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63870-117">-DefaultProfile</span></span>
<span data-ttu-id="63870-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63870-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63870-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63870-119">-InputObject</span></span>
<span data-ttu-id="63870-120">Das Objekt "Gremlin-Datenbank".</span><span class="sxs-lookup"><span data-stu-id="63870-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="63870-121">-Name</span><span class="sxs-lookup"><span data-stu-id="63870-121">-Name</span></span>
<span data-ttu-id="63870-122">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="63870-122">Database name.</span></span>

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

### <span data-ttu-id="63870-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63870-123">-PassThru</span></span>
<span data-ttu-id="63870-124">Wird auf "true" festgelegt, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="63870-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="63870-125">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war, und andern falls nicht, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="63870-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="63870-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63870-126">-ResourceGroupName</span></span>
<span data-ttu-id="63870-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="63870-127">Name of resource group.</span></span>

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

### <span data-ttu-id="63870-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="63870-128">-WhatIf</span></span>
<span data-ttu-id="63870-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63870-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63870-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63870-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63870-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63870-131">CommonParameters</span></span>
<span data-ttu-id="63870-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63870-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63870-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63870-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63870-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="63870-134">INPUTS</span></span>

### <span data-ttu-id="63870-135">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="63870-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="63870-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="63870-136">OUTPUTS</span></span>

### <span data-ttu-id="63870-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="63870-137">System.Void</span></span>

### <span data-ttu-id="63870-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="63870-138">System.Boolean</span></span>

## <span data-ttu-id="63870-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="63870-139">NOTES</span></span>

## <span data-ttu-id="63870-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="63870-140">RELATED LINKS</span></span>
