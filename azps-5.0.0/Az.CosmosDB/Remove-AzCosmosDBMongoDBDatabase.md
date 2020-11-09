---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299151"
---
# <span data-ttu-id="9de50-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="9de50-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="9de50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9de50-102">SYNOPSIS</span></span>
<span data-ttu-id="9de50-103">Löscht eine CosmosDB-MongoDB-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9de50-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="9de50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9de50-104">SYNTAX</span></span>

### <span data-ttu-id="9de50-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9de50-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9de50-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9de50-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9de50-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9de50-107">DESCRIPTION</span></span>
<span data-ttu-id="9de50-108">Das Cmdlet **Remove-AzCosmosDBMongoDBDatabase** löscht eine CosmosDB MongoDB-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9de50-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="9de50-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9de50-109">EXAMPLES</span></span>

### <span data-ttu-id="9de50-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9de50-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="9de50-111">Das Cmdlet gibt ein Objekt vom Typ bool zurück (wenn-passthru übergeben wird), das wahr ist, wenn der Löschvorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="9de50-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="9de50-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9de50-112">PARAMETERS</span></span>

### <span data-ttu-id="9de50-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="9de50-113">-AccountName</span></span>
<span data-ttu-id="9de50-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="9de50-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9de50-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9de50-115">-Confirm</span></span>
<span data-ttu-id="9de50-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9de50-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9de50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de50-117">-DefaultProfile</span></span>
<span data-ttu-id="9de50-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9de50-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9de50-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9de50-119">-InputObject</span></span>
<span data-ttu-id="9de50-120">Mongo-Datenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="9de50-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="9de50-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9de50-121">-Name</span></span>
<span data-ttu-id="9de50-122">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="9de50-122">Database name.</span></span>

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

### <span data-ttu-id="9de50-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9de50-123">-PassThru</span></span>
<span data-ttu-id="9de50-124">Auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="9de50-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="9de50-125">Die Ausgabe ist wahr, wenn der Vorgang erfolgreich war, und andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="9de50-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="9de50-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de50-126">-ResourceGroupName</span></span>
<span data-ttu-id="9de50-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9de50-127">Name of resource group.</span></span>

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

### <span data-ttu-id="9de50-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9de50-128">-WhatIf</span></span>
<span data-ttu-id="9de50-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9de50-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9de50-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9de50-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9de50-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de50-131">CommonParameters</span></span>
<span data-ttu-id="9de50-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de50-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de50-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9de50-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de50-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9de50-134">INPUTS</span></span>

### <span data-ttu-id="9de50-135">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9de50-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="9de50-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9de50-136">OUTPUTS</span></span>

### <span data-ttu-id="9de50-137">System. void</span><span class="sxs-lookup"><span data-stu-id="9de50-137">System.Void</span></span>

### <span data-ttu-id="9de50-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9de50-138">System.Boolean</span></span>

## <span data-ttu-id="9de50-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="9de50-139">NOTES</span></span>

## <span data-ttu-id="9de50-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9de50-140">RELATED LINKS</span></span>
