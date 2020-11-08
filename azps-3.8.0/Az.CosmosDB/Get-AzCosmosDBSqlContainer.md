---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 89a48ecb4b167919562428e1116d95bb1e3d6390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004314"
---
# <span data-ttu-id="53381-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="53381-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="53381-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53381-102">SYNOPSIS</span></span>
<span data-ttu-id="53381-103">Ruft den CosmosDB-SQL-Container ab.</span><span class="sxs-lookup"><span data-stu-id="53381-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="53381-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53381-104">SYNTAX</span></span>

### <span data-ttu-id="53381-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="53381-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="53381-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53381-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -InputObject <PSSqlDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53381-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53381-107">DESCRIPTION</span></span>
<span data-ttu-id="53381-108">Das Cmdlet " **Get-AzCosmosDBSqlContainer** " Ruft die Liste aller vorhandenen CosmosDB SQL-Container für einen angegebenen ResourceGroupName, Accountname und DATABASENAME ab und Ruft einen einzelnen CosmosDB-SQL-Container für einen bestimmten ResourceGroupName, "Accountname", "DatabaseName" und "Container Name" ab.</span><span class="sxs-lookup"><span data-stu-id="53381-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="53381-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53381-109">EXAMPLES</span></span>

### <span data-ttu-id="53381-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53381-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="53381-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="53381-111">PARAMETERS</span></span>

### <span data-ttu-id="53381-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="53381-112">-AccountName</span></span>
<span data-ttu-id="53381-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="53381-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="53381-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="53381-114">-DatabaseName</span></span>
<span data-ttu-id="53381-115">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="53381-115">Database name.</span></span>

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

### <span data-ttu-id="53381-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53381-116">-DefaultProfile</span></span>
<span data-ttu-id="53381-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53381-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53381-118">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="53381-118">-Detailed</span></span>
<span data-ttu-id="53381-119">Wenn Sie dann bereitgestellt werden, gibt das Cmdlet den Container mit dem Durchsatz zurück.</span><span class="sxs-lookup"><span data-stu-id="53381-119">If provided then, the cmdlet returns the container with the throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53381-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="53381-120">-InputObject</span></span>
<span data-ttu-id="53381-121">SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="53381-121">Sql Database object.</span></span>

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

### <span data-ttu-id="53381-122">-Name</span><span class="sxs-lookup"><span data-stu-id="53381-122">-Name</span></span>
<span data-ttu-id="53381-123">Container Name.</span><span class="sxs-lookup"><span data-stu-id="53381-123">Container name.</span></span>

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

### <span data-ttu-id="53381-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53381-124">-ResourceGroupName</span></span>
<span data-ttu-id="53381-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="53381-125">Name of resource group.</span></span>

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

### <span data-ttu-id="53381-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53381-126">CommonParameters</span></span>
<span data-ttu-id="53381-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53381-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53381-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53381-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53381-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53381-129">INPUTS</span></span>

### <span data-ttu-id="53381-130">Keine</span><span class="sxs-lookup"><span data-stu-id="53381-130">None</span></span>

## <span data-ttu-id="53381-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53381-131">OUTPUTS</span></span>

### <span data-ttu-id="53381-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="53381-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="53381-133">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="53381-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="53381-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="53381-134">NOTES</span></span>

## <span data-ttu-id="53381-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53381-135">RELATED LINKS</span></span>
