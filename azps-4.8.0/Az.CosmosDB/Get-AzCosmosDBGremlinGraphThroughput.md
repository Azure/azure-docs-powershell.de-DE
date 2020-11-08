---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174409"
---
# <span data-ttu-id="b610a-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="b610a-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="b610a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b610a-102">SYNOPSIS</span></span>
<span data-ttu-id="b610a-103">Ruft den Durchsatz eines CosmosDB-Gremlin-Diagramms ab.</span><span class="sxs-lookup"><span data-stu-id="b610a-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b610a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b610a-104">SYNTAX</span></span>

### <span data-ttu-id="b610a-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b610a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b610a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b610a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b610a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b610a-107">DESCRIPTION</span></span>
<span data-ttu-id="b610a-108">Das Cmdlet " **Get-AzCosmosDBGremlinGraphThroughput** " Ruft den Durchsatz eines CosmosDB Gremlin-Diagramms ab.</span><span class="sxs-lookup"><span data-stu-id="b610a-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b610a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b610a-109">EXAMPLES</span></span>

### <span data-ttu-id="b610a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b610a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="b610a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b610a-111">PARAMETERS</span></span>

### <span data-ttu-id="b610a-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b610a-112">-AccountName</span></span>
<span data-ttu-id="b610a-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="b610a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b610a-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b610a-114">-Confirm</span></span>
<span data-ttu-id="b610a-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b610a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b610a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b610a-116">-DatabaseName</span></span>
<span data-ttu-id="b610a-117">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="b610a-117">Database name.</span></span>

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

### <span data-ttu-id="b610a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b610a-118">-DefaultProfile</span></span>
<span data-ttu-id="b610a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b610a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b610a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b610a-120">-InputObject</span></span>
<span data-ttu-id="b610a-121">Gremlin-Diagrammobjekt</span><span class="sxs-lookup"><span data-stu-id="b610a-121">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b610a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b610a-122">-Name</span></span>
<span data-ttu-id="b610a-123">Gremlin-Diagramm Name</span><span class="sxs-lookup"><span data-stu-id="b610a-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="b610a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b610a-124">-ResourceGroupName</span></span>
<span data-ttu-id="b610a-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b610a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="b610a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b610a-126">-WhatIf</span></span>
<span data-ttu-id="b610a-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b610a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b610a-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b610a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b610a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b610a-129">CommonParameters</span></span>
<span data-ttu-id="b610a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b610a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b610a-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b610a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b610a-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b610a-132">INPUTS</span></span>

### <span data-ttu-id="b610a-133">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="b610a-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="b610a-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b610a-134">OUTPUTS</span></span>

### <span data-ttu-id="b610a-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b610a-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b610a-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b610a-136">NOTES</span></span>

## <span data-ttu-id="b610a-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b610a-137">RELATED LINKS</span></span>
