---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295930"
---
# <span data-ttu-id="a2c20-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="a2c20-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="a2c20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2c20-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c20-103">Löscht das Sql StoredProcedure-Element".</span><span class="sxs-lookup"><span data-stu-id="a2c20-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="a2c20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2c20-104">SYNTAX</span></span>

### <span data-ttu-id="a2c20-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2c20-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c20-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2c20-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2c20-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2c20-107">DESCRIPTION</span></span>
<span data-ttu-id="a2c20-108">Das **Cmdlet "Remove-AzCosmosDBSqlStoredProcedure"** löscht das SkriptsDB Sql StoredProcedure, das den angegebenen Angaben "ResourceGroupName", "AccountName" und "DatabaseName" entspricht.</span><span class="sxs-lookup"><span data-stu-id="a2c20-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="a2c20-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a2c20-109">EXAMPLES</span></span>

### <span data-ttu-id="a2c20-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2c20-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="a2c20-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2c20-111">PARAMETERS</span></span>

### <span data-ttu-id="a2c20-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a2c20-112">-AccountName</span></span>
<span data-ttu-id="a2c20-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="a2c20-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a2c20-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2c20-114">-Confirm</span></span>
<span data-ttu-id="a2c20-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2c20-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2c20-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a2c20-116">-ContainerName</span></span>
<span data-ttu-id="a2c20-117">Containername.</span><span class="sxs-lookup"><span data-stu-id="a2c20-117">Container name.</span></span>

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

### <span data-ttu-id="a2c20-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2c20-118">-DatabaseName</span></span>
<span data-ttu-id="a2c20-119">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="a2c20-119">Database name.</span></span>

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

### <span data-ttu-id="a2c20-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c20-120">-DefaultProfile</span></span>
<span data-ttu-id="a2c20-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2c20-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2c20-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2c20-122">-InputObject</span></span>
<span data-ttu-id="a2c20-123">Sql-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="a2c20-123">Sql Database object.</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c20-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a2c20-124">-Name</span></span>
<span data-ttu-id="a2c20-125">Gespeicherter Prcodecure-Name.</span><span class="sxs-lookup"><span data-stu-id="a2c20-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="a2c20-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2c20-126">-PassThru</span></span>
<span data-ttu-id="a2c20-127">Wird auf "true" festgelegt, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="a2c20-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="a2c20-128">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war und andern falls nicht ein Fehler ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="a2c20-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="a2c20-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c20-129">-ResourceGroupName</span></span>
<span data-ttu-id="a2c20-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a2c20-130">Name of resource group.</span></span>

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

### <span data-ttu-id="a2c20-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a2c20-131">-WhatIf</span></span>
<span data-ttu-id="a2c20-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2c20-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2c20-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2c20-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2c20-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c20-134">CommonParameters</span></span>
<span data-ttu-id="a2c20-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c20-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c20-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2c20-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c20-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a2c20-137">INPUTS</span></span>

### <span data-ttu-id="a2c20-138">Keine</span><span class="sxs-lookup"><span data-stu-id="a2c20-138">None</span></span>

## <span data-ttu-id="a2c20-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a2c20-139">OUTPUTS</span></span>

### <span data-ttu-id="a2c20-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="a2c20-140">System.Void</span></span>

### <span data-ttu-id="a2c20-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a2c20-141">System.Boolean</span></span>

## <span data-ttu-id="a2c20-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a2c20-142">NOTES</span></span>

## <span data-ttu-id="a2c20-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a2c20-143">RELATED LINKS</span></span>
