---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144468"
---
# <span data-ttu-id="878ca-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="878ca-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="878ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="878ca-102">SYNOPSIS</span></span>
<span data-ttu-id="878ca-103">Löscht eine AbosDB MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="878ca-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="878ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="878ca-104">SYNTAX</span></span>

### <span data-ttu-id="878ca-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="878ca-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="878ca-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="878ca-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="878ca-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="878ca-107">DESCRIPTION</span></span>
<span data-ttu-id="878ca-108">Das **Cmdlet "Remove-AzCosmosDBMongoDBCollection"** löscht eine AbosDB MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="878ca-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="878ca-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="878ca-109">EXAMPLES</span></span>

### <span data-ttu-id="878ca-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="878ca-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="878ca-111">Das Cmdlet gibt ein Objekt vom Typ boolesch (wenn -PassThru übergeben wird) zurück, das "true" ist, wenn das Löschen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="878ca-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="878ca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="878ca-112">PARAMETERS</span></span>

### <span data-ttu-id="878ca-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="878ca-113">-AccountName</span></span>
<span data-ttu-id="878ca-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="878ca-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="878ca-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="878ca-115">-Confirm</span></span>
<span data-ttu-id="878ca-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="878ca-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="878ca-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="878ca-117">-DatabaseName</span></span>
<span data-ttu-id="878ca-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="878ca-118">Database name.</span></span>

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

### <span data-ttu-id="878ca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="878ca-119">-DefaultProfile</span></span>
<span data-ttu-id="878ca-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="878ca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="878ca-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="878ca-121">-InputObject</span></span>
<span data-ttu-id="878ca-122">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="878ca-122">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="878ca-123">-Name</span><span class="sxs-lookup"><span data-stu-id="878ca-123">-Name</span></span>
<span data-ttu-id="878ca-124">Sammlungsname.</span><span class="sxs-lookup"><span data-stu-id="878ca-124">Collection name.</span></span>

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

### <span data-ttu-id="878ca-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="878ca-125">-PassThru</span></span>
<span data-ttu-id="878ca-126">Soll auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="878ca-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="878ca-127">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war, und andern falls nicht, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="878ca-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="878ca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="878ca-128">-ResourceGroupName</span></span>
<span data-ttu-id="878ca-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="878ca-129">Name of resource group.</span></span>

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

### <span data-ttu-id="878ca-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="878ca-130">-WhatIf</span></span>
<span data-ttu-id="878ca-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="878ca-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="878ca-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="878ca-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="878ca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="878ca-133">CommonParameters</span></span>
<span data-ttu-id="878ca-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="878ca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="878ca-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="878ca-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="878ca-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="878ca-136">INPUTS</span></span>

### <span data-ttu-id="878ca-137">Microsoft.Azure.Commands.ExesDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="878ca-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="878ca-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="878ca-138">OUTPUTS</span></span>

### <span data-ttu-id="878ca-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="878ca-139">System.Void</span></span>

### <span data-ttu-id="878ca-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="878ca-140">System.Boolean</span></span>

## <span data-ttu-id="878ca-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="878ca-141">NOTES</span></span>

## <span data-ttu-id="878ca-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="878ca-142">RELATED LINKS</span></span>
