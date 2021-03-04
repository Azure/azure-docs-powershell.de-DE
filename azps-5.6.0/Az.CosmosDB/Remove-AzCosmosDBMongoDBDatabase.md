---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: aa5934de20812a8f8a5ebf76c4b23e01cb59d2b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941267"
---
# <span data-ttu-id="68c01-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="68c01-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="68c01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68c01-102">SYNOPSIS</span></span>
<span data-ttu-id="68c01-103">Löscht eine CosmosDB-MongoDB-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="68c01-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="68c01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68c01-104">SYNTAX</span></span>

### <span data-ttu-id="68c01-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="68c01-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68c01-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68c01-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68c01-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68c01-107">DESCRIPTION</span></span>
<span data-ttu-id="68c01-108">Das **Cmdlet Remove-AzCosmosDBMongoDBDatabase** löscht eine CosmosDB MongoDB-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="68c01-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="68c01-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="68c01-109">EXAMPLES</span></span>

### <span data-ttu-id="68c01-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="68c01-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="68c01-111">Das Cmdlet gibt ein Objekt vom Typ bool(wenn -PassThru übergeben wird) zurück, das wahr ist, wenn das Löschen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="68c01-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="68c01-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="68c01-112">PARAMETERS</span></span>

### <span data-ttu-id="68c01-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="68c01-113">-AccountName</span></span>
<span data-ttu-id="68c01-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="68c01-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="68c01-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="68c01-115">-Confirm</span></span>
<span data-ttu-id="68c01-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68c01-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68c01-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68c01-117">-DefaultProfile</span></span>
<span data-ttu-id="68c01-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68c01-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68c01-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68c01-119">-InputObject</span></span>
<span data-ttu-id="68c01-120">Mongo-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="68c01-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="68c01-121">-Name</span><span class="sxs-lookup"><span data-stu-id="68c01-121">-Name</span></span>
<span data-ttu-id="68c01-122">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="68c01-122">Database name.</span></span>

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

### <span data-ttu-id="68c01-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68c01-123">-PassThru</span></span>
<span data-ttu-id="68c01-124">Um auf true festgelegt zu sein, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="68c01-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="68c01-125">Die Ausgabe ist true, wenn der Vorgang erfolgreich war und ein Fehler ausgelöst wird, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="68c01-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="68c01-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68c01-126">-ResourceGroupName</span></span>
<span data-ttu-id="68c01-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="68c01-127">Name of resource group.</span></span>

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

### <span data-ttu-id="68c01-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68c01-128">-WhatIf</span></span>
<span data-ttu-id="68c01-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68c01-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68c01-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68c01-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68c01-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68c01-131">CommonParameters</span></span>
<span data-ttu-id="68c01-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68c01-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68c01-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68c01-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68c01-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="68c01-134">INPUTS</span></span>

### <span data-ttu-id="68c01-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="68c01-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="68c01-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="68c01-136">OUTPUTS</span></span>

### <span data-ttu-id="68c01-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="68c01-137">System.Void</span></span>

### <span data-ttu-id="68c01-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="68c01-138">System.Boolean</span></span>

## <span data-ttu-id="68c01-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="68c01-139">NOTES</span></span>

## <span data-ttu-id="68c01-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="68c01-140">RELATED LINKS</span></span>
