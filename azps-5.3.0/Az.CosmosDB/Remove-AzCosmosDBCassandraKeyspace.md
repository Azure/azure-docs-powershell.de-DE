---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470704"
---
# <span data-ttu-id="95ecb-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="95ecb-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="95ecb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="95ecb-103">Löscht einen Keyspace aus Demkka.</span><span class="sxs-lookup"><span data-stu-id="95ecb-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="95ecb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95ecb-104">SYNTAX</span></span>

### <span data-ttu-id="95ecb-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="95ecb-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95ecb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95ecb-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95ecb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95ecb-107">DESCRIPTION</span></span>
<span data-ttu-id="95ecb-108">Das **Cmdlet "Remove-AzCosmosDBCasskeyspace"** löscht einen vorhandenen Kommentartastenspace.</span><span class="sxs-lookup"><span data-stu-id="95ecb-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="95ecb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95ecb-109">EXAMPLES</span></span>

### <span data-ttu-id="95ecb-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95ecb-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="95ecb-111">Das Cmdlet gibt ein Objekt vom Typ boolesch (wenn -PassThru übergeben wird) zurück, das wahr ist, wenn das Löschen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="95ecb-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="95ecb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95ecb-112">PARAMETERS</span></span>

### <span data-ttu-id="95ecb-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="95ecb-113">-AccountName</span></span>
<span data-ttu-id="95ecb-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="95ecb-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="95ecb-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95ecb-115">-Confirm</span></span>
<span data-ttu-id="95ecb-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95ecb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95ecb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ecb-117">-DefaultProfile</span></span>
<span data-ttu-id="95ecb-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95ecb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95ecb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95ecb-119">-InputObject</span></span>
<span data-ttu-id="95ecb-120">Dieses Keyspaceobjekt.</span><span class="sxs-lookup"><span data-stu-id="95ecb-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95ecb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="95ecb-121">-Name</span></span>
<span data-ttu-id="95ecb-122">Der Name des Schlüsselraums.</span><span class="sxs-lookup"><span data-stu-id="95ecb-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="95ecb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95ecb-123">-PassThru</span></span>
<span data-ttu-id="95ecb-124">Soll auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="95ecb-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="95ecb-125">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war und andern falls nicht ein Fehler ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="95ecb-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ecb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ecb-126">-ResourceGroupName</span></span>
<span data-ttu-id="95ecb-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="95ecb-127">Name of resource group.</span></span>

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

### <span data-ttu-id="95ecb-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="95ecb-128">-WhatIf</span></span>
<span data-ttu-id="95ecb-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95ecb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95ecb-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95ecb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95ecb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ecb-131">CommonParameters</span></span>
<span data-ttu-id="95ecb-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95ecb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ecb-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95ecb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ecb-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95ecb-134">INPUTS</span></span>

### <span data-ttu-id="95ecb-135">Microsoft.Azure.Commands.UmsDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="95ecb-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="95ecb-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95ecb-136">OUTPUTS</span></span>

### <span data-ttu-id="95ecb-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="95ecb-137">System.Void</span></span>

### <span data-ttu-id="95ecb-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="95ecb-138">System.Boolean</span></span>

## <span data-ttu-id="95ecb-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="95ecb-139">NOTES</span></span>

## <span data-ttu-id="95ecb-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="95ecb-140">RELATED LINKS</span></span>
