---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304803"
---
# <span data-ttu-id="c2800-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="c2800-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="c2800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2800-102">SYNOPSIS</span></span>
<span data-ttu-id="c2800-103">Löscht einen Keyspace aus Demkka.</span><span class="sxs-lookup"><span data-stu-id="c2800-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="c2800-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2800-104">SYNTAX</span></span>

### <span data-ttu-id="c2800-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2800-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2800-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2800-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2800-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2800-107">DESCRIPTION</span></span>
<span data-ttu-id="c2800-108">Das **Cmdlet "Remove-AzCosmosDBCasskeyspace"** löscht einen vorhandenen Kommentartastenspace.</span><span class="sxs-lookup"><span data-stu-id="c2800-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="c2800-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2800-109">EXAMPLES</span></span>

### <span data-ttu-id="c2800-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2800-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="c2800-111">Das Cmdlet gibt ein Objekt vom Typ boolesch (wenn -PassThru übergeben wird) zurück, das wahr ist, wenn das Löschen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c2800-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="c2800-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2800-112">PARAMETERS</span></span>

### <span data-ttu-id="c2800-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2800-113">-AccountName</span></span>
<span data-ttu-id="c2800-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="c2800-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c2800-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2800-115">-Confirm</span></span>
<span data-ttu-id="c2800-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2800-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2800-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2800-117">-DefaultProfile</span></span>
<span data-ttu-id="c2800-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2800-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2800-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2800-119">-InputObject</span></span>
<span data-ttu-id="c2800-120">Dieses Keyspaceobjekt.</span><span class="sxs-lookup"><span data-stu-id="c2800-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="c2800-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c2800-121">-Name</span></span>
<span data-ttu-id="c2800-122">Der Name des Schlüsselraums.</span><span class="sxs-lookup"><span data-stu-id="c2800-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c2800-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2800-123">-PassThru</span></span>
<span data-ttu-id="c2800-124">Wird auf "true" festgelegt, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="c2800-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="c2800-125">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war und andern falls nicht ein Fehler ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="c2800-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="c2800-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2800-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2800-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2800-127">Name of resource group.</span></span>

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

### <span data-ttu-id="c2800-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c2800-128">-WhatIf</span></span>
<span data-ttu-id="c2800-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2800-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2800-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2800-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2800-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2800-131">CommonParameters</span></span>
<span data-ttu-id="c2800-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2800-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2800-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2800-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2800-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2800-134">INPUTS</span></span>

### <span data-ttu-id="c2800-135">Microsoft.Azure.Commands.UmsDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c2800-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="c2800-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2800-136">OUTPUTS</span></span>

### <span data-ttu-id="c2800-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="c2800-137">System.Void</span></span>

### <span data-ttu-id="c2800-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c2800-138">System.Boolean</span></span>

## <span data-ttu-id="c2800-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c2800-139">NOTES</span></span>

## <span data-ttu-id="c2800-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c2800-140">RELATED LINKS</span></span>
