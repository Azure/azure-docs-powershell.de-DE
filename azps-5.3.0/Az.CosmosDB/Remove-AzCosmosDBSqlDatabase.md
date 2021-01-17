---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472791"
---
# <span data-ttu-id="d7dc2-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d7dc2-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="d7dc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="d7dc2-103">Löscht die Datenbank DestallenDB Sql.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="d7dc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7dc2-104">SYNTAX</span></span>

### <span data-ttu-id="d7dc2-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7dc2-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7dc2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7dc2-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7dc2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7dc2-107">DESCRIPTION</span></span>
<span data-ttu-id="d7dc2-108">Das **Cmdlet "Remove-AzCosmosDBSqlDatabase"** löscht dieBasesDB-Sql-Datenbank, die dem angegebenen ResourceGroupName, AccountName und DatabaseName entspricht.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="d7dc2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d7dc2-109">EXAMPLES</span></span>

### <span data-ttu-id="d7dc2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d7dc2-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="d7dc2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7dc2-111">PARAMETERS</span></span>

### <span data-ttu-id="d7dc2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d7dc2-112">-AccountName</span></span>
<span data-ttu-id="d7dc2-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d7dc2-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7dc2-114">-Confirm</span></span>
<span data-ttu-id="d7dc2-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7dc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7dc2-116">-DefaultProfile</span></span>
<span data-ttu-id="d7dc2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7dc2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7dc2-118">-InputObject</span></span>
<span data-ttu-id="d7dc2-119">Sql-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-119">Sql Database object.</span></span>

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

### <span data-ttu-id="d7dc2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d7dc2-120">-Name</span></span>
<span data-ttu-id="d7dc2-121">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-121">Database name.</span></span>

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

### <span data-ttu-id="d7dc2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7dc2-122">-PassThru</span></span>
<span data-ttu-id="d7dc2-123">Wird auf "true" festgelegt, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="d7dc2-124">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war und andern falls nicht ein Fehler ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="d7dc2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7dc2-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7dc2-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-126">Name of resource group.</span></span>

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

### <span data-ttu-id="d7dc2-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d7dc2-127">-WhatIf</span></span>
<span data-ttu-id="d7dc2-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7dc2-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7dc2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7dc2-130">CommonParameters</span></span>
<span data-ttu-id="d7dc2-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7dc2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7dc2-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7dc2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7dc2-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d7dc2-133">INPUTS</span></span>

### <span data-ttu-id="d7dc2-134">Keine</span><span class="sxs-lookup"><span data-stu-id="d7dc2-134">None</span></span>

## <span data-ttu-id="d7dc2-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d7dc2-135">OUTPUTS</span></span>

### <span data-ttu-id="d7dc2-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="d7dc2-136">System.Void</span></span>

### <span data-ttu-id="d7dc2-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d7dc2-137">System.Boolean</span></span>

## <span data-ttu-id="d7dc2-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d7dc2-138">NOTES</span></span>

## <span data-ttu-id="d7dc2-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d7dc2-139">RELATED LINKS</span></span>
