---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472851"
---
# <span data-ttu-id="8098f-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="8098f-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="8098f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8098f-102">SYNOPSIS</span></span>
<span data-ttu-id="8098f-103">Ruft die SkriptsDB Sql StoredProcedure ab.</span><span class="sxs-lookup"><span data-stu-id="8098f-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="8098f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8098f-104">SYNTAX</span></span>

### <span data-ttu-id="8098f-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8098f-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8098f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8098f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8098f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8098f-107">DESCRIPTION</span></span>
<span data-ttu-id="8098f-108">Das Cmdlet **"Get-AzCosmosDBSqlStoredProcedure"** ruft die Liste aller vorhandenen Sql StoredProcedures für einen bestimmten ResourceGroupName, AccountName, DatabaseName und ContainerName ab und ruft eine einzelne DatenbanksDB Sql StoredProcedure für einen bestimmten ResourceGroupName, AccountName, DatabaseName, ContainerName und StoredProcedureName ab.</span><span class="sxs-lookup"><span data-stu-id="8098f-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="8098f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8098f-109">EXAMPLES</span></span>

### <span data-ttu-id="8098f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8098f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="8098f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8098f-111">PARAMETERS</span></span>

### <span data-ttu-id="8098f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8098f-112">-AccountName</span></span>
<span data-ttu-id="8098f-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="8098f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8098f-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8098f-114">-ContainerName</span></span>
<span data-ttu-id="8098f-115">Containername.</span><span class="sxs-lookup"><span data-stu-id="8098f-115">Container name.</span></span>

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

### <span data-ttu-id="8098f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8098f-116">-DatabaseName</span></span>
<span data-ttu-id="8098f-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="8098f-117">Database name.</span></span>

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

### <span data-ttu-id="8098f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8098f-118">-DefaultProfile</span></span>
<span data-ttu-id="8098f-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8098f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8098f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8098f-120">-Name</span></span>
<span data-ttu-id="8098f-121">Gespeicherter Prcodecure-Name.</span><span class="sxs-lookup"><span data-stu-id="8098f-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="8098f-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8098f-122">-ParentObject</span></span>
<span data-ttu-id="8098f-123">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8098f-123">Sql Container object.</span></span>

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

### <span data-ttu-id="8098f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8098f-124">-ResourceGroupName</span></span>
<span data-ttu-id="8098f-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8098f-125">Name of resource group.</span></span>

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

### <span data-ttu-id="8098f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8098f-126">CommonParameters</span></span>
<span data-ttu-id="8098f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8098f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8098f-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8098f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8098f-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8098f-129">INPUTS</span></span>

### <span data-ttu-id="8098f-130">Keine</span><span class="sxs-lookup"><span data-stu-id="8098f-130">None</span></span>

## <span data-ttu-id="8098f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8098f-131">OUTPUTS</span></span>

### <span data-ttu-id="8098f-132">Microsoft.Azure.Commands.ExesDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="8098f-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="8098f-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8098f-133">NOTES</span></span>

## <span data-ttu-id="8098f-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8098f-134">RELATED LINKS</span></span>
