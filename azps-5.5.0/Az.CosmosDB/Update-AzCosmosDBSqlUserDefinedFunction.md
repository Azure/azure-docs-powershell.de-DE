---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148449"
---
# <span data-ttu-id="a4ecc-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="a4ecc-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="a4ecc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ecc-103">Aktualisiert die Datenbank sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="a4ecc-104">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene UserDefinedFunction gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="a4ecc-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4ecc-105">SYNTAX</span></span>

### <span data-ttu-id="a4ecc-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a4ecc-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4ecc-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4ecc-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4ecc-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4ecc-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4ecc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4ecc-109">DESCRIPTION</span></span>
<span data-ttu-id="a4ecc-110">Aktualisiert die Datenbank sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="a4ecc-111">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene UserDefinedFunction gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="a4ecc-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a4ecc-112">EXAMPLES</span></span>

### <span data-ttu-id="a4ecc-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a4ecc-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="a4ecc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4ecc-114">PARAMETERS</span></span>

### <span data-ttu-id="a4ecc-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a4ecc-115">-AccountName</span></span>
<span data-ttu-id="a4ecc-116">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a4ecc-117">-Body</span><span class="sxs-lookup"><span data-stu-id="a4ecc-117">-Body</span></span>
<span data-ttu-id="a4ecc-118">Der Textkörper der benutzerdefinierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="a4ecc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4ecc-119">-Confirm</span></span>
<span data-ttu-id="a4ecc-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4ecc-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a4ecc-121">-ContainerName</span></span>
<span data-ttu-id="a4ecc-122">Containername.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-122">Container name.</span></span>

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

### <span data-ttu-id="a4ecc-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a4ecc-123">-DatabaseName</span></span>
<span data-ttu-id="a4ecc-124">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-124">Database name.</span></span>

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

### <span data-ttu-id="a4ecc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ecc-125">-DefaultProfile</span></span>
<span data-ttu-id="a4ecc-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ecc-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4ecc-127">-InputObject</span></span>
<span data-ttu-id="a4ecc-128">Benutzerdefiniertes Sql-Funktionsobjekt</span><span class="sxs-lookup"><span data-stu-id="a4ecc-128">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="a4ecc-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a4ecc-129">-Name</span></span>
<span data-ttu-id="a4ecc-130">Benutzerdefinierter Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="a4ecc-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a4ecc-131">-ParentObject</span></span>
<span data-ttu-id="a4ecc-132">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-132">Sql Container object.</span></span>

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

### <span data-ttu-id="a4ecc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ecc-133">-ResourceGroupName</span></span>
<span data-ttu-id="a4ecc-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-134">Name of resource group.</span></span>

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

### <span data-ttu-id="a4ecc-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a4ecc-135">-WhatIf</span></span>
<span data-ttu-id="a4ecc-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4ecc-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4ecc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ecc-138">CommonParameters</span></span>
<span data-ttu-id="a4ecc-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ecc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ecc-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4ecc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ecc-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a4ecc-141">INPUTS</span></span>

### <span data-ttu-id="a4ecc-142">Microsoft.Azure.Commands.ExesDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="a4ecc-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="a4ecc-143">Microsoft.Azure.Commands.ExesDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="a4ecc-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="a4ecc-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a4ecc-144">OUTPUTS</span></span>

### <span data-ttu-id="a4ecc-145">Microsoft.Azure.Commands.ExesDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="a4ecc-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="a4ecc-146">Microsoft.Azure.Commands.UmsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="a4ecc-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="a4ecc-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a4ecc-147">NOTES</span></span>

## <span data-ttu-id="a4ecc-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a4ecc-148">RELATED LINKS</span></span>
