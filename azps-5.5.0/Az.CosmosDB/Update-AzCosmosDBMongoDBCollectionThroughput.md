---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163980"
---
# <span data-ttu-id="04471-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="04471-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="04471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04471-102">SYNOPSIS</span></span>
<span data-ttu-id="04471-103">Aktualisiert den Durchsatzwert einer Abtdb MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="04471-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="04471-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04471-104">SYNTAX</span></span>

### <span data-ttu-id="04471-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="04471-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04471-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04471-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04471-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04471-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04471-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04471-108">DESCRIPTION</span></span>
<span data-ttu-id="04471-109">Aktualisiert den Durchsatzwert einer Abtdb MongoDB-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="04471-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="04471-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04471-110">EXAMPLES</span></span>

### <span data-ttu-id="04471-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="04471-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="04471-112">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="04471-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="04471-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04471-113">PARAMETERS</span></span>

### <span data-ttu-id="04471-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="04471-114">-AccountName</span></span>
<span data-ttu-id="04471-115">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="04471-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="04471-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="04471-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="04471-117">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="04471-117">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04471-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04471-118">-Confirm</span></span>
<span data-ttu-id="04471-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04471-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04471-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="04471-120">-DatabaseName</span></span>
<span data-ttu-id="04471-121">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="04471-121">Database name.</span></span>

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

### <span data-ttu-id="04471-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04471-122">-DefaultProfile</span></span>
<span data-ttu-id="04471-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04471-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04471-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04471-124">-InputObject</span></span>
<span data-ttu-id="04471-125">Mongo-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="04471-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="04471-126">-Name</span><span class="sxs-lookup"><span data-stu-id="04471-126">-Name</span></span>
<span data-ttu-id="04471-127">Sammlungsname.</span><span class="sxs-lookup"><span data-stu-id="04471-127">Collection name.</span></span>

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

### <span data-ttu-id="04471-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="04471-128">-ParentObject</span></span>
<span data-ttu-id="04471-129">Mongo-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="04471-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="04471-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04471-130">-ResourceGroupName</span></span>
<span data-ttu-id="04471-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="04471-131">Name of resource group.</span></span>

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

### <span data-ttu-id="04471-132">-Throughput</span><span class="sxs-lookup"><span data-stu-id="04471-132">-Throughput</span></span>
<span data-ttu-id="04471-133">Der Durchsatz SQL Container (RU/s).</span><span class="sxs-lookup"><span data-stu-id="04471-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="04471-134">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="04471-134">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04471-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="04471-135">-WhatIf</span></span>
<span data-ttu-id="04471-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04471-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04471-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04471-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04471-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04471-138">CommonParameters</span></span>
<span data-ttu-id="04471-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04471-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04471-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04471-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04471-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04471-141">INPUTS</span></span>

### <span data-ttu-id="04471-142">Microsoft.Azure.Commands.ExesDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="04471-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="04471-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04471-143">OUTPUTS</span></span>

### <span data-ttu-id="04471-144">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="04471-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="04471-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="04471-145">NOTES</span></span>

## <span data-ttu-id="04471-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="04471-146">RELATED LINKS</span></span>
