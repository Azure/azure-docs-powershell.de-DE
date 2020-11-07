---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: c8cfb1077f418c9d671729cb0ff762141a7b77c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845623"
---
# <span data-ttu-id="613f6-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="613f6-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="613f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="613f6-102">SYNOPSIS</span></span>
<span data-ttu-id="613f6-103">Ruft die CosmosDB SQL-benutzerdefinierte Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="613f6-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="613f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="613f6-104">SYNTAX</span></span>

### <span data-ttu-id="613f6-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="613f6-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="613f6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="613f6-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="613f6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="613f6-107">DESCRIPTION</span></span>
<span data-ttu-id="613f6-108">Das Cmdlet " **Get-AzCosmosDBSqlUserDefinedFunction** " Ruft die Liste aller vorhandenen CosmosDB-SQL-UserDefinedFunctions für eine bestimmte ResourceGroupName, Accountname, DatabaseName und Containername ab und Ruft einen einzelnen CosmosDB-SQL-UserDefinedFunction für eine bestimmte ResourceGroupName, "Accountname", "DatabaseName", "Containername" und "UserDefinedFunctionName" ab.</span><span class="sxs-lookup"><span data-stu-id="613f6-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="613f6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="613f6-109">EXAMPLES</span></span>

### <span data-ttu-id="613f6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="613f6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="613f6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="613f6-111">PARAMETERS</span></span>

### <span data-ttu-id="613f6-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="613f6-112">-AccountName</span></span>
<span data-ttu-id="613f6-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="613f6-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="613f6-114">-Containername</span><span class="sxs-lookup"><span data-stu-id="613f6-114">-ContainerName</span></span>
<span data-ttu-id="613f6-115">Container Name.</span><span class="sxs-lookup"><span data-stu-id="613f6-115">Container name.</span></span>

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

### <span data-ttu-id="613f6-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="613f6-116">-DatabaseName</span></span>
<span data-ttu-id="613f6-117">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="613f6-117">Database name.</span></span>

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

### <span data-ttu-id="613f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="613f6-118">-DefaultProfile</span></span>
<span data-ttu-id="613f6-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="613f6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="613f6-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="613f6-120">-InputObject</span></span>
<span data-ttu-id="613f6-121">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="613f6-121">Sql Container object.</span></span>

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

### <span data-ttu-id="613f6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="613f6-122">-Name</span></span>
<span data-ttu-id="613f6-123">Name der benutzerdefinierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="613f6-123">User Defined Function Name.</span></span>

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

### <span data-ttu-id="613f6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="613f6-124">-ResourceGroupName</span></span>
<span data-ttu-id="613f6-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="613f6-125">Name of resource group.</span></span>

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

### <span data-ttu-id="613f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="613f6-126">CommonParameters</span></span>
<span data-ttu-id="613f6-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="613f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="613f6-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="613f6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="613f6-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="613f6-129">INPUTS</span></span>

### <span data-ttu-id="613f6-130">Keine</span><span class="sxs-lookup"><span data-stu-id="613f6-130">None</span></span>

## <span data-ttu-id="613f6-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="613f6-131">OUTPUTS</span></span>

### <span data-ttu-id="613f6-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="613f6-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="613f6-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="613f6-133">NOTES</span></span>

## <span data-ttu-id="613f6-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="613f6-134">RELATED LINKS</span></span>
