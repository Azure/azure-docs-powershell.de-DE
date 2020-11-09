---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299152"
---
# <span data-ttu-id="dbff1-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="dbff1-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="dbff1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbff1-102">SYNOPSIS</span></span>
<span data-ttu-id="dbff1-103">Löscht eine CosmosDB-MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="dbff1-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="dbff1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbff1-104">SYNTAX</span></span>

### <span data-ttu-id="dbff1-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbff1-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbff1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbff1-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbff1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbff1-107">DESCRIPTION</span></span>
<span data-ttu-id="dbff1-108">Das Cmdlet **Remove-AzCosmosDBMongoDBCollection** löscht eine CosmosDB MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="dbff1-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="dbff1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbff1-109">EXAMPLES</span></span>

### <span data-ttu-id="dbff1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dbff1-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="dbff1-111">Das Cmdlet gibt ein Objekt vom Typ bool zurück (wenn-passthru übergeben wird), das wahr ist, wenn der Löschvorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="dbff1-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="dbff1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbff1-112">PARAMETERS</span></span>

### <span data-ttu-id="dbff1-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="dbff1-113">-AccountName</span></span>
<span data-ttu-id="dbff1-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="dbff1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dbff1-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dbff1-115">-Confirm</span></span>
<span data-ttu-id="dbff1-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbff1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbff1-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dbff1-117">-DatabaseName</span></span>
<span data-ttu-id="dbff1-118">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="dbff1-118">Database name.</span></span>

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

### <span data-ttu-id="dbff1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbff1-119">-DefaultProfile</span></span>
<span data-ttu-id="dbff1-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dbff1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbff1-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dbff1-121">-InputObject</span></span>
<span data-ttu-id="dbff1-122">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="dbff1-122">Sql Container object.</span></span>

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

### <span data-ttu-id="dbff1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="dbff1-123">-Name</span></span>
<span data-ttu-id="dbff1-124">Name der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="dbff1-124">Collection name.</span></span>

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

### <span data-ttu-id="dbff1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbff1-125">-PassThru</span></span>
<span data-ttu-id="dbff1-126">Auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="dbff1-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="dbff1-127">Die Ausgabe ist wahr, wenn der Vorgang erfolgreich war, und andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="dbff1-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="dbff1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbff1-128">-ResourceGroupName</span></span>
<span data-ttu-id="dbff1-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dbff1-129">Name of resource group.</span></span>

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

### <span data-ttu-id="dbff1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbff1-130">-WhatIf</span></span>
<span data-ttu-id="dbff1-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbff1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbff1-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbff1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbff1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbff1-133">CommonParameters</span></span>
<span data-ttu-id="dbff1-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbff1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbff1-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbff1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbff1-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbff1-136">INPUTS</span></span>

### <span data-ttu-id="dbff1-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="dbff1-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="dbff1-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbff1-138">OUTPUTS</span></span>

### <span data-ttu-id="dbff1-139">System. void</span><span class="sxs-lookup"><span data-stu-id="dbff1-139">System.Void</span></span>

### <span data-ttu-id="dbff1-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dbff1-140">System.Boolean</span></span>

## <span data-ttu-id="dbff1-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbff1-141">NOTES</span></span>

## <span data-ttu-id="dbff1-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbff1-142">RELATED LINKS</span></span>
