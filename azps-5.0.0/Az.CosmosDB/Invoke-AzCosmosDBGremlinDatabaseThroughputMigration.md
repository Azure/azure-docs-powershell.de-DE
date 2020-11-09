---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlindatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
ms.openlocfilehash: 84039f883937354cf8c8fae3c99bfbc6f73bb574
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299445"
---
# <span data-ttu-id="bc139-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="bc139-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span></span>

## <span data-ttu-id="bc139-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc139-102">SYNOPSIS</span></span>
<span data-ttu-id="bc139-103">Verwenden Sie diese Vorgehensweise, um den AutoScale-Durchsatz auf manuellen Durchsatz zu migrieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="bc139-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="bc139-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc139-104">SYNTAX</span></span>

### <span data-ttu-id="bc139-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bc139-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc139-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc139-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc139-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc139-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc139-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc139-108">DESCRIPTION</span></span>
<span data-ttu-id="bc139-109">ThroughpyteType Parameter definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="bc139-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="bc139-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc139-110">EXAMPLES</span></span>

### <span data-ttu-id="bc139-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bc139-111">Example 1</span></span>
```powershell
PS C:\> $NewDb =  New-AzCosmosDBGremlinDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinDatabaseThroughputMigration -InputObject $NewDb -ThroughputType Autoscale
```


## <span data-ttu-id="bc139-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc139-112">PARAMETERS</span></span>

### <span data-ttu-id="bc139-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="bc139-113">-AccountName</span></span>
<span data-ttu-id="bc139-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="bc139-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bc139-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bc139-115">-Confirm</span></span>
<span data-ttu-id="bc139-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc139-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc139-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc139-117">-DefaultProfile</span></span>
<span data-ttu-id="bc139-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc139-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc139-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bc139-119">-InputObject</span></span>
<span data-ttu-id="bc139-120">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="bc139-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc139-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bc139-121">-Name</span></span>
<span data-ttu-id="bc139-122">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="bc139-122">Database name.</span></span>

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

### <span data-ttu-id="bc139-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bc139-123">-ParentObject</span></span>
<span data-ttu-id="bc139-124">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="bc139-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc139-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc139-125">-ResourceGroupName</span></span>
<span data-ttu-id="bc139-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bc139-126">Name of resource group.</span></span>

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

### <span data-ttu-id="bc139-127">-Durchsatztyp</span><span class="sxs-lookup"><span data-stu-id="bc139-127">-ThroughputType</span></span>
<span data-ttu-id="bc139-128">Der durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc139-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="bc139-129">Mögliche Werte sind: AutoScale, manuell.</span><span class="sxs-lookup"><span data-stu-id="bc139-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="bc139-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc139-130">-WhatIf</span></span>
<span data-ttu-id="bc139-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc139-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc139-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc139-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc139-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc139-133">CommonParameters</span></span>
<span data-ttu-id="bc139-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc139-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc139-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc139-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc139-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc139-136">INPUTS</span></span>

### <span data-ttu-id="bc139-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="bc139-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="bc139-138">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="bc139-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="bc139-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc139-139">OUTPUTS</span></span>

### <span data-ttu-id="bc139-140">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="bc139-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bc139-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc139-141">NOTES</span></span>

## <span data-ttu-id="bc139-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc139-142">RELATED LINKS</span></span>
