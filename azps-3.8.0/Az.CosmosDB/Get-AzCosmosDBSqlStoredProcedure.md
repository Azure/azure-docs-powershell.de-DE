---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: a9a81336ab921ebd63b8a969be5fbf65f4b7fa14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995263"
---
# <span data-ttu-id="467bf-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="467bf-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="467bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="467bf-102">SYNOPSIS</span></span>
<span data-ttu-id="467bf-103">Ruft die CosmosDB SQL-StoredProcedure Befehlstyp.</span><span class="sxs-lookup"><span data-stu-id="467bf-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="467bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="467bf-104">SYNTAX</span></span>

### <span data-ttu-id="467bf-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="467bf-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="467bf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="467bf-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="467bf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="467bf-107">DESCRIPTION</span></span>
<span data-ttu-id="467bf-108">Das Cmdlet " **Get-AzCosmosDBSqlStoredProcedure** " Ruft die Liste aller vorhandenen CosmosDB-SQL-StoredProcedures für eine bestimmte ResourceGroupName, Accountname, DatabaseName und Containername ab und Ruft einen einzelnen CosmosDB-SQL-StoredProcedure Befehlstyp für eine bestimmte ResourceGroupName, "Accountname", "DatabaseName", "Containername" und "StoredProcedureName" ab.</span><span class="sxs-lookup"><span data-stu-id="467bf-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="467bf-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="467bf-109">EXAMPLES</span></span>

### <span data-ttu-id="467bf-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="467bf-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="467bf-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="467bf-111">PARAMETERS</span></span>

### <span data-ttu-id="467bf-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="467bf-112">-AccountName</span></span>
<span data-ttu-id="467bf-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="467bf-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="467bf-114">-Containername</span><span class="sxs-lookup"><span data-stu-id="467bf-114">-ContainerName</span></span>
<span data-ttu-id="467bf-115">Container Name.</span><span class="sxs-lookup"><span data-stu-id="467bf-115">Container name.</span></span>

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

### <span data-ttu-id="467bf-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="467bf-116">-DatabaseName</span></span>
<span data-ttu-id="467bf-117">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="467bf-117">Database name.</span></span>

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

### <span data-ttu-id="467bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467bf-118">-DefaultProfile</span></span>
<span data-ttu-id="467bf-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="467bf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="467bf-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="467bf-120">-InputObject</span></span>
<span data-ttu-id="467bf-121">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="467bf-121">Sql Container object.</span></span>

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

### <span data-ttu-id="467bf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="467bf-122">-Name</span></span>
<span data-ttu-id="467bf-123">Gespeicherter Prcodecure-Name.</span><span class="sxs-lookup"><span data-stu-id="467bf-123">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="467bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="467bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="467bf-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="467bf-125">Name of resource group.</span></span>

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

### <span data-ttu-id="467bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467bf-126">CommonParameters</span></span>
<span data-ttu-id="467bf-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="467bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467bf-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="467bf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467bf-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="467bf-129">INPUTS</span></span>

### <span data-ttu-id="467bf-130">Keine</span><span class="sxs-lookup"><span data-stu-id="467bf-130">None</span></span>

## <span data-ttu-id="467bf-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="467bf-131">OUTPUTS</span></span>

### <span data-ttu-id="467bf-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="467bf-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="467bf-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="467bf-133">NOTES</span></span>

## <span data-ttu-id="467bf-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="467bf-134">RELATED LINKS</span></span>
