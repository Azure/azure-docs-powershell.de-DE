---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299427"
---
# <span data-ttu-id="2848a-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="2848a-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="2848a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2848a-102">SYNOPSIS</span></span>
<span data-ttu-id="2848a-103">Verwenden Sie diese Vorgehensweise, um den AutoScale-Durchsatz auf manuellen Durchsatz zu migrieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="2848a-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="2848a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2848a-104">SYNTAX</span></span>

### <span data-ttu-id="2848a-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2848a-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2848a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2848a-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2848a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2848a-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2848a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2848a-108">DESCRIPTION</span></span>
<span data-ttu-id="2848a-109">ThroughpyteType Parameter definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="2848a-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="2848a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2848a-110">EXAMPLES</span></span>

### <span data-ttu-id="2848a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2848a-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="2848a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2848a-112">PARAMETERS</span></span>

### <span data-ttu-id="2848a-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="2848a-113">-AccountName</span></span>
<span data-ttu-id="2848a-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="2848a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2848a-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2848a-115">-Confirm</span></span>
<span data-ttu-id="2848a-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2848a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2848a-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2848a-117">-DatabaseName</span></span>
<span data-ttu-id="2848a-118">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="2848a-118">Database name.</span></span>

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

### <span data-ttu-id="2848a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2848a-119">-DefaultProfile</span></span>
<span data-ttu-id="2848a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2848a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2848a-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2848a-121">-InputObject</span></span>
<span data-ttu-id="2848a-122">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="2848a-122">Sql Container object.</span></span>

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

### <span data-ttu-id="2848a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2848a-123">-Name</span></span>
<span data-ttu-id="2848a-124">Container Name.</span><span class="sxs-lookup"><span data-stu-id="2848a-124">Container name.</span></span>

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

### <span data-ttu-id="2848a-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2848a-125">-ParentObject</span></span>
<span data-ttu-id="2848a-126">SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="2848a-126">Sql Database object.</span></span>

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

### <span data-ttu-id="2848a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2848a-127">-ResourceGroupName</span></span>
<span data-ttu-id="2848a-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2848a-128">Name of resource group.</span></span>

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

### <span data-ttu-id="2848a-129">-Durchsatztyp</span><span class="sxs-lookup"><span data-stu-id="2848a-129">-ThroughputType</span></span>
<span data-ttu-id="2848a-130">Der durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2848a-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="2848a-131">Mögliche Werte sind: AutoScale, manuell.</span><span class="sxs-lookup"><span data-stu-id="2848a-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="2848a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2848a-132">-WhatIf</span></span>
<span data-ttu-id="2848a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2848a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2848a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2848a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2848a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2848a-135">CommonParameters</span></span>
<span data-ttu-id="2848a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2848a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2848a-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2848a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2848a-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2848a-138">INPUTS</span></span>

### <span data-ttu-id="2848a-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2848a-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="2848a-140">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="2848a-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="2848a-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2848a-141">OUTPUTS</span></span>

### <span data-ttu-id="2848a-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2848a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2848a-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="2848a-143">NOTES</span></span>

## <span data-ttu-id="2848a-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2848a-144">RELATED LINKS</span></span>
