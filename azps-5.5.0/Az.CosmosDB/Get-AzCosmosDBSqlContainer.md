---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171047"
---
# <span data-ttu-id="4aad4-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="4aad4-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="4aad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aad4-102">SYNOPSIS</span></span>
<span data-ttu-id="4aad4-103">Ruft den Sql Container für Die Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="4aad4-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="4aad4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4aad4-104">SYNTAX</span></span>

### <span data-ttu-id="4aad4-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4aad4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="4aad4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aad4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aad4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4aad4-107">DESCRIPTION</span></span>
<span data-ttu-id="4aad4-108">Das **Cmdlet "Get-AzCosmosDBSqlContainer"** ruft die Liste aller vorhandenen "DessDB Sql Containers" für einen bestimmten ResourceGroupName, AccountName und DatabaseName ab und ruft einen einzelnen DurchlaufsDB -Sql-Container für einen angegebenen ResourceGroupName, AccountName, DatabaseName und ContainerName ab.</span><span class="sxs-lookup"><span data-stu-id="4aad4-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="4aad4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4aad4-109">EXAMPLES</span></span>

### <span data-ttu-id="4aad4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4aad4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="4aad4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4aad4-111">PARAMETERS</span></span>

### <span data-ttu-id="4aad4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4aad4-112">-AccountName</span></span>
<span data-ttu-id="4aad4-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="4aad4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4aad4-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4aad4-114">-DatabaseName</span></span>
<span data-ttu-id="4aad4-115">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="4aad4-115">Database name.</span></span>

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

### <span data-ttu-id="4aad4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aad4-116">-DefaultProfile</span></span>
<span data-ttu-id="4aad4-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4aad4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aad4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4aad4-118">-Name</span></span>
<span data-ttu-id="4aad4-119">Containername.</span><span class="sxs-lookup"><span data-stu-id="4aad4-119">Container name.</span></span>

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

### <span data-ttu-id="4aad4-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4aad4-120">-ParentObject</span></span>
<span data-ttu-id="4aad4-121">Sql-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="4aad4-121">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4aad4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aad4-122">-ResourceGroupName</span></span>
<span data-ttu-id="4aad4-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4aad4-123">Name of resource group.</span></span>

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

### <span data-ttu-id="4aad4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aad4-124">CommonParameters</span></span>
<span data-ttu-id="4aad4-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aad4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aad4-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4aad4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aad4-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4aad4-127">INPUTS</span></span>

### <span data-ttu-id="4aad4-128">Keine</span><span class="sxs-lookup"><span data-stu-id="4aad4-128">None</span></span>

## <span data-ttu-id="4aad4-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4aad4-129">OUTPUTS</span></span>

### <span data-ttu-id="4aad4-130">Microsoft.Azure.Commands.ExesDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="4aad4-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="4aad4-131">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4aad4-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4aad4-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4aad4-132">NOTES</span></span>

## <span data-ttu-id="4aad4-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4aad4-133">RELATED LINKS</span></span>
