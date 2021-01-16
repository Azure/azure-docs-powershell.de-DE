---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301808"
---
# <span data-ttu-id="253ac-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="253ac-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="253ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="253ac-102">SYNOPSIS</span></span>
<span data-ttu-id="253ac-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skala in den manuellen Durchsatz und umgekehrt zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="253ac-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="253ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="253ac-104">SYNTAX</span></span>

### <span data-ttu-id="253ac-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="253ac-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="253ac-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="253ac-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="253ac-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="253ac-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="253ac-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="253ac-108">DESCRIPTION</span></span>
<span data-ttu-id="253ac-109">Der ThroughpyteType-Parameterer definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="253ac-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="253ac-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="253ac-110">EXAMPLES</span></span>

### <span data-ttu-id="253ac-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="253ac-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="253ac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="253ac-112">PARAMETERS</span></span>

### <span data-ttu-id="253ac-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="253ac-113">-AccountName</span></span>
<span data-ttu-id="253ac-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="253ac-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="253ac-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="253ac-115">-Confirm</span></span>
<span data-ttu-id="253ac-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="253ac-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="253ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="253ac-117">-DefaultProfile</span></span>
<span data-ttu-id="253ac-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="253ac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="253ac-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="253ac-119">-InputObject</span></span>
<span data-ttu-id="253ac-120">Dieses Keyspaceobjekt.</span><span class="sxs-lookup"><span data-stu-id="253ac-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="253ac-121">-Name</span><span class="sxs-lookup"><span data-stu-id="253ac-121">-Name</span></span>
<span data-ttu-id="253ac-122">Der Name des Schlüsselraums.</span><span class="sxs-lookup"><span data-stu-id="253ac-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="253ac-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="253ac-123">-ParentObject</span></span>
<span data-ttu-id="253ac-124">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="253ac-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="253ac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="253ac-125">-ResourceGroupName</span></span>
<span data-ttu-id="253ac-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="253ac-126">Name of resource group.</span></span>

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

### <span data-ttu-id="253ac-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="253ac-127">-ThroughputType</span></span>
<span data-ttu-id="253ac-128">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="253ac-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="253ac-129">Mögliche Werte sind: Autoskalieren, Manuell.</span><span class="sxs-lookup"><span data-stu-id="253ac-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="253ac-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="253ac-130">-WhatIf</span></span>
<span data-ttu-id="253ac-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="253ac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="253ac-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="253ac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="253ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="253ac-133">CommonParameters</span></span>
<span data-ttu-id="253ac-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="253ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="253ac-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="253ac-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="253ac-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="253ac-136">INPUTS</span></span>

### <span data-ttu-id="253ac-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="253ac-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="253ac-138">Microsoft.Azure.Commands.UmsDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="253ac-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="253ac-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="253ac-139">OUTPUTS</span></span>

### <span data-ttu-id="253ac-140">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="253ac-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="253ac-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="253ac-141">NOTES</span></span>

## <span data-ttu-id="253ac-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="253ac-142">RELATED LINKS</span></span>
