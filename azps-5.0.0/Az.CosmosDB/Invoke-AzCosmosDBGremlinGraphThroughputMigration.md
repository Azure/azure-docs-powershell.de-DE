---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16a477febeb5c0272f3e8cc36f577b0659f4826f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299434"
---
# <span data-ttu-id="9f416-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="9f416-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="9f416-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f416-102">SYNOPSIS</span></span>
<span data-ttu-id="9f416-103">Verwenden Sie diese Vorgehensweise, um den AutoScale-Durchsatz auf manuellen Durchsatz zu migrieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="9f416-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="9f416-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f416-104">SYNTAX</span></span>

### <span data-ttu-id="9f416-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f416-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f416-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f416-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f416-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f416-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f416-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f416-108">DESCRIPTION</span></span>
<span data-ttu-id="9f416-109">ThroughpyteType Parameter definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="9f416-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="9f416-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f416-110">EXAMPLES</span></span>

### <span data-ttu-id="9f416-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9f416-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```


## <span data-ttu-id="9f416-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f416-112">PARAMETERS</span></span>

### <span data-ttu-id="9f416-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="9f416-113">-AccountName</span></span>
<span data-ttu-id="9f416-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="9f416-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9f416-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9f416-115">-Confirm</span></span>
<span data-ttu-id="9f416-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f416-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f416-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9f416-117">-DatabaseName</span></span>
<span data-ttu-id="9f416-118">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="9f416-118">Database name.</span></span>

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

### <span data-ttu-id="9f416-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f416-119">-DefaultProfile</span></span>
<span data-ttu-id="9f416-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9f416-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f416-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9f416-121">-InputObject</span></span>
<span data-ttu-id="9f416-122">Gremlin-Diagrammobjekt</span><span class="sxs-lookup"><span data-stu-id="9f416-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="9f416-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9f416-123">-Name</span></span>
<span data-ttu-id="9f416-124">Gremlin-Diagramm Name</span><span class="sxs-lookup"><span data-stu-id="9f416-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="9f416-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9f416-125">-ParentObject</span></span>
<span data-ttu-id="9f416-126">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="9f416-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="9f416-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f416-127">-ResourceGroupName</span></span>
<span data-ttu-id="9f416-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9f416-128">Name of resource group.</span></span>

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

### <span data-ttu-id="9f416-129">-Durchsatztyp</span><span class="sxs-lookup"><span data-stu-id="9f416-129">-ThroughputType</span></span>
<span data-ttu-id="9f416-130">Der durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f416-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="9f416-131">Mögliche Werte sind: AutoScale, manuell.</span><span class="sxs-lookup"><span data-stu-id="9f416-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="9f416-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f416-132">-WhatIf</span></span>
<span data-ttu-id="9f416-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f416-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f416-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f416-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f416-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f416-135">CommonParameters</span></span>
<span data-ttu-id="9f416-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f416-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f416-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f416-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f416-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f416-138">INPUTS</span></span>

### <span data-ttu-id="9f416-139">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9f416-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="9f416-140">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="9f416-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="9f416-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f416-141">OUTPUTS</span></span>

### <span data-ttu-id="9f416-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9f416-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9f416-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f416-143">NOTES</span></span>

## <span data-ttu-id="9f416-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f416-144">RELATED LINKS</span></span>
