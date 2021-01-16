---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297586"
---
# <span data-ttu-id="7ded1-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="7ded1-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="7ded1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ded1-102">SYNOPSIS</span></span>
<span data-ttu-id="7ded1-103">Erstellt eine neue Sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="7ded1-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="7ded1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ded1-104">SYNTAX</span></span>

### <span data-ttu-id="7ded1-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ded1-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ded1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ded1-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ded1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ded1-107">DESCRIPTION</span></span>
<span data-ttu-id="7ded1-108">Erstellt eine neue Sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="7ded1-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="7ded1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ded1-109">EXAMPLES</span></span>

### <span data-ttu-id="7ded1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ded1-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="7ded1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ded1-111">PARAMETERS</span></span>

### <span data-ttu-id="7ded1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7ded1-112">-AccountName</span></span>
<span data-ttu-id="7ded1-113">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="7ded1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7ded1-114">-Body</span><span class="sxs-lookup"><span data-stu-id="7ded1-114">-Body</span></span>
<span data-ttu-id="7ded1-115">Der Textkörper der benutzerdefinierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="7ded1-115">The body of the User Defined Function.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ded1-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ded1-116">-Confirm</span></span>
<span data-ttu-id="7ded1-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ded1-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ded1-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7ded1-118">-ContainerName</span></span>
<span data-ttu-id="7ded1-119">Containername.</span><span class="sxs-lookup"><span data-stu-id="7ded1-119">Container name.</span></span>

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

### <span data-ttu-id="7ded1-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7ded1-120">-DatabaseName</span></span>
<span data-ttu-id="7ded1-121">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="7ded1-121">Database name.</span></span>

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

### <span data-ttu-id="7ded1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ded1-122">-DefaultProfile</span></span>
<span data-ttu-id="7ded1-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ded1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ded1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7ded1-124">-Name</span></span>
<span data-ttu-id="7ded1-125">Benutzerdefinierter Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="7ded1-125">User Defined Function Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ded1-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7ded1-126">-ParentObject</span></span>
<span data-ttu-id="7ded1-127">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7ded1-127">Sql Container object.</span></span>

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

### <span data-ttu-id="7ded1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ded1-128">-ResourceGroupName</span></span>
<span data-ttu-id="7ded1-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7ded1-129">Name of resource group.</span></span>

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

### <span data-ttu-id="7ded1-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7ded1-130">-WhatIf</span></span>
<span data-ttu-id="7ded1-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ded1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ded1-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ded1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ded1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ded1-133">CommonParameters</span></span>
<span data-ttu-id="7ded1-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ded1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ded1-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ded1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ded1-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ded1-136">INPUTS</span></span>

### <span data-ttu-id="7ded1-137">Microsoft.Azure.Commands.ExesDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="7ded1-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="7ded1-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ded1-138">OUTPUTS</span></span>

### <span data-ttu-id="7ded1-139">Microsoft.Azure.Commands.ExesDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="7ded1-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="7ded1-140">Microsoft.Azure.Commands.DiesDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="7ded1-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="7ded1-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7ded1-141">NOTES</span></span>

## <span data-ttu-id="7ded1-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7ded1-142">RELATED LINKS</span></span>
