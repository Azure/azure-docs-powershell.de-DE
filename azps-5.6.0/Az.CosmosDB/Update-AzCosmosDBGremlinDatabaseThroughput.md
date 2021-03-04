---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 21dd30bd60e9b26fc306ed99b31cd3c52d9fdf8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931288"
---
# <span data-ttu-id="e0715-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="e0715-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="e0715-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0715-102">SYNOPSIS</span></span>
<span data-ttu-id="e0715-103">Aktualisiert den Durchsatzwert einer CosmosDB-Gremlin-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e0715-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e0715-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0715-104">SYNTAX</span></span>

### <span data-ttu-id="e0715-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e0715-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0715-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0715-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0715-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0715-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0715-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0715-108">DESCRIPTION</span></span>
<span data-ttu-id="e0715-109">Aktualisiert den Durchsatzwert einer CosmosDB-Gremlin-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e0715-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e0715-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0715-110">EXAMPLES</span></span>

### <span data-ttu-id="e0715-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e0715-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="e0715-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e0715-112">PARAMETERS</span></span>

### <span data-ttu-id="e0715-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e0715-113">-AccountName</span></span>
<span data-ttu-id="e0715-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="e0715-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e0715-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e0715-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e0715-116">Maximaler Durchsatzwert, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e0715-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e0715-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e0715-117">-Confirm</span></span>
<span data-ttu-id="e0715-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0715-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0715-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0715-119">-DefaultProfile</span></span>
<span data-ttu-id="e0715-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0715-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0715-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0715-121">-InputObject</span></span>
<span data-ttu-id="e0715-122">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="e0715-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e0715-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e0715-123">-Name</span></span>
<span data-ttu-id="e0715-124">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="e0715-124">Database name.</span></span>

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

### <span data-ttu-id="e0715-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e0715-125">-ParentObject</span></span>
<span data-ttu-id="e0715-126">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="e0715-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e0715-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0715-127">-ResourceGroupName</span></span>
<span data-ttu-id="e0715-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e0715-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e0715-129">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="e0715-129">-Throughput</span></span>
<span data-ttu-id="e0715-130">Der Durchsatz der Gremlin-Datenbank (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e0715-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="e0715-131">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="e0715-131">Default value is 400.</span></span>

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

### <span data-ttu-id="e0715-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0715-132">-WhatIf</span></span>
<span data-ttu-id="e0715-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0715-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0715-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0715-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0715-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0715-135">CommonParameters</span></span>
<span data-ttu-id="e0715-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0715-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0715-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0715-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0715-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0715-138">INPUTS</span></span>

### <span data-ttu-id="e0715-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e0715-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e0715-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0715-140">OUTPUTS</span></span>

### <span data-ttu-id="e0715-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e0715-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e0715-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e0715-142">NOTES</span></span>

## <span data-ttu-id="e0715-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e0715-143">RELATED LINKS</span></span>
