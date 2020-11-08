---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 43426c97e809bf576dd6df19af108fb54c6874a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174815"
---
# <span data-ttu-id="d7b8e-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="d7b8e-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="d7b8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b8e-103">Aktualisiert den Durchsatz einer CosmosDB-Gremlin-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="d7b8e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7b8e-104">SYNTAX</span></span>

### <span data-ttu-id="d7b8e-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7b8e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7b8e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7b8e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7b8e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7b8e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7b8e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7b8e-108">DESCRIPTION</span></span>
<span data-ttu-id="d7b8e-109">Aktualisiert den Durchsatz einer CosmosDB-Gremlin-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="d7b8e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7b8e-110">EXAMPLES</span></span>

### <span data-ttu-id="d7b8e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d7b8e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="d7b8e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7b8e-112">PARAMETERS</span></span>

### <span data-ttu-id="d7b8e-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="d7b8e-113">-AccountName</span></span>
<span data-ttu-id="d7b8e-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d7b8e-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d7b8e-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d7b8e-116">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d7b8e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7b8e-117">-Confirm</span></span>
<span data-ttu-id="d7b8e-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7b8e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b8e-119">-DefaultProfile</span></span>
<span data-ttu-id="d7b8e-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7b8e-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d7b8e-121">-InputObject</span></span>
<span data-ttu-id="d7b8e-122">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="d7b8e-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d7b8e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d7b8e-123">-Name</span></span>
<span data-ttu-id="d7b8e-124">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="d7b8e-124">Database name.</span></span>

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

### <span data-ttu-id="d7b8e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d7b8e-125">-ParentObject</span></span>
<span data-ttu-id="d7b8e-126">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="d7b8e-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d7b8e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b8e-127">-ResourceGroupName</span></span>
<span data-ttu-id="d7b8e-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-128">Name of resource group.</span></span>

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

### <span data-ttu-id="d7b8e-129">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="d7b8e-129">-Throughput</span></span>
<span data-ttu-id="d7b8e-130">Der Durchsatz der Gremlin-Datenbank (ru/s).</span><span class="sxs-lookup"><span data-stu-id="d7b8e-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="d7b8e-131">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-131">Default value is 400.</span></span>

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

### <span data-ttu-id="d7b8e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b8e-132">-WhatIf</span></span>
<span data-ttu-id="d7b8e-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7b8e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7b8e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b8e-135">CommonParameters</span></span>
<span data-ttu-id="d7b8e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b8e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b8e-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7b8e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b8e-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7b8e-138">INPUTS</span></span>

### <span data-ttu-id="d7b8e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d7b8e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d7b8e-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7b8e-140">OUTPUTS</span></span>

### <span data-ttu-id="d7b8e-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d7b8e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d7b8e-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7b8e-142">NOTES</span></span>

## <span data-ttu-id="d7b8e-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7b8e-143">RELATED LINKS</span></span>
