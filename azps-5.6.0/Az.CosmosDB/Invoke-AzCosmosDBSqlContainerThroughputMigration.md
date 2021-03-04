---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: c502040c2d4b11302c158cffb66bf6fd01e148ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941936"
---
# <span data-ttu-id="79e0e-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="79e0e-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="79e0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="79e0e-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skalierung in den manuellen Durchsatz zu migrieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="79e0e-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="79e0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79e0e-104">SYNTAX</span></span>

### <span data-ttu-id="79e0e-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="79e0e-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79e0e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79e0e-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79e0e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79e0e-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79e0e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79e0e-108">DESCRIPTION</span></span>
<span data-ttu-id="79e0e-109">ThroughpyteType-Paramter definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="79e0e-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="79e0e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79e0e-110">EXAMPLES</span></span>

### <span data-ttu-id="79e0e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79e0e-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```

## <span data-ttu-id="79e0e-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="79e0e-112">PARAMETERS</span></span>

### <span data-ttu-id="79e0e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79e0e-113">-AccountName</span></span>
<span data-ttu-id="79e0e-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="79e0e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="79e0e-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79e0e-115">-Confirm</span></span>
<span data-ttu-id="79e0e-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79e0e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79e0e-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79e0e-117">-DatabaseName</span></span>
<span data-ttu-id="79e0e-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="79e0e-118">Database name.</span></span>

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

### <span data-ttu-id="79e0e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e0e-119">-DefaultProfile</span></span>
<span data-ttu-id="79e0e-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79e0e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79e0e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79e0e-121">-InputObject</span></span>
<span data-ttu-id="79e0e-122">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="79e0e-122">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79e0e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="79e0e-123">-Name</span></span>
<span data-ttu-id="79e0e-124">Containername.</span><span class="sxs-lookup"><span data-stu-id="79e0e-124">Container name.</span></span>

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

### <span data-ttu-id="79e0e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="79e0e-125">-ParentObject</span></span>
<span data-ttu-id="79e0e-126">Sql Database-Objekt.</span><span class="sxs-lookup"><span data-stu-id="79e0e-126">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79e0e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79e0e-127">-ResourceGroupName</span></span>
<span data-ttu-id="79e0e-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="79e0e-128">Name of resource group.</span></span>

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

### <span data-ttu-id="79e0e-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="79e0e-129">-ThroughputType</span></span>
<span data-ttu-id="79e0e-130">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="79e0e-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="79e0e-131">Mögliche Werte sind: Automatische Skalierung, Manuell.</span><span class="sxs-lookup"><span data-stu-id="79e0e-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="79e0e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79e0e-132">-WhatIf</span></span>
<span data-ttu-id="79e0e-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79e0e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79e0e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79e0e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79e0e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e0e-135">CommonParameters</span></span>
<span data-ttu-id="79e0e-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79e0e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e0e-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79e0e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e0e-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79e0e-138">INPUTS</span></span>

### <span data-ttu-id="79e0e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="79e0e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="79e0e-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="79e0e-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="79e0e-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79e0e-141">OUTPUTS</span></span>

### <span data-ttu-id="79e0e-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="79e0e-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="79e0e-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="79e0e-143">NOTES</span></span>

## <span data-ttu-id="79e0e-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="79e0e-144">RELATED LINKS</span></span>
