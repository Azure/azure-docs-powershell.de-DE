---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299043"
---
# <span data-ttu-id="6fe8e-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="6fe8e-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="6fe8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6fe8e-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe8e-103">Aktualisiert den Durchsatz eines CosmosDB-Gremlin-Diagramms.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="6fe8e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fe8e-104">SYNTAX</span></span>

### <span data-ttu-id="6fe8e-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6fe8e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fe8e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fe8e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fe8e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fe8e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fe8e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fe8e-108">DESCRIPTION</span></span>
<span data-ttu-id="6fe8e-109">Aktualisiert den Durchsatz eines CosmosDB-Gremlin-Diagramms.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="6fe8e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6fe8e-110">EXAMPLES</span></span>

### <span data-ttu-id="6fe8e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6fe8e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="6fe8e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fe8e-112">PARAMETERS</span></span>

### <span data-ttu-id="6fe8e-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="6fe8e-113">-AccountName</span></span>
<span data-ttu-id="6fe8e-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6fe8e-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="6fe8e-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="6fe8e-116">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="6fe8e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6fe8e-117">-Confirm</span></span>
<span data-ttu-id="6fe8e-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fe8e-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6fe8e-119">-DatabaseName</span></span>
<span data-ttu-id="6fe8e-120">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="6fe8e-120">Database name.</span></span>

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

### <span data-ttu-id="6fe8e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe8e-121">-DefaultProfile</span></span>
<span data-ttu-id="6fe8e-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fe8e-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6fe8e-123">-InputObject</span></span>
<span data-ttu-id="6fe8e-124">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="6fe8e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6fe8e-125">-Name</span></span>
<span data-ttu-id="6fe8e-126">Gremlin-Diagramm Name</span><span class="sxs-lookup"><span data-stu-id="6fe8e-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="6fe8e-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6fe8e-127">-ParentObject</span></span>
<span data-ttu-id="6fe8e-128">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-128">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe8e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe8e-129">-ResourceGroupName</span></span>
<span data-ttu-id="6fe8e-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-130">Name of resource group.</span></span>

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

### <span data-ttu-id="6fe8e-131">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="6fe8e-131">-Throughput</span></span>
<span data-ttu-id="6fe8e-132">Der Durchsatz von Gremlin Graph (ru/s).</span><span class="sxs-lookup"><span data-stu-id="6fe8e-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="6fe8e-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-133">Default value is 400.</span></span>

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

### <span data-ttu-id="6fe8e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fe8e-134">-WhatIf</span></span>
<span data-ttu-id="6fe8e-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fe8e-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fe8e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe8e-137">CommonParameters</span></span>
<span data-ttu-id="6fe8e-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe8e-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fe8e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe8e-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6fe8e-140">INPUTS</span></span>

### <span data-ttu-id="6fe8e-141">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="6fe8e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="6fe8e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6fe8e-142">OUTPUTS</span></span>

### <span data-ttu-id="6fe8e-143">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6fe8e-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6fe8e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="6fe8e-144">NOTES</span></span>

## <span data-ttu-id="6fe8e-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6fe8e-145">RELATED LINKS</span></span>
