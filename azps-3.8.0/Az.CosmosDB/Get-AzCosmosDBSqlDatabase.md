---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 5efdbc3f1f8172ba59a78d4ec462f57a527faf07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847336"
---
# <span data-ttu-id="7674b-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7674b-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="7674b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7674b-102">SYNOPSIS</span></span>
<span data-ttu-id="7674b-103">Ruft die CosmosDB-SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="7674b-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="7674b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7674b-104">SYNTAX</span></span>

### <span data-ttu-id="7674b-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7674b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7674b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7674b-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7674b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7674b-107">DESCRIPTION</span></span>
<span data-ttu-id="7674b-108">Das Cmdlet " **Get-AzCosmosDBSqlDatabase** " Ruft die Liste aller vorhandenen CosmosDB SQL-Datenbanken für einen bestimmten ResourceGroupName, Accountname, ab und ruft eine einzelne CosmosDB-SQL-Datenbank für eine bestimmte ResourceGroupName, Accountname, DatabaseName und Containername ab.</span><span class="sxs-lookup"><span data-stu-id="7674b-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="7674b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7674b-109">EXAMPLES</span></span>

### <span data-ttu-id="7674b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7674b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="7674b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7674b-111">PARAMETERS</span></span>

### <span data-ttu-id="7674b-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="7674b-112">-AccountName</span></span>
<span data-ttu-id="7674b-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="7674b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7674b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7674b-114">-DefaultProfile</span></span>
<span data-ttu-id="7674b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7674b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7674b-116">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="7674b-116">-Detailed</span></span>
<span data-ttu-id="7674b-117">Wenn Sie dann bereitgestellt werden, gibt das Cmdlet den Container mit dem Durchsatz zurück.</span><span class="sxs-lookup"><span data-stu-id="7674b-117">If provided then, the cmdlet returns the container with the throughput value.</span></span>

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

### <span data-ttu-id="7674b-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7674b-118">-InputObject</span></span>
<span data-ttu-id="7674b-119">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="7674b-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7674b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7674b-120">-Name</span></span>
<span data-ttu-id="7674b-121">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="7674b-121">Database name.</span></span>

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

### <span data-ttu-id="7674b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7674b-122">-ResourceGroupName</span></span>
<span data-ttu-id="7674b-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7674b-123">Name of resource group.</span></span>

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

### <span data-ttu-id="7674b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7674b-124">CommonParameters</span></span>
<span data-ttu-id="7674b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7674b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7674b-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7674b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7674b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7674b-127">INPUTS</span></span>

### <span data-ttu-id="7674b-128">Keine</span><span class="sxs-lookup"><span data-stu-id="7674b-128">None</span></span>

## <span data-ttu-id="7674b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7674b-129">OUTPUTS</span></span>

### <span data-ttu-id="7674b-130">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7674b-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="7674b-131">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7674b-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7674b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="7674b-132">NOTES</span></span>

## <span data-ttu-id="7674b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7674b-133">RELATED LINKS</span></span>
