---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166177"
---
# <span data-ttu-id="c2d24-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="c2d24-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="c2d24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2d24-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d24-103">Löscht eine Tabelle vom 1.</span><span class="sxs-lookup"><span data-stu-id="c2d24-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="c2d24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2d24-104">SYNTAX</span></span>

### <span data-ttu-id="c2d24-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2d24-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2d24-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2d24-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2d24-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2d24-107">DESCRIPTION</span></span>
<span data-ttu-id="c2d24-108">Die **Remove-AzCosmosDBCasstable** löscht eine Tabelle vom Namen "Abt.</span><span class="sxs-lookup"><span data-stu-id="c2d24-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="c2d24-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2d24-109">EXAMPLES</span></span>

### <span data-ttu-id="c2d24-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2d24-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="c2d24-111">Das Cmdlet gibt ein Objekt vom Typ boolesch (wenn -PassThru übergeben wird) zurück, das "true" ist, wenn das Löschen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c2d24-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="c2d24-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2d24-112">PARAMETERS</span></span>

### <span data-ttu-id="c2d24-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2d24-113">-AccountName</span></span>
<span data-ttu-id="c2d24-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="c2d24-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c2d24-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2d24-115">-Confirm</span></span>
<span data-ttu-id="c2d24-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2d24-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2d24-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2d24-117">-DefaultProfile</span></span>
<span data-ttu-id="c2d24-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2d24-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2d24-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2d24-119">-InputObject</span></span>
<span data-ttu-id="c2d24-120">Das Objekt "Tabelle" aus Untere Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c2d24-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2d24-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="c2d24-121">-KeyspaceName</span></span>
<span data-ttu-id="c2d24-122">Name des Tastaturschlüssels.</span><span class="sxs-lookup"><span data-stu-id="c2d24-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c2d24-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c2d24-123">-Name</span></span>
<span data-ttu-id="c2d24-124">DestgensEr Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="c2d24-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="c2d24-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2d24-125">-PassThru</span></span>
<span data-ttu-id="c2d24-126">Soll auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="c2d24-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="c2d24-127">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war, und andern falls nicht, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="c2d24-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="c2d24-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2d24-128">-ResourceGroupName</span></span>
<span data-ttu-id="c2d24-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2d24-129">Name of resource group.</span></span>

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

### <span data-ttu-id="c2d24-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c2d24-130">-WhatIf</span></span>
<span data-ttu-id="c2d24-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2d24-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2d24-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2d24-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2d24-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d24-133">CommonParameters</span></span>
<span data-ttu-id="c2d24-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2d24-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d24-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2d24-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d24-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2d24-136">INPUTS</span></span>

### <span data-ttu-id="c2d24-137">Microsoft.Azure.Commands.CassDB.Models.PSCassistenTableGetResults</span><span class="sxs-lookup"><span data-stu-id="c2d24-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="c2d24-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2d24-138">OUTPUTS</span></span>

### <span data-ttu-id="c2d24-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="c2d24-139">System.Void</span></span>

### <span data-ttu-id="c2d24-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c2d24-140">System.Boolean</span></span>

## <span data-ttu-id="c2d24-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c2d24-141">NOTES</span></span>

## <span data-ttu-id="c2d24-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c2d24-142">RELATED LINKS</span></span>
