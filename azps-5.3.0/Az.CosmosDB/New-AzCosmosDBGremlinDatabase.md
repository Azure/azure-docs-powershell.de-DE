---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 535d6aa9f2ea6538e6b00f1334ce1114fad89f81
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470732"
---
# <span data-ttu-id="82d5a-101">New-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="82d5a-101">New-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="82d5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="82d5a-103">Erstellt eine neue Datenbank für Unterndb-Gremlin.</span><span class="sxs-lookup"><span data-stu-id="82d5a-103">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="82d5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82d5a-104">SYNTAX</span></span>

### <span data-ttu-id="82d5a-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="82d5a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82d5a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82d5a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82d5a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82d5a-107">DESCRIPTION</span></span>
<span data-ttu-id="82d5a-108">Erstellt eine neue Datenbank für Unterndb-Gremlin.</span><span class="sxs-lookup"><span data-stu-id="82d5a-108">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="82d5a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82d5a-109">EXAMPLES</span></span>

### <span data-ttu-id="82d5a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="82d5a-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="82d5a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82d5a-111">PARAMETERS</span></span>

### <span data-ttu-id="82d5a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="82d5a-112">-AccountName</span></span>
<span data-ttu-id="82d5a-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="82d5a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="82d5a-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="82d5a-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="82d5a-115">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="82d5a-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="82d5a-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82d5a-116">-Confirm</span></span>
<span data-ttu-id="82d5a-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82d5a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82d5a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82d5a-118">-DefaultProfile</span></span>
<span data-ttu-id="82d5a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82d5a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82d5a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="82d5a-120">-Name</span></span>
<span data-ttu-id="82d5a-121">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="82d5a-121">Database name.</span></span>

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

### <span data-ttu-id="82d5a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="82d5a-122">-ParentObject</span></span>
<span data-ttu-id="82d5a-123">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="82d5a-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="82d5a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82d5a-124">-ResourceGroupName</span></span>
<span data-ttu-id="82d5a-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="82d5a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="82d5a-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="82d5a-126">-Throughput</span></span>
<span data-ttu-id="82d5a-127">Der Durchsatz von Gremlin Database (RU/s).</span><span class="sxs-lookup"><span data-stu-id="82d5a-127">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="82d5a-128">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="82d5a-128">Default value is 400.</span></span>

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

### <span data-ttu-id="82d5a-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="82d5a-129">-WhatIf</span></span>
<span data-ttu-id="82d5a-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82d5a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82d5a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82d5a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82d5a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d5a-132">CommonParameters</span></span>
<span data-ttu-id="82d5a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82d5a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82d5a-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82d5a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d5a-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82d5a-135">INPUTS</span></span>

### <span data-ttu-id="82d5a-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="82d5a-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="82d5a-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82d5a-137">OUTPUTS</span></span>

### <span data-ttu-id="82d5a-138">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="82d5a-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="82d5a-139">Microsoft.Azure.Commands.DiesDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="82d5a-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="82d5a-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="82d5a-140">NOTES</span></span>

## <span data-ttu-id="82d5a-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="82d5a-141">RELATED LINKS</span></span>
