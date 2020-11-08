---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174404"
---
# <span data-ttu-id="f29d4-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f29d4-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="f29d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f29d4-102">SYNOPSIS</span></span>
<span data-ttu-id="f29d4-103">Ruft die CosmosDB-SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="f29d4-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="f29d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f29d4-104">SYNTAX</span></span>

### <span data-ttu-id="f29d4-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f29d4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f29d4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f29d4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f29d4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f29d4-107">DESCRIPTION</span></span>
<span data-ttu-id="f29d4-108">Das Cmdlet " **Get-AzCosmosDBSqlDatabase** " Ruft die Liste aller vorhandenen CosmosDB SQL-Datenbanken für einen bestimmten ResourceGroupName, Accountname, ab und ruft eine einzelne CosmosDB-SQL-Datenbank für eine bestimmte ResourceGroupName, Accountname, DatabaseName und Containername ab.</span><span class="sxs-lookup"><span data-stu-id="f29d4-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="f29d4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f29d4-109">EXAMPLES</span></span>

### <span data-ttu-id="f29d4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f29d4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="f29d4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f29d4-111">PARAMETERS</span></span>

### <span data-ttu-id="f29d4-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="f29d4-112">-AccountName</span></span>
<span data-ttu-id="f29d4-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="f29d4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f29d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f29d4-114">-DefaultProfile</span></span>
<span data-ttu-id="f29d4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f29d4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f29d4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f29d4-116">-Name</span></span>
<span data-ttu-id="f29d4-117">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="f29d4-117">Database name.</span></span>

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

### <span data-ttu-id="f29d4-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f29d4-118">-ParentObject</span></span>
<span data-ttu-id="f29d4-119">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="f29d4-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f29d4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f29d4-120">-ResourceGroupName</span></span>
<span data-ttu-id="f29d4-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f29d4-121">Name of resource group.</span></span>

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

### <span data-ttu-id="f29d4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29d4-122">CommonParameters</span></span>
<span data-ttu-id="f29d4-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f29d4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29d4-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f29d4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29d4-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f29d4-125">INPUTS</span></span>

### <span data-ttu-id="f29d4-126">Keine</span><span class="sxs-lookup"><span data-stu-id="f29d4-126">None</span></span>

## <span data-ttu-id="f29d4-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f29d4-127">OUTPUTS</span></span>

### <span data-ttu-id="f29d4-128">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f29d4-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="f29d4-129">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f29d4-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f29d4-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f29d4-130">NOTES</span></span>

## <span data-ttu-id="f29d4-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f29d4-131">RELATED LINKS</span></span>
