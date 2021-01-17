---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470769"
---
# <span data-ttu-id="feb3e-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="feb3e-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="feb3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feb3e-102">SYNOPSIS</span></span>
<span data-ttu-id="feb3e-103">Ruft den Durchsatzwert der Tabelle "Untere Tabelle" ab.</span><span class="sxs-lookup"><span data-stu-id="feb3e-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="feb3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="feb3e-104">SYNTAX</span></span>

### <span data-ttu-id="feb3e-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="feb3e-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb3e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="feb3e-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feb3e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="feb3e-107">DESCRIPTION</span></span>
<span data-ttu-id="feb3e-108">Das **Cmdlet "Get-AzCosmosDBCassrateThroughput"** ruft das Durchsatzobjekt ab, das einem bestimmten Keyspace entspricht.</span><span class="sxs-lookup"><span data-stu-id="feb3e-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="feb3e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="feb3e-109">EXAMPLES</span></span>

### <span data-ttu-id="feb3e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="feb3e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="feb3e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="feb3e-111">PARAMETERS</span></span>

### <span data-ttu-id="feb3e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="feb3e-112">-AccountName</span></span>
<span data-ttu-id="feb3e-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="feb3e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="feb3e-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="feb3e-114">-Confirm</span></span>
<span data-ttu-id="feb3e-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="feb3e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feb3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb3e-116">-DefaultProfile</span></span>
<span data-ttu-id="feb3e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="feb3e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feb3e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="feb3e-118">-InputObject</span></span>
<span data-ttu-id="feb3e-119">Das Objekt "Tabelle" aus Untere Tabelle.</span><span class="sxs-lookup"><span data-stu-id="feb3e-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="feb3e-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="feb3e-120">-KeyspaceName</span></span>
<span data-ttu-id="feb3e-121">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="feb3e-121">Database name.</span></span>

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

### <span data-ttu-id="feb3e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="feb3e-122">-Name</span></span>
<span data-ttu-id="feb3e-123">DestgensEr Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="feb3e-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="feb3e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feb3e-124">-ResourceGroupName</span></span>
<span data-ttu-id="feb3e-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="feb3e-125">Name of resource group.</span></span>

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

### <span data-ttu-id="feb3e-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="feb3e-126">-WhatIf</span></span>
<span data-ttu-id="feb3e-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="feb3e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feb3e-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="feb3e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feb3e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb3e-129">CommonParameters</span></span>
<span data-ttu-id="feb3e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feb3e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb3e-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="feb3e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb3e-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="feb3e-132">INPUTS</span></span>

### <span data-ttu-id="feb3e-133">Microsoft.Azure.Commands.UmsDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="feb3e-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="feb3e-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="feb3e-134">OUTPUTS</span></span>

### <span data-ttu-id="feb3e-135">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="feb3e-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="feb3e-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="feb3e-136">NOTES</span></span>

## <span data-ttu-id="feb3e-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="feb3e-137">RELATED LINKS</span></span>
