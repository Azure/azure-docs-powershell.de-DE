---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: d90df542fd2acc925531f4bf9da7244ea1831a63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996884"
---
# <span data-ttu-id="ccaa4-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="ccaa4-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="ccaa4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ccaa4-102">SYNOPSIS</span></span>
<span data-ttu-id="ccaa4-103">Aktualisiert den Durchsatz einer CosmosDB-MongoDB-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ccaa4-103">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="ccaa4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccaa4-104">SYNTAX</span></span>

### <span data-ttu-id="ccaa4-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ccaa4-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaa4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccaa4-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccaa4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccaa4-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ccaa4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ccaa4-108">EXAMPLES</span></span>

### <span data-ttu-id="ccaa4-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ccaa4-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="ccaa4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccaa4-110">PARAMETERS</span></span>

### <span data-ttu-id="ccaa4-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="ccaa4-111">-AccountName</span></span>
<span data-ttu-id="ccaa4-112">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="ccaa4-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ccaa4-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ccaa4-113">-Confirm</span></span>
<span data-ttu-id="ccaa4-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ccaa4-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccaa4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccaa4-115">-DefaultProfile</span></span>
<span data-ttu-id="ccaa4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ccaa4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccaa4-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ccaa4-117">-InputObject</span></span>
<span data-ttu-id="ccaa4-118">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="ccaa4-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ccaa4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ccaa4-119">-Name</span></span>
<span data-ttu-id="ccaa4-120">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="ccaa4-120">Database name.</span></span>

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

### <span data-ttu-id="ccaa4-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ccaa4-121">-ParentObject</span></span>
<span data-ttu-id="ccaa4-122">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="ccaa4-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaa4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccaa4-123">-ResourceGroupName</span></span>
<span data-ttu-id="ccaa4-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ccaa4-124">Name of resource group.</span></span>

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

### <span data-ttu-id="ccaa4-125">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="ccaa4-125">-Throughput</span></span>
<span data-ttu-id="ccaa4-126">Der Durchsatz der Mongo-Datenbank (ru/s).</span><span class="sxs-lookup"><span data-stu-id="ccaa4-126">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="ccaa4-127">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="ccaa4-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaa4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccaa4-128">-WhatIf</span></span>
<span data-ttu-id="ccaa4-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ccaa4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccaa4-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccaa4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccaa4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccaa4-131">CommonParameters</span></span>
<span data-ttu-id="ccaa4-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccaa4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccaa4-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccaa4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccaa4-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ccaa4-134">INPUTS</span></span>

### <span data-ttu-id="ccaa4-135">Keine</span><span class="sxs-lookup"><span data-stu-id="ccaa4-135">None</span></span>

## <span data-ttu-id="ccaa4-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ccaa4-136">OUTPUTS</span></span>

### <span data-ttu-id="ccaa4-137">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ccaa4-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ccaa4-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="ccaa4-138">NOTES</span></span>

## <span data-ttu-id="ccaa4-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ccaa4-139">RELATED LINKS</span></span>
