---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173058"
---
# <span data-ttu-id="64a4a-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="64a4a-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="64a4a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="64a4a-103">Aktualisiert die CosmosDB SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="64a4a-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="64a4a-104">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="64a4a-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="64a4a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64a4a-105">SYNTAX</span></span>

### <span data-ttu-id="64a4a-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="64a4a-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64a4a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64a4a-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64a4a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64a4a-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64a4a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64a4a-109">DESCRIPTION</span></span>
<span data-ttu-id="64a4a-110">Aktualisiert die CosmosDB SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="64a4a-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="64a4a-111">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="64a4a-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="64a4a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64a4a-112">EXAMPLES</span></span>

### <span data-ttu-id="64a4a-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64a4a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="64a4a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="64a4a-114">PARAMETERS</span></span>

### <span data-ttu-id="64a4a-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="64a4a-115">-AccountName</span></span>
<span data-ttu-id="64a4a-116">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="64a4a-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="64a4a-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="64a4a-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="64a4a-118">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="64a4a-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="64a4a-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="64a4a-119">-Confirm</span></span>
<span data-ttu-id="64a4a-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64a4a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64a4a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a4a-121">-DefaultProfile</span></span>
<span data-ttu-id="64a4a-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64a4a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a4a-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="64a4a-123">-InputObject</span></span>
<span data-ttu-id="64a4a-124">SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="64a4a-124">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64a4a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="64a4a-125">-Name</span></span>
<span data-ttu-id="64a4a-126">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="64a4a-126">Database name.</span></span>

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

### <span data-ttu-id="64a4a-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="64a4a-127">-ParentObject</span></span>
<span data-ttu-id="64a4a-128">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="64a4a-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="64a4a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a4a-129">-ResourceGroupName</span></span>
<span data-ttu-id="64a4a-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="64a4a-130">Name of resource group.</span></span>

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

### <span data-ttu-id="64a4a-131">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="64a4a-131">-Throughput</span></span>
<span data-ttu-id="64a4a-132">Der Durchsatz der SQL-Datenbank (ru/s).</span><span class="sxs-lookup"><span data-stu-id="64a4a-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="64a4a-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="64a4a-133">Default value is 400.</span></span>

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

### <span data-ttu-id="64a4a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64a4a-134">-WhatIf</span></span>
<span data-ttu-id="64a4a-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64a4a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64a4a-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64a4a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64a4a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a4a-137">CommonParameters</span></span>
<span data-ttu-id="64a4a-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a4a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a4a-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64a4a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a4a-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64a4a-140">INPUTS</span></span>

### <span data-ttu-id="64a4a-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="64a4a-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="64a4a-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="64a4a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="64a4a-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64a4a-143">OUTPUTS</span></span>

### <span data-ttu-id="64a4a-144">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="64a4a-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="64a4a-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="64a4a-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="64a4a-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="64a4a-146">NOTES</span></span>

## <span data-ttu-id="64a4a-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64a4a-147">RELATED LINKS</span></span>
