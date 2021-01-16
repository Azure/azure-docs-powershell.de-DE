---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294617"
---
# <span data-ttu-id="66d0f-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="66d0f-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="66d0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="66d0f-103">Ruft die Sql-Datenbank "Dessdb" ab.</span><span class="sxs-lookup"><span data-stu-id="66d0f-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="66d0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66d0f-104">SYNTAX</span></span>

### <span data-ttu-id="66d0f-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="66d0f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d0f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d0f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66d0f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66d0f-107">DESCRIPTION</span></span>
<span data-ttu-id="66d0f-108">Das **Cmdlet "Get-AzCosmosDBSqlDatabase"** ruft die Liste aller vorhandenen Sql-Datenbanken des TypEsdb sql für einen bestimmten ResourceGroupName,AccountName ab und ruft eine einzelneBasesDB -Sql-Datenbank für einen bestimmten ResourceGroupName, AccountName, DatabaseName und ContainerName ab.</span><span class="sxs-lookup"><span data-stu-id="66d0f-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="66d0f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66d0f-109">EXAMPLES</span></span>

### <span data-ttu-id="66d0f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66d0f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="66d0f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66d0f-111">PARAMETERS</span></span>

### <span data-ttu-id="66d0f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66d0f-112">-AccountName</span></span>
<span data-ttu-id="66d0f-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="66d0f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="66d0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d0f-114">-DefaultProfile</span></span>
<span data-ttu-id="66d0f-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66d0f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66d0f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="66d0f-116">-Name</span></span>
<span data-ttu-id="66d0f-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="66d0f-117">Database name.</span></span>

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

### <span data-ttu-id="66d0f-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="66d0f-118">-ParentObject</span></span>
<span data-ttu-id="66d0f-119">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="66d0f-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="66d0f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66d0f-120">-ResourceGroupName</span></span>
<span data-ttu-id="66d0f-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="66d0f-121">Name of resource group.</span></span>

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

### <span data-ttu-id="66d0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d0f-122">CommonParameters</span></span>
<span data-ttu-id="66d0f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66d0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d0f-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66d0f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d0f-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66d0f-125">INPUTS</span></span>

### <span data-ttu-id="66d0f-126">Keine</span><span class="sxs-lookup"><span data-stu-id="66d0f-126">None</span></span>

## <span data-ttu-id="66d0f-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66d0f-127">OUTPUTS</span></span>

### <span data-ttu-id="66d0f-128">Microsoft.Azure.Commands.ExesDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="66d0f-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="66d0f-129">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="66d0f-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="66d0f-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="66d0f-130">NOTES</span></span>

## <span data-ttu-id="66d0f-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="66d0f-131">RELATED LINKS</span></span>
