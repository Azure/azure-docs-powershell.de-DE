---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166244"
---
# <span data-ttu-id="5097c-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5097c-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="5097c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5097c-102">SYNOPSIS</span></span>
<span data-ttu-id="5097c-103">Ruft die Sql-Datenbank "DessDB" ab.</span><span class="sxs-lookup"><span data-stu-id="5097c-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="5097c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5097c-104">SYNTAX</span></span>

### <span data-ttu-id="5097c-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5097c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5097c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5097c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5097c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5097c-107">DESCRIPTION</span></span>
<span data-ttu-id="5097c-108">Das **Cmdlet "Get-AzCosmosDBSqlDatabase"** ruft die Liste aller vorhandenen Sql-Datenbanken des TypEsdb sql für einen bestimmten ResourceGroupName,AccountName ab und ruft eine einzelneBasesDB -Sql-Datenbank für einen bestimmten ResourceGroupName, AccountName, DatabaseName und ContainerName ab.</span><span class="sxs-lookup"><span data-stu-id="5097c-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="5097c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5097c-109">EXAMPLES</span></span>

### <span data-ttu-id="5097c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5097c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="5097c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5097c-111">PARAMETERS</span></span>

### <span data-ttu-id="5097c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5097c-112">-AccountName</span></span>
<span data-ttu-id="5097c-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="5097c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5097c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5097c-114">-DefaultProfile</span></span>
<span data-ttu-id="5097c-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5097c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5097c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5097c-116">-Name</span></span>
<span data-ttu-id="5097c-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="5097c-117">Database name.</span></span>

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

### <span data-ttu-id="5097c-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5097c-118">-ParentObject</span></span>
<span data-ttu-id="5097c-119">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="5097c-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5097c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5097c-120">-ResourceGroupName</span></span>
<span data-ttu-id="5097c-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5097c-121">Name of resource group.</span></span>

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

### <span data-ttu-id="5097c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5097c-122">CommonParameters</span></span>
<span data-ttu-id="5097c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5097c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5097c-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5097c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5097c-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5097c-125">INPUTS</span></span>

### <span data-ttu-id="5097c-126">Keine</span><span class="sxs-lookup"><span data-stu-id="5097c-126">None</span></span>

## <span data-ttu-id="5097c-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5097c-127">OUTPUTS</span></span>

### <span data-ttu-id="5097c-128">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5097c-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="5097c-129">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5097c-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5097c-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5097c-130">NOTES</span></span>

## <span data-ttu-id="5097c-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5097c-131">RELATED LINKS</span></span>
