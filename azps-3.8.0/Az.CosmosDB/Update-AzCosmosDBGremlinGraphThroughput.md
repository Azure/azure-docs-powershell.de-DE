---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: ee1527beb11db3027a416277ed04a444dda90af0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996885"
---
# <span data-ttu-id="22bc0-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="22bc0-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="22bc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="22bc0-103">Aktualisiert den Durchsatz eines CosmosDB-Gremlin-Diagramms.</span><span class="sxs-lookup"><span data-stu-id="22bc0-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="22bc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22bc0-104">SYNTAX</span></span>

### <span data-ttu-id="22bc0-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="22bc0-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22bc0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22bc0-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22bc0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22bc0-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinGraphGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22bc0-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22bc0-108">EXAMPLES</span></span>

### <span data-ttu-id="22bc0-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22bc0-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="22bc0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22bc0-110">PARAMETERS</span></span>

### <span data-ttu-id="22bc0-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="22bc0-111">-AccountName</span></span>
<span data-ttu-id="22bc0-112">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="22bc0-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="22bc0-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="22bc0-113">-Confirm</span></span>
<span data-ttu-id="22bc0-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22bc0-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22bc0-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="22bc0-115">-DatabaseName</span></span>
<span data-ttu-id="22bc0-116">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="22bc0-116">Database name.</span></span>

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

### <span data-ttu-id="22bc0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22bc0-117">-DefaultProfile</span></span>
<span data-ttu-id="22bc0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="22bc0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22bc0-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="22bc0-119">-InputObject</span></span>
<span data-ttu-id="22bc0-120">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="22bc0-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="22bc0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="22bc0-121">-Name</span></span>
<span data-ttu-id="22bc0-122">Gremlin-Diagramm Name</span><span class="sxs-lookup"><span data-stu-id="22bc0-122">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="22bc0-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="22bc0-123">-ParentObject</span></span>
<span data-ttu-id="22bc0-124">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="22bc0-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="22bc0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22bc0-125">-ResourceGroupName</span></span>
<span data-ttu-id="22bc0-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="22bc0-126">Name of resource group.</span></span>

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

### <span data-ttu-id="22bc0-127">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="22bc0-127">-Throughput</span></span>
<span data-ttu-id="22bc0-128">Der Durchsatz von Gremlin Graph (ru/s).</span><span class="sxs-lookup"><span data-stu-id="22bc0-128">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="22bc0-129">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="22bc0-129">Default value is 400.</span></span>

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

### <span data-ttu-id="22bc0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22bc0-130">-WhatIf</span></span>
<span data-ttu-id="22bc0-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22bc0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22bc0-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22bc0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22bc0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22bc0-133">CommonParameters</span></span>
<span data-ttu-id="22bc0-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22bc0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22bc0-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22bc0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22bc0-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22bc0-136">INPUTS</span></span>

### <span data-ttu-id="22bc0-137">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="22bc0-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="22bc0-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22bc0-138">OUTPUTS</span></span>

### <span data-ttu-id="22bc0-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="22bc0-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="22bc0-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="22bc0-140">NOTES</span></span>

## <span data-ttu-id="22bc0-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22bc0-141">RELATED LINKS</span></span>
