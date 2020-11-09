---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 2953da3747404c0b6b98992cc8a8b80573da5129
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299259"
---
# <span data-ttu-id="af298-101">New-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="af298-101">New-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="af298-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af298-102">SYNOPSIS</span></span>
<span data-ttu-id="af298-103">Erstellt eine neue CosmosDB SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="af298-103">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="af298-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af298-104">SYNTAX</span></span>

### <span data-ttu-id="af298-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="af298-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af298-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af298-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af298-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af298-107">DESCRIPTION</span></span>
<span data-ttu-id="af298-108">Erstellt eine neue CosmosDB SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="af298-108">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="af298-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af298-109">EXAMPLES</span></span>

### <span data-ttu-id="af298-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="af298-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="af298-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="af298-111">PARAMETERS</span></span>

### <span data-ttu-id="af298-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="af298-112">-AccountName</span></span>
<span data-ttu-id="af298-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="af298-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="af298-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="af298-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="af298-115">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="af298-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="af298-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="af298-116">-Confirm</span></span>
<span data-ttu-id="af298-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="af298-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af298-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af298-118">-DefaultProfile</span></span>
<span data-ttu-id="af298-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="af298-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af298-120">-Name</span><span class="sxs-lookup"><span data-stu-id="af298-120">-Name</span></span>
<span data-ttu-id="af298-121">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="af298-121">Database name.</span></span>

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

### <span data-ttu-id="af298-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="af298-122">-ParentObject</span></span>
<span data-ttu-id="af298-123">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="af298-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="af298-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af298-124">-ResourceGroupName</span></span>
<span data-ttu-id="af298-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="af298-125">Name of resource group.</span></span>

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

### <span data-ttu-id="af298-126">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="af298-126">-Throughput</span></span>
<span data-ttu-id="af298-127">Der Durchsatz der SQL-Datenbank (ru/s).</span><span class="sxs-lookup"><span data-stu-id="af298-127">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="af298-128">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="af298-128">Default value is 400.</span></span>

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

### <span data-ttu-id="af298-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af298-129">-WhatIf</span></span>
<span data-ttu-id="af298-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af298-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af298-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af298-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af298-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af298-132">CommonParameters</span></span>
<span data-ttu-id="af298-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af298-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af298-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af298-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af298-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af298-135">INPUTS</span></span>

### <span data-ttu-id="af298-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="af298-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="af298-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af298-137">OUTPUTS</span></span>

### <span data-ttu-id="af298-138">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="af298-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="af298-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="af298-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="af298-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="af298-140">NOTES</span></span>

## <span data-ttu-id="af298-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af298-141">RELATED LINKS</span></span>
