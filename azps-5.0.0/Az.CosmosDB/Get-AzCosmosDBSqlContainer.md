---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299506"
---
# <span data-ttu-id="c3a1e-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="c3a1e-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="c3a1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="c3a1e-103">Ruft den CosmosDB-SQL-Container ab.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="c3a1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3a1e-104">SYNTAX</span></span>

### <span data-ttu-id="c3a1e-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3a1e-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="c3a1e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3a1e-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3a1e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3a1e-107">DESCRIPTION</span></span>
<span data-ttu-id="c3a1e-108">Das Cmdlet " **Get-AzCosmosDBSqlContainer** " Ruft die Liste aller vorhandenen CosmosDB SQL-Container für einen angegebenen ResourceGroupName, Accountname und DATABASENAME ab und Ruft einen einzelnen CosmosDB-SQL-Container für einen bestimmten ResourceGroupName, "Accountname", "DatabaseName" und "Container Name" ab.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="c3a1e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3a1e-109">EXAMPLES</span></span>

### <span data-ttu-id="c3a1e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3a1e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="c3a1e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3a1e-111">PARAMETERS</span></span>

### <span data-ttu-id="c3a1e-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="c3a1e-112">-AccountName</span></span>
<span data-ttu-id="c3a1e-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c3a1e-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c3a1e-114">-DatabaseName</span></span>
<span data-ttu-id="c3a1e-115">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="c3a1e-115">Database name.</span></span>

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

### <span data-ttu-id="c3a1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3a1e-116">-DefaultProfile</span></span>
<span data-ttu-id="c3a1e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3a1e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c3a1e-118">-Name</span></span>
<span data-ttu-id="c3a1e-119">Container Name.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-119">Container name.</span></span>

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

### <span data-ttu-id="c3a1e-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c3a1e-120">-ParentObject</span></span>
<span data-ttu-id="c3a1e-121">SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-121">Sql Database object.</span></span>

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

### <span data-ttu-id="c3a1e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3a1e-122">-ResourceGroupName</span></span>
<span data-ttu-id="c3a1e-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-123">Name of resource group.</span></span>

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

### <span data-ttu-id="c3a1e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3a1e-124">CommonParameters</span></span>
<span data-ttu-id="c3a1e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3a1e-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3a1e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3a1e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3a1e-127">INPUTS</span></span>

### <span data-ttu-id="c3a1e-128">Keine</span><span class="sxs-lookup"><span data-stu-id="c3a1e-128">None</span></span>

## <span data-ttu-id="c3a1e-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3a1e-129">OUTPUTS</span></span>

### <span data-ttu-id="c3a1e-130">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="c3a1e-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="c3a1e-131">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c3a1e-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c3a1e-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3a1e-132">NOTES</span></span>

## <span data-ttu-id="c3a1e-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3a1e-133">RELATED LINKS</span></span>
