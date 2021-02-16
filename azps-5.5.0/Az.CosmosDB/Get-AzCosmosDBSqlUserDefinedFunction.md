---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: b2f6e203b1ef8f14623df2910b853ea6f3841f72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148609"
---
# <span data-ttu-id="f56a2-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="f56a2-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="f56a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f56a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f56a2-103">Ruft die benutzerdefinierte Sql User Defined -Funktion "Deserdb" ab.</span><span class="sxs-lookup"><span data-stu-id="f56a2-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="f56a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f56a2-104">SYNTAX</span></span>

### <span data-ttu-id="f56a2-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f56a2-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f56a2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f56a2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f56a2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f56a2-107">DESCRIPTION</span></span>
<span data-ttu-id="f56a2-108">Das Cmdlet **"Get-AzCosmosDBSqlUserDefinedFunction"** ruft die Liste aller vorhandenen Sql UserDefinedFunctions für einen bestimmten ResourceGroupName, AccountName, DatabaseName und ContainerName ab und ruft eine einzelne Abspieldb Sql UserDefinedFunction für einen angegebenen ResourceGroupName, AccountName, DatabaseName, ContainerName und UserDefinedFunctionName ab.</span><span class="sxs-lookup"><span data-stu-id="f56a2-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="f56a2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f56a2-109">EXAMPLES</span></span>

### <span data-ttu-id="f56a2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f56a2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="f56a2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f56a2-111">PARAMETERS</span></span>

### <span data-ttu-id="f56a2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f56a2-112">-AccountName</span></span>
<span data-ttu-id="f56a2-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="f56a2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f56a2-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="f56a2-114">-ContainerName</span></span>
<span data-ttu-id="f56a2-115">Containername.</span><span class="sxs-lookup"><span data-stu-id="f56a2-115">Container name.</span></span>

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

### <span data-ttu-id="f56a2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f56a2-116">-DatabaseName</span></span>
<span data-ttu-id="f56a2-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="f56a2-117">Database name.</span></span>

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

### <span data-ttu-id="f56a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f56a2-118">-DefaultProfile</span></span>
<span data-ttu-id="f56a2-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f56a2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f56a2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f56a2-120">-Name</span></span>
<span data-ttu-id="f56a2-121">Benutzerdefinierter Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="f56a2-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="f56a2-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f56a2-122">-ParentObject</span></span>
<span data-ttu-id="f56a2-123">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f56a2-123">Sql Container object.</span></span>

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

### <span data-ttu-id="f56a2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f56a2-124">-ResourceGroupName</span></span>
<span data-ttu-id="f56a2-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f56a2-125">Name of resource group.</span></span>

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

### <span data-ttu-id="f56a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f56a2-126">CommonParameters</span></span>
<span data-ttu-id="f56a2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f56a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f56a2-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f56a2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f56a2-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f56a2-129">INPUTS</span></span>

### <span data-ttu-id="f56a2-130">Keine</span><span class="sxs-lookup"><span data-stu-id="f56a2-130">None</span></span>

## <span data-ttu-id="f56a2-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f56a2-131">OUTPUTS</span></span>

### <span data-ttu-id="f56a2-132">Microsoft.Azure.Commands.ExesDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="f56a2-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="f56a2-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f56a2-133">NOTES</span></span>

## <span data-ttu-id="f56a2-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f56a2-134">RELATED LINKS</span></span>
