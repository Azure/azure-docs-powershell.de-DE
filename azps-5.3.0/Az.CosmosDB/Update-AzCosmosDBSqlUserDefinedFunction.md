---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472764"
---
# <span data-ttu-id="bf5fa-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="bf5fa-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="bf5fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5fa-103">Aktualisiert die Datenbank sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="bf5fa-104">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene UserDefinedFunction gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="bf5fa-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf5fa-105">SYNTAX</span></span>

### <span data-ttu-id="bf5fa-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf5fa-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf5fa-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf5fa-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf5fa-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf5fa-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf5fa-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf5fa-109">DESCRIPTION</span></span>
<span data-ttu-id="bf5fa-110">Aktualisiert die Datenbank sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="bf5fa-111">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene UserDefinedFunction gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="bf5fa-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf5fa-112">EXAMPLES</span></span>

### <span data-ttu-id="bf5fa-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf5fa-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="bf5fa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf5fa-114">PARAMETERS</span></span>

### <span data-ttu-id="bf5fa-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bf5fa-115">-AccountName</span></span>
<span data-ttu-id="bf5fa-116">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bf5fa-117">-Body</span><span class="sxs-lookup"><span data-stu-id="bf5fa-117">-Body</span></span>
<span data-ttu-id="bf5fa-118">Der Textkörper der benutzerdefinierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-118">The body of the User Defined Function.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf5fa-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf5fa-119">-Confirm</span></span>
<span data-ttu-id="bf5fa-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf5fa-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="bf5fa-121">-ContainerName</span></span>
<span data-ttu-id="bf5fa-122">Containername.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-122">Container name.</span></span>

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

### <span data-ttu-id="bf5fa-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bf5fa-123">-DatabaseName</span></span>
<span data-ttu-id="bf5fa-124">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-124">Database name.</span></span>

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

### <span data-ttu-id="bf5fa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf5fa-125">-DefaultProfile</span></span>
<span data-ttu-id="bf5fa-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf5fa-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf5fa-127">-InputObject</span></span>
<span data-ttu-id="bf5fa-128">Benutzerdefiniertes Sql-Funktionsobjekt</span><span class="sxs-lookup"><span data-stu-id="bf5fa-128">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="bf5fa-129">-Name</span><span class="sxs-lookup"><span data-stu-id="bf5fa-129">-Name</span></span>
<span data-ttu-id="bf5fa-130">Benutzerdefinierter Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-130">User Defined Function Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf5fa-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bf5fa-131">-ParentObject</span></span>
<span data-ttu-id="bf5fa-132">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-132">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf5fa-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf5fa-133">-ResourceGroupName</span></span>
<span data-ttu-id="bf5fa-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-134">Name of resource group.</span></span>

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

### <span data-ttu-id="bf5fa-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bf5fa-135">-WhatIf</span></span>
<span data-ttu-id="bf5fa-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf5fa-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf5fa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5fa-138">CommonParameters</span></span>
<span data-ttu-id="bf5fa-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5fa-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf5fa-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5fa-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf5fa-141">INPUTS</span></span>

### <span data-ttu-id="bf5fa-142">Microsoft.Azure.Commands.ExesDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="bf5fa-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="bf5fa-143">Microsoft.Azure.Commands.ExesDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="bf5fa-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="bf5fa-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf5fa-144">OUTPUTS</span></span>

### <span data-ttu-id="bf5fa-145">Microsoft.Azure.Commands.ExesDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="bf5fa-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="bf5fa-146">Microsoft.Azure.Commands.Abt. Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="bf5fa-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="bf5fa-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bf5fa-147">NOTES</span></span>

## <span data-ttu-id="bf5fa-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bf5fa-148">RELATED LINKS</span></span>
