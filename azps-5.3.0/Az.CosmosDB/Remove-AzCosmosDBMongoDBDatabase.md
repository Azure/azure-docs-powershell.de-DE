---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472793"
---
# <span data-ttu-id="2ea5f-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="2ea5f-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="2ea5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ea5f-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea5f-103">Löscht eine Datenbank des 1.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="2ea5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ea5f-104">SYNTAX</span></span>

### <span data-ttu-id="2ea5f-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ea5f-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ea5f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ea5f-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ea5f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ea5f-107">DESCRIPTION</span></span>
<span data-ttu-id="2ea5f-108">Mit **dem Cmdlet "Remove-AzCosmosDBMongoDBDatabase"** wird eine Datenbank des Ordners "MongoDB" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="2ea5f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ea5f-109">EXAMPLES</span></span>

### <span data-ttu-id="2ea5f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2ea5f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="2ea5f-111">Das Cmdlet gibt ein Objekt vom Typ boolesch (wenn -PassThru übergeben wird) zurück, das "true" ist, wenn das Löschen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="2ea5f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ea5f-112">PARAMETERS</span></span>

### <span data-ttu-id="2ea5f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ea5f-113">-AccountName</span></span>
<span data-ttu-id="2ea5f-114">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="2ea5f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2ea5f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ea5f-115">-Confirm</span></span>
<span data-ttu-id="2ea5f-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ea5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea5f-117">-DefaultProfile</span></span>
<span data-ttu-id="2ea5f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ea5f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ea5f-119">-InputObject</span></span>
<span data-ttu-id="2ea5f-120">Mongo-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea5f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2ea5f-121">-Name</span></span>
<span data-ttu-id="2ea5f-122">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-122">Database name.</span></span>

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

### <span data-ttu-id="2ea5f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ea5f-123">-PassThru</span></span>
<span data-ttu-id="2ea5f-124">Wird auf "true" festgelegt, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="2ea5f-125">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war und andern falls nicht ein Fehler ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="2ea5f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea5f-126">-ResourceGroupName</span></span>
<span data-ttu-id="2ea5f-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-127">Name of resource group.</span></span>

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

### <span data-ttu-id="2ea5f-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2ea5f-128">-WhatIf</span></span>
<span data-ttu-id="2ea5f-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ea5f-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ea5f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea5f-131">CommonParameters</span></span>
<span data-ttu-id="2ea5f-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea5f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea5f-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ea5f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea5f-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ea5f-134">INPUTS</span></span>

### <span data-ttu-id="2ea5f-135">Microsoft.Azure.Commands.ExesDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2ea5f-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="2ea5f-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ea5f-136">OUTPUTS</span></span>

### <span data-ttu-id="2ea5f-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="2ea5f-137">System.Void</span></span>

### <span data-ttu-id="2ea5f-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ea5f-138">System.Boolean</span></span>

## <span data-ttu-id="2ea5f-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2ea5f-139">NOTES</span></span>

## <span data-ttu-id="2ea5f-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2ea5f-140">RELATED LINKS</span></span>
