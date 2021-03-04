---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 7e7ffd7c06217b4e2d12aaf75684c85f8ab12e9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934243"
---
# <span data-ttu-id="9ffc1-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="9ffc1-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="9ffc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ffc1-102">SYNOPSIS</span></span>
<span data-ttu-id="9ffc1-103">Löscht die Funktion "CosmosDB Sql UserDefinedFunction".</span><span class="sxs-lookup"><span data-stu-id="9ffc1-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="9ffc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ffc1-104">SYNTAX</span></span>

### <span data-ttu-id="9ffc1-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ffc1-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ffc1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ffc1-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ffc1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ffc1-107">DESCRIPTION</span></span>
<span data-ttu-id="9ffc1-108">Das **Cmdlet Remove-AzCosmosDBSqlUserDefinedFunction** löscht das CosmosDB Sql UserDefinedFunction, das den angegebenen ResourceGroupName, AccountName und DatabaseName entspricht.</span><span class="sxs-lookup"><span data-stu-id="9ffc1-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="9ffc1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ffc1-109">EXAMPLES</span></span>

### <span data-ttu-id="9ffc1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ffc1-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="9ffc1-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9ffc1-111">PARAMETERS</span></span>

### <span data-ttu-id="9ffc1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9ffc1-112">-AccountName</span></span>
<span data-ttu-id="9ffc1-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="9ffc1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9ffc1-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ffc1-114">-Confirm</span></span>
<span data-ttu-id="9ffc1-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ffc1-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ffc1-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9ffc1-116">-ContainerName</span></span>
<span data-ttu-id="9ffc1-117">Containername.</span><span class="sxs-lookup"><span data-stu-id="9ffc1-117">Container name.</span></span>

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

### <span data-ttu-id="9ffc1-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9ffc1-118">-DatabaseName</span></span>
<span data-ttu-id="9ffc1-119">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="9ffc1-119">Database name.</span></span>

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

### <span data-ttu-id="9ffc1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ffc1-120">-DefaultProfile</span></span>
<span data-ttu-id="9ffc1-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ffc1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ffc1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ffc1-122">-InputObject</span></span>
<span data-ttu-id="9ffc1-123">Sql User Defined Function Object</span><span class="sxs-lookup"><span data-stu-id="9ffc1-123">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="9ffc1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9ffc1-124">-Name</span></span>
<span data-ttu-id="9ffc1-125">Benutzerdefinierter Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="9ffc1-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="9ffc1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ffc1-126">-PassThru</span></span>
<span data-ttu-id="9ffc1-127">Um auf true festgelegt zu sein, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="9ffc1-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="9ffc1-128">Die Ausgabe ist true, wenn der Vorgang erfolgreich war und ein Fehler ausgelöst wird, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="9ffc1-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="9ffc1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ffc1-129">-ResourceGroupName</span></span>
<span data-ttu-id="9ffc1-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9ffc1-130">Name of resource group.</span></span>

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

### <span data-ttu-id="9ffc1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ffc1-131">-WhatIf</span></span>
<span data-ttu-id="9ffc1-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ffc1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ffc1-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ffc1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ffc1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ffc1-134">CommonParameters</span></span>
<span data-ttu-id="9ffc1-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ffc1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ffc1-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ffc1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ffc1-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ffc1-137">INPUTS</span></span>

### <span data-ttu-id="9ffc1-138">Keine</span><span class="sxs-lookup"><span data-stu-id="9ffc1-138">None</span></span>

## <span data-ttu-id="9ffc1-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ffc1-139">OUTPUTS</span></span>

### <span data-ttu-id="9ffc1-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="9ffc1-140">System.Void</span></span>

### <span data-ttu-id="9ffc1-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9ffc1-141">System.Boolean</span></span>

## <span data-ttu-id="9ffc1-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9ffc1-142">NOTES</span></span>

## <span data-ttu-id="9ffc1-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9ffc1-143">RELATED LINKS</span></span>
