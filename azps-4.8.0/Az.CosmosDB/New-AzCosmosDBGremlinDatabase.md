---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 535d6aa9f2ea6538e6b00f1334ce1114fad89f81
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167080"
---
# <span data-ttu-id="e5f26-101">New-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="e5f26-101">New-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="e5f26-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5f26-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f26-103">Erstellt eine neue CosmosDB-Gremlin-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e5f26-103">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e5f26-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5f26-104">SYNTAX</span></span>

### <span data-ttu-id="e5f26-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5f26-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f26-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f26-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5f26-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5f26-107">DESCRIPTION</span></span>
<span data-ttu-id="e5f26-108">Erstellt eine neue CosmosDB-Gremlin-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e5f26-108">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e5f26-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5f26-109">EXAMPLES</span></span>

### <span data-ttu-id="e5f26-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5f26-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="e5f26-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5f26-111">PARAMETERS</span></span>

### <span data-ttu-id="e5f26-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="e5f26-112">-AccountName</span></span>
<span data-ttu-id="e5f26-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="e5f26-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e5f26-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e5f26-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e5f26-115">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e5f26-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e5f26-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5f26-116">-Confirm</span></span>
<span data-ttu-id="e5f26-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5f26-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5f26-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f26-118">-DefaultProfile</span></span>
<span data-ttu-id="e5f26-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5f26-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5f26-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e5f26-120">-Name</span></span>
<span data-ttu-id="e5f26-121">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="e5f26-121">Database name.</span></span>

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

### <span data-ttu-id="e5f26-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e5f26-122">-ParentObject</span></span>
<span data-ttu-id="e5f26-123">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="e5f26-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e5f26-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5f26-124">-ResourceGroupName</span></span>
<span data-ttu-id="e5f26-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f26-125">Name of resource group.</span></span>

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

### <span data-ttu-id="e5f26-126">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="e5f26-126">-Throughput</span></span>
<span data-ttu-id="e5f26-127">Der Durchsatz der Gremlin-Datenbank (ru/s).</span><span class="sxs-lookup"><span data-stu-id="e5f26-127">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="e5f26-128">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="e5f26-128">Default value is 400.</span></span>

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

### <span data-ttu-id="e5f26-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f26-129">-WhatIf</span></span>
<span data-ttu-id="e5f26-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5f26-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5f26-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5f26-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5f26-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f26-132">CommonParameters</span></span>
<span data-ttu-id="e5f26-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5f26-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f26-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5f26-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f26-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5f26-135">INPUTS</span></span>

### <span data-ttu-id="e5f26-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e5f26-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e5f26-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5f26-137">OUTPUTS</span></span>

### <span data-ttu-id="e5f26-138">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e5f26-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="e5f26-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="e5f26-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="e5f26-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5f26-140">NOTES</span></span>

## <span data-ttu-id="e5f26-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5f26-141">RELATED LINKS</span></span>
