---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: e2f1449536f9b4db5b743c1a1e352e427ae86821
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299433"
---
# <span data-ttu-id="c97ae-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="c97ae-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="c97ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c97ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c97ae-103">Verwenden Sie diese Vorgehensweise, um den AutoScale-Durchsatz auf manuellen Durchsatz zu migrieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="c97ae-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="c97ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97ae-104">SYNTAX</span></span>

### <span data-ttu-id="c97ae-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c97ae-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c97ae-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c97ae-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c97ae-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c97ae-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c97ae-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c97ae-108">DESCRIPTION</span></span>
<span data-ttu-id="c97ae-109">ThroughpyteType Parameter definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c97ae-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="c97ae-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c97ae-110">EXAMPLES</span></span>

### <span data-ttu-id="c97ae-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c97ae-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```


## <span data-ttu-id="c97ae-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c97ae-112">PARAMETERS</span></span>

### <span data-ttu-id="c97ae-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="c97ae-113">-AccountName</span></span>
<span data-ttu-id="c97ae-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="c97ae-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c97ae-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c97ae-115">-Confirm</span></span>
<span data-ttu-id="c97ae-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c97ae-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c97ae-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c97ae-117">-DatabaseName</span></span>
<span data-ttu-id="c97ae-118">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="c97ae-118">Database name.</span></span>

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

### <span data-ttu-id="c97ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97ae-119">-DefaultProfile</span></span>
<span data-ttu-id="c97ae-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c97ae-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c97ae-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c97ae-121">-InputObject</span></span>
<span data-ttu-id="c97ae-122">Mongo-Sammlungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c97ae-122">Mongo Collection object.</span></span>

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

### <span data-ttu-id="c97ae-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c97ae-123">-Name</span></span>
<span data-ttu-id="c97ae-124">Name der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="c97ae-124">Collection name.</span></span>

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

### <span data-ttu-id="c97ae-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c97ae-125">-ParentObject</span></span>
<span data-ttu-id="c97ae-126">Mongo-Datenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="c97ae-126">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c97ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c97ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="c97ae-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c97ae-128">Name of resource group.</span></span>

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

### <span data-ttu-id="c97ae-129">-Durchsatztyp</span><span class="sxs-lookup"><span data-stu-id="c97ae-129">-ThroughputType</span></span>
<span data-ttu-id="c97ae-130">Der durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c97ae-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="c97ae-131">Mögliche Werte sind: AutoScale, manuell.</span><span class="sxs-lookup"><span data-stu-id="c97ae-131">Possible values are: Autoscale, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c97ae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c97ae-132">-WhatIf</span></span>
<span data-ttu-id="c97ae-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c97ae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c97ae-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c97ae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c97ae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97ae-135">CommonParameters</span></span>
<span data-ttu-id="c97ae-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c97ae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97ae-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c97ae-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97ae-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c97ae-138">INPUTS</span></span>

### <span data-ttu-id="c97ae-139">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c97ae-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="c97ae-140">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="c97ae-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="c97ae-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c97ae-141">OUTPUTS</span></span>

### <span data-ttu-id="c97ae-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c97ae-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c97ae-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c97ae-143">NOTES</span></span>

## <span data-ttu-id="c97ae-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c97ae-144">RELATED LINKS</span></span>
