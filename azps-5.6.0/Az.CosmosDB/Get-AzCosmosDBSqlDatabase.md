---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 6d0fe9565a969de19234d65378fd91a1af7a327f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950299"
---
# <span data-ttu-id="2c62d-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2c62d-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="2c62d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c62d-102">SYNOPSIS</span></span>
<span data-ttu-id="2c62d-103">Ruft die CosmosDB Sql-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="2c62d-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="2c62d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c62d-104">SYNTAX</span></span>

### <span data-ttu-id="2c62d-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2c62d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c62d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c62d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c62d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c62d-107">DESCRIPTION</span></span>
<span data-ttu-id="2c62d-108">Das **Get-AzCosmosDBSqlDatabase-Cmdlet** ruft die Liste aller vorhandenen CosmosDB-Sql-Datenbanken für einen bestimmten ResourceGroupName, AccountName ab und ruft eine einzelne CosmosDB-Sql-Datenbank für einen bestimmten ResourceGroupName, AccountName, DatabaseName und ContainerName ab.</span><span class="sxs-lookup"><span data-stu-id="2c62d-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="2c62d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2c62d-109">EXAMPLES</span></span>

### <span data-ttu-id="2c62d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c62d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="2c62d-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2c62d-111">PARAMETERS</span></span>

### <span data-ttu-id="2c62d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2c62d-112">-AccountName</span></span>
<span data-ttu-id="2c62d-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="2c62d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2c62d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c62d-114">-DefaultProfile</span></span>
<span data-ttu-id="2c62d-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c62d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c62d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2c62d-116">-Name</span></span>
<span data-ttu-id="2c62d-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="2c62d-117">Database name.</span></span>

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

### <span data-ttu-id="2c62d-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2c62d-118">-ParentObject</span></span>
<span data-ttu-id="2c62d-119">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="2c62d-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="2c62d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c62d-120">-ResourceGroupName</span></span>
<span data-ttu-id="2c62d-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2c62d-121">Name of resource group.</span></span>

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

### <span data-ttu-id="2c62d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c62d-122">CommonParameters</span></span>
<span data-ttu-id="2c62d-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c62d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c62d-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c62d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c62d-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2c62d-125">INPUTS</span></span>

### <span data-ttu-id="2c62d-126">Keine</span><span class="sxs-lookup"><span data-stu-id="2c62d-126">None</span></span>

## <span data-ttu-id="2c62d-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2c62d-127">OUTPUTS</span></span>

### <span data-ttu-id="2c62d-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2c62d-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="2c62d-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2c62d-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2c62d-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2c62d-130">NOTES</span></span>

## <span data-ttu-id="2c62d-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2c62d-131">RELATED LINKS</span></span>
