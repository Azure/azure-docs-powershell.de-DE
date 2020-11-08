---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003919"
---
# <span data-ttu-id="1c27a-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="1c27a-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="1c27a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c27a-102">SYNOPSIS</span></span>
<span data-ttu-id="1c27a-103">Löscht einen CosmosDB Cassandra-Keyspace.</span><span class="sxs-lookup"><span data-stu-id="1c27a-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1c27a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c27a-104">SYNTAX</span></span>

### <span data-ttu-id="1c27a-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c27a-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c27a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c27a-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c27a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c27a-107">DESCRIPTION</span></span>
<span data-ttu-id="1c27a-108">Das Cmdlet **Remove-AzCosmosDBCassandraKeyspace** löscht einen vorhandenen CosmosDB Cassandra-Keyspace.</span><span class="sxs-lookup"><span data-stu-id="1c27a-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1c27a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c27a-109">EXAMPLES</span></span>

### <span data-ttu-id="1c27a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1c27a-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="1c27a-111">Das Cmdlet gibt ein Objekt vom Typ bool zurück (wenn-passthru übergeben wird), das wahr ist, wenn der Löschvorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1c27a-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="1c27a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c27a-112">PARAMETERS</span></span>

### <span data-ttu-id="1c27a-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="1c27a-113">-AccountName</span></span>
<span data-ttu-id="1c27a-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="1c27a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1c27a-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c27a-115">-Confirm</span></span>
<span data-ttu-id="1c27a-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c27a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c27a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c27a-117">-DefaultProfile</span></span>
<span data-ttu-id="1c27a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1c27a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c27a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1c27a-119">-InputObject</span></span>
<span data-ttu-id="1c27a-120">Cassandra-Keyspace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1c27a-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="1c27a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1c27a-121">-Name</span></span>
<span data-ttu-id="1c27a-122">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="1c27a-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="1c27a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c27a-123">-PassThru</span></span>
<span data-ttu-id="1c27a-124">Auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="1c27a-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="1c27a-125">Die Ausgabe ist wahr, wenn der Vorgang erfolgreich war, und andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="1c27a-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="1c27a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c27a-126">-ResourceGroupName</span></span>
<span data-ttu-id="1c27a-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1c27a-127">Name of resource group.</span></span>

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

### <span data-ttu-id="1c27a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c27a-128">-WhatIf</span></span>
<span data-ttu-id="1c27a-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c27a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c27a-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c27a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c27a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c27a-131">CommonParameters</span></span>
<span data-ttu-id="1c27a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c27a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c27a-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c27a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c27a-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c27a-134">INPUTS</span></span>

### <span data-ttu-id="1c27a-135">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="1c27a-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="1c27a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c27a-136">OUTPUTS</span></span>

### <span data-ttu-id="1c27a-137">System. void</span><span class="sxs-lookup"><span data-stu-id="1c27a-137">System.Void</span></span>

### <span data-ttu-id="1c27a-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c27a-138">System.Boolean</span></span>

## <span data-ttu-id="1c27a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c27a-139">NOTES</span></span>

## <span data-ttu-id="1c27a-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c27a-140">RELATED LINKS</span></span>
