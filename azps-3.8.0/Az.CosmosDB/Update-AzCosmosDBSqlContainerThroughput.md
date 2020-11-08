---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: e38e10765bc9a9768efaf1598a1865ec985b376c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996887"
---
# <span data-ttu-id="906ad-101">Update-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="906ad-101">Update-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="906ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="906ad-102">SYNOPSIS</span></span>
<span data-ttu-id="906ad-103">Aktualisiert den Durchsatz eines CosmosDB SQL-Containers.</span><span class="sxs-lookup"><span data-stu-id="906ad-103">Updates the throughput value of a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="906ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="906ad-104">SYNTAX</span></span>

### <span data-ttu-id="906ad-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="906ad-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="906ad-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="906ad-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="906ad-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="906ad-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="906ad-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="906ad-108">EXAMPLES</span></span>

### <span data-ttu-id="906ad-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="906ad-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlContainerThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {myDatabaseName} -Name {myContainerName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/conatiners/{myContainerName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="906ad-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="906ad-110">PARAMETERS</span></span>

### <span data-ttu-id="906ad-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="906ad-111">-AccountName</span></span>
<span data-ttu-id="906ad-112">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="906ad-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="906ad-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="906ad-113">-Confirm</span></span>
<span data-ttu-id="906ad-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="906ad-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="906ad-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="906ad-115">-DatabaseName</span></span>
<span data-ttu-id="906ad-116">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="906ad-116">Database name.</span></span>

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

### <span data-ttu-id="906ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="906ad-117">-DefaultProfile</span></span>
<span data-ttu-id="906ad-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="906ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="906ad-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="906ad-119">-InputObject</span></span>
<span data-ttu-id="906ad-120">SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="906ad-120">Sql Database object.</span></span>

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

### <span data-ttu-id="906ad-121">-Name</span><span class="sxs-lookup"><span data-stu-id="906ad-121">-Name</span></span>
<span data-ttu-id="906ad-122">Container Name.</span><span class="sxs-lookup"><span data-stu-id="906ad-122">Container name.</span></span>

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

### <span data-ttu-id="906ad-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="906ad-123">-ParentObject</span></span>
<span data-ttu-id="906ad-124">SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="906ad-124">Sql Database object.</span></span>

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

### <span data-ttu-id="906ad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="906ad-125">-ResourceGroupName</span></span>
<span data-ttu-id="906ad-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="906ad-126">Name of resource group.</span></span>

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

### <span data-ttu-id="906ad-127">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="906ad-127">-Throughput</span></span>
<span data-ttu-id="906ad-128">Der Durchsatz des SQL-Containers (ru/s).</span><span class="sxs-lookup"><span data-stu-id="906ad-128">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="906ad-129">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="906ad-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906ad-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="906ad-130">-WhatIf</span></span>
<span data-ttu-id="906ad-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="906ad-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="906ad-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="906ad-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="906ad-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="906ad-133">CommonParameters</span></span>
<span data-ttu-id="906ad-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="906ad-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="906ad-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="906ad-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="906ad-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="906ad-136">INPUTS</span></span>

### <span data-ttu-id="906ad-137">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="906ad-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="906ad-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="906ad-138">OUTPUTS</span></span>

### <span data-ttu-id="906ad-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="906ad-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="906ad-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="906ad-140">NOTES</span></span>

## <span data-ttu-id="906ad-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="906ad-141">RELATED LINKS</span></span>
