---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166276"
---
# <span data-ttu-id="74b24-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="74b24-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="74b24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74b24-102">SYNOPSIS</span></span>
<span data-ttu-id="74b24-103">Ruft den Durchsatzwert der Tabelle "Untere Tabelle" ab.</span><span class="sxs-lookup"><span data-stu-id="74b24-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="74b24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74b24-104">SYNTAX</span></span>

### <span data-ttu-id="74b24-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="74b24-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74b24-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74b24-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74b24-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74b24-107">DESCRIPTION</span></span>
<span data-ttu-id="74b24-108">Das **Cmdlet "Get-AzCosmosDBCassrateThroughput"** ruft das Durchsatzobjekt ab, das einem bestimmten Keyspace entspricht.</span><span class="sxs-lookup"><span data-stu-id="74b24-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="74b24-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74b24-109">EXAMPLES</span></span>

### <span data-ttu-id="74b24-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74b24-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="74b24-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74b24-111">PARAMETERS</span></span>

### <span data-ttu-id="74b24-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="74b24-112">-AccountName</span></span>
<span data-ttu-id="74b24-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="74b24-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="74b24-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74b24-114">-Confirm</span></span>
<span data-ttu-id="74b24-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74b24-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74b24-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b24-116">-DefaultProfile</span></span>
<span data-ttu-id="74b24-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74b24-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74b24-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74b24-118">-InputObject</span></span>
<span data-ttu-id="74b24-119">Das Objekt "Tabelle" aus Untere Tabelle.</span><span class="sxs-lookup"><span data-stu-id="74b24-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="74b24-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="74b24-120">-KeyspaceName</span></span>
<span data-ttu-id="74b24-121">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="74b24-121">Database name.</span></span>

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

### <span data-ttu-id="74b24-122">-Name</span><span class="sxs-lookup"><span data-stu-id="74b24-122">-Name</span></span>
<span data-ttu-id="74b24-123">DestgensEr Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="74b24-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="74b24-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b24-124">-ResourceGroupName</span></span>
<span data-ttu-id="74b24-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="74b24-125">Name of resource group.</span></span>

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

### <span data-ttu-id="74b24-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="74b24-126">-WhatIf</span></span>
<span data-ttu-id="74b24-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74b24-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74b24-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74b24-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74b24-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b24-129">CommonParameters</span></span>
<span data-ttu-id="74b24-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74b24-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b24-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74b24-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b24-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74b24-132">INPUTS</span></span>

### <span data-ttu-id="74b24-133">Microsoft.Azure.Commands.ExesDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="74b24-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="74b24-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74b24-134">OUTPUTS</span></span>

### <span data-ttu-id="74b24-135">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="74b24-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="74b24-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="74b24-136">NOTES</span></span>

## <span data-ttu-id="74b24-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="74b24-137">RELATED LINKS</span></span>
