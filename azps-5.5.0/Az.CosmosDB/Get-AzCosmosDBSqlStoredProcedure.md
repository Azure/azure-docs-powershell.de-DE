---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144545"
---
# <span data-ttu-id="721a5-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="721a5-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="721a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="721a5-102">SYNOPSIS</span></span>
<span data-ttu-id="721a5-103">Ruft die SkriptsDB Sql StoredProcedure ab.</span><span class="sxs-lookup"><span data-stu-id="721a5-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="721a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="721a5-104">SYNTAX</span></span>

### <span data-ttu-id="721a5-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="721a5-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="721a5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="721a5-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="721a5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="721a5-107">DESCRIPTION</span></span>
<span data-ttu-id="721a5-108">Das Cmdlet **"Get-AzCosmosDBSqlStoredProcedure"** ruft die Liste aller vorhandenen Sql StoredProcedures für einen bestimmten ResourceGroupName, AccountName, DatabaseName und ContainerName ab und ruft eine einzelne DatenbanksDB Sql StoredProcedure für einen bestimmten ResourceGroupName, AccountName, DatabaseName, ContainerName und StoredProcedureName ab.</span><span class="sxs-lookup"><span data-stu-id="721a5-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="721a5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="721a5-109">EXAMPLES</span></span>

### <span data-ttu-id="721a5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="721a5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="721a5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="721a5-111">PARAMETERS</span></span>

### <span data-ttu-id="721a5-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="721a5-112">-AccountName</span></span>
<span data-ttu-id="721a5-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="721a5-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="721a5-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="721a5-114">-ContainerName</span></span>
<span data-ttu-id="721a5-115">Containername.</span><span class="sxs-lookup"><span data-stu-id="721a5-115">Container name.</span></span>

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

### <span data-ttu-id="721a5-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="721a5-116">-DatabaseName</span></span>
<span data-ttu-id="721a5-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="721a5-117">Database name.</span></span>

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

### <span data-ttu-id="721a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721a5-118">-DefaultProfile</span></span>
<span data-ttu-id="721a5-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="721a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="721a5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="721a5-120">-Name</span></span>
<span data-ttu-id="721a5-121">Gespeicherter Prcodecure-Name.</span><span class="sxs-lookup"><span data-stu-id="721a5-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="721a5-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="721a5-122">-ParentObject</span></span>
<span data-ttu-id="721a5-123">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="721a5-123">Sql Container object.</span></span>

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

### <span data-ttu-id="721a5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="721a5-124">-ResourceGroupName</span></span>
<span data-ttu-id="721a5-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="721a5-125">Name of resource group.</span></span>

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

### <span data-ttu-id="721a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721a5-126">CommonParameters</span></span>
<span data-ttu-id="721a5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="721a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721a5-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="721a5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721a5-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="721a5-129">INPUTS</span></span>

### <span data-ttu-id="721a5-130">Keine</span><span class="sxs-lookup"><span data-stu-id="721a5-130">None</span></span>

## <span data-ttu-id="721a5-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="721a5-131">OUTPUTS</span></span>

### <span data-ttu-id="721a5-132">Microsoft.Azure.Commands.ExesDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="721a5-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="721a5-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="721a5-133">NOTES</span></span>

## <span data-ttu-id="721a5-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="721a5-134">RELATED LINKS</span></span>
