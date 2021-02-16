---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170982"
---
# <span data-ttu-id="7a969-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="7a969-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="7a969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a969-102">SYNOPSIS</span></span>
<span data-ttu-id="7a969-103">Löscht die Sql UserDefinedFunction".</span><span class="sxs-lookup"><span data-stu-id="7a969-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="7a969-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a969-104">SYNTAX</span></span>

### <span data-ttu-id="7a969-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a969-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a969-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a969-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a969-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a969-107">DESCRIPTION</span></span>
<span data-ttu-id="7a969-108">Das **Cmdlet "Remove-AzCosmosDBSqlUserDefinedFunction"** löscht das Cmdlet "Destalldb Sql UserDefinedFunction", das den angegebenen Ressourcengruppennamen, "AccountName" und "DatabaseName" entspricht.</span><span class="sxs-lookup"><span data-stu-id="7a969-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="7a969-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a969-109">EXAMPLES</span></span>

### <span data-ttu-id="7a969-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7a969-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="7a969-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a969-111">PARAMETERS</span></span>

### <span data-ttu-id="7a969-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7a969-112">-AccountName</span></span>
<span data-ttu-id="7a969-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="7a969-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7a969-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a969-114">-Confirm</span></span>
<span data-ttu-id="7a969-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a969-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a969-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7a969-116">-ContainerName</span></span>
<span data-ttu-id="7a969-117">Containername.</span><span class="sxs-lookup"><span data-stu-id="7a969-117">Container name.</span></span>

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

### <span data-ttu-id="7a969-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7a969-118">-DatabaseName</span></span>
<span data-ttu-id="7a969-119">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="7a969-119">Database name.</span></span>

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

### <span data-ttu-id="7a969-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a969-120">-DefaultProfile</span></span>
<span data-ttu-id="7a969-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a969-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a969-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a969-122">-InputObject</span></span>
<span data-ttu-id="7a969-123">Benutzerdefiniertes Sql-Funktionsobjekt</span><span class="sxs-lookup"><span data-stu-id="7a969-123">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a969-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7a969-124">-Name</span></span>
<span data-ttu-id="7a969-125">Benutzerdefinierter Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="7a969-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="7a969-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a969-126">-PassThru</span></span>
<span data-ttu-id="7a969-127">Soll auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="7a969-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="7a969-128">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war, und andern falls nicht, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7a969-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="7a969-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a969-129">-ResourceGroupName</span></span>
<span data-ttu-id="7a969-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7a969-130">Name of resource group.</span></span>

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

### <span data-ttu-id="7a969-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7a969-131">-WhatIf</span></span>
<span data-ttu-id="7a969-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a969-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a969-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a969-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a969-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a969-134">CommonParameters</span></span>
<span data-ttu-id="7a969-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a969-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a969-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a969-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a969-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a969-137">INPUTS</span></span>

### <span data-ttu-id="7a969-138">Keine</span><span class="sxs-lookup"><span data-stu-id="7a969-138">None</span></span>

## <span data-ttu-id="7a969-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a969-139">OUTPUTS</span></span>

### <span data-ttu-id="7a969-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="7a969-140">System.Void</span></span>

### <span data-ttu-id="7a969-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a969-141">System.Boolean</span></span>

## <span data-ttu-id="7a969-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7a969-142">NOTES</span></span>

## <span data-ttu-id="7a969-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7a969-143">RELATED LINKS</span></span>
