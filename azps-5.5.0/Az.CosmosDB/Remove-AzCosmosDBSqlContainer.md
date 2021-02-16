---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171017"
---
# <span data-ttu-id="95a95-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="95a95-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="95a95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95a95-102">SYNOPSIS</span></span>
<span data-ttu-id="95a95-103">Löscht den Sql-Container".</span><span class="sxs-lookup"><span data-stu-id="95a95-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="95a95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95a95-104">SYNTAX</span></span>

### <span data-ttu-id="95a95-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="95a95-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95a95-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95a95-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95a95-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95a95-107">DESCRIPTION</span></span>
<span data-ttu-id="95a95-108">Das **Cmdlet "Remove-AzCosmosDBSqlContainer"** löscht den Sql Container", der den angegebenen Ressourcengruppennamen, "AccountName", "DatabaseName" und "ContainerName" entspricht.</span><span class="sxs-lookup"><span data-stu-id="95a95-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="95a95-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95a95-109">EXAMPLES</span></span>

### <span data-ttu-id="95a95-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95a95-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="95a95-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95a95-111">PARAMETERS</span></span>

### <span data-ttu-id="95a95-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="95a95-112">-AccountName</span></span>
<span data-ttu-id="95a95-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="95a95-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="95a95-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95a95-114">-Confirm</span></span>
<span data-ttu-id="95a95-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95a95-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95a95-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="95a95-116">-DatabaseName</span></span>
<span data-ttu-id="95a95-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="95a95-117">Database name.</span></span>

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

### <span data-ttu-id="95a95-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95a95-118">-DefaultProfile</span></span>
<span data-ttu-id="95a95-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95a95-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95a95-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95a95-120">-InputObject</span></span>
<span data-ttu-id="95a95-121">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="95a95-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95a95-122">-Name</span><span class="sxs-lookup"><span data-stu-id="95a95-122">-Name</span></span>
<span data-ttu-id="95a95-123">Containername.</span><span class="sxs-lookup"><span data-stu-id="95a95-123">Container name.</span></span>

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

### <span data-ttu-id="95a95-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95a95-124">-PassThru</span></span>
<span data-ttu-id="95a95-125">Soll auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="95a95-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="95a95-126">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war, und andern falls nicht, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="95a95-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="95a95-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95a95-127">-ResourceGroupName</span></span>
<span data-ttu-id="95a95-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="95a95-128">Name of resource group.</span></span>

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

### <span data-ttu-id="95a95-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="95a95-129">-WhatIf</span></span>
<span data-ttu-id="95a95-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95a95-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95a95-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95a95-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95a95-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a95-132">CommonParameters</span></span>
<span data-ttu-id="95a95-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95a95-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a95-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95a95-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a95-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95a95-135">INPUTS</span></span>

### <span data-ttu-id="95a95-136">Keine</span><span class="sxs-lookup"><span data-stu-id="95a95-136">None</span></span>

## <span data-ttu-id="95a95-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95a95-137">OUTPUTS</span></span>

### <span data-ttu-id="95a95-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="95a95-138">System.Void</span></span>

### <span data-ttu-id="95a95-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="95a95-139">System.Boolean</span></span>

## <span data-ttu-id="95a95-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="95a95-140">NOTES</span></span>

## <span data-ttu-id="95a95-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="95a95-141">RELATED LINKS</span></span>
