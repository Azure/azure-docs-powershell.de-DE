---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004332"
---
# <span data-ttu-id="02ada-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="02ada-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="02ada-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02ada-102">SYNOPSIS</span></span>
<span data-ttu-id="02ada-103">Ruft den Durchsatz Wert der Cassandra-Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="02ada-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="02ada-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02ada-104">SYNTAX</span></span>

### <span data-ttu-id="02ada-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="02ada-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02ada-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02ada-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02ada-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02ada-107">DESCRIPTION</span></span>
<span data-ttu-id="02ada-108">Das Cmdlet " **Get-AzCosmosDBCassandraTableThroughput** " Ruft das Durchsatz Objekt ab, das einem angegebenen Keyspace entspricht.</span><span class="sxs-lookup"><span data-stu-id="02ada-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="02ada-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02ada-109">EXAMPLES</span></span>

### <span data-ttu-id="02ada-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="02ada-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="02ada-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="02ada-111">PARAMETERS</span></span>

### <span data-ttu-id="02ada-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="02ada-112">-AccountName</span></span>
<span data-ttu-id="02ada-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="02ada-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="02ada-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="02ada-114">-Confirm</span></span>
<span data-ttu-id="02ada-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02ada-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02ada-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ada-116">-DefaultProfile</span></span>
<span data-ttu-id="02ada-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02ada-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02ada-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="02ada-118">-InputObject</span></span>
<span data-ttu-id="02ada-119">Cassandra-Tabellenobjekt.</span><span class="sxs-lookup"><span data-stu-id="02ada-119">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02ada-120">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="02ada-120">-KeyspaceName</span></span>
<span data-ttu-id="02ada-121">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="02ada-121">Database name.</span></span>

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

### <span data-ttu-id="02ada-122">-Name</span><span class="sxs-lookup"><span data-stu-id="02ada-122">-Name</span></span>
<span data-ttu-id="02ada-123">Cassandra-Tabellen Name.</span><span class="sxs-lookup"><span data-stu-id="02ada-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="02ada-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ada-124">-ResourceGroupName</span></span>
<span data-ttu-id="02ada-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="02ada-125">Name of resource group.</span></span>

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

### <span data-ttu-id="02ada-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02ada-126">-WhatIf</span></span>
<span data-ttu-id="02ada-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02ada-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02ada-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02ada-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02ada-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ada-129">CommonParameters</span></span>
<span data-ttu-id="02ada-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02ada-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ada-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02ada-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ada-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02ada-132">INPUTS</span></span>

### <span data-ttu-id="02ada-133">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="02ada-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="02ada-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02ada-134">OUTPUTS</span></span>

### <span data-ttu-id="02ada-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="02ada-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="02ada-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="02ada-136">NOTES</span></span>

## <span data-ttu-id="02ada-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02ada-137">RELATED LINKS</span></span>
