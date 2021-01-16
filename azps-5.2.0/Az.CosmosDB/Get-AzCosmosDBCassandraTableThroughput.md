---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298579"
---
# <span data-ttu-id="1b2ed-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="1b2ed-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="1b2ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b2ed-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2ed-103">Ruft den Durchsatzwert der Tabelle "Untere Tabelle" ab.</span><span class="sxs-lookup"><span data-stu-id="1b2ed-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="1b2ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b2ed-104">SYNTAX</span></span>

### <span data-ttu-id="1b2ed-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b2ed-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b2ed-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b2ed-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b2ed-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b2ed-107">DESCRIPTION</span></span>
<span data-ttu-id="1b2ed-108">Das **Cmdlet "Get-AzCosmosDBCassrateThroughput"** ruft das Durchsatzobjekt ab, das einem bestimmten Keyspace entspricht.</span><span class="sxs-lookup"><span data-stu-id="1b2ed-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="1b2ed-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b2ed-109">EXAMPLES</span></span>

### <span data-ttu-id="1b2ed-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1b2ed-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="1b2ed-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b2ed-111">PARAMETERS</span></span>

### <span data-ttu-id="1b2ed-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b2ed-112">-AccountName</span></span>
<span data-ttu-id="1b2ed-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="1b2ed-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1b2ed-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b2ed-114">-Confirm</span></span>
<span data-ttu-id="1b2ed-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b2ed-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b2ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2ed-116">-DefaultProfile</span></span>
<span data-ttu-id="1b2ed-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b2ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b2ed-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b2ed-118">-InputObject</span></span>
<span data-ttu-id="1b2ed-119">Das Tabellenobjekt "Untere Tabelle".</span><span class="sxs-lookup"><span data-stu-id="1b2ed-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="1b2ed-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="1b2ed-120">-KeyspaceName</span></span>
<span data-ttu-id="1b2ed-121">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="1b2ed-121">Database name.</span></span>

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

### <span data-ttu-id="1b2ed-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1b2ed-122">-Name</span></span>
<span data-ttu-id="1b2ed-123">DestgensEr Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="1b2ed-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="1b2ed-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b2ed-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b2ed-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1b2ed-125">Name of resource group.</span></span>

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

### <span data-ttu-id="1b2ed-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1b2ed-126">-WhatIf</span></span>
<span data-ttu-id="1b2ed-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b2ed-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b2ed-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b2ed-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b2ed-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2ed-129">CommonParameters</span></span>
<span data-ttu-id="1b2ed-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b2ed-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2ed-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b2ed-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2ed-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b2ed-132">INPUTS</span></span>

### <span data-ttu-id="1b2ed-133">Microsoft.Azure.Commands.UmsDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="1b2ed-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="1b2ed-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b2ed-134">OUTPUTS</span></span>

### <span data-ttu-id="1b2ed-135">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1b2ed-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1b2ed-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1b2ed-136">NOTES</span></span>

## <span data-ttu-id="1b2ed-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1b2ed-137">RELATED LINKS</span></span>
