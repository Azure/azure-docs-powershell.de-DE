---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: f1fb191a235cdf1c98768d3201cab49278f4403c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922040"
---
# <span data-ttu-id="22478-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="22478-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="22478-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22478-102">SYNOPSIS</span></span>
<span data-ttu-id="22478-103">Ruft die CosmosDB Sql StoredProcedure ab.</span><span class="sxs-lookup"><span data-stu-id="22478-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="22478-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22478-104">SYNTAX</span></span>

### <span data-ttu-id="22478-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="22478-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22478-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22478-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22478-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22478-107">DESCRIPTION</span></span>
<span data-ttu-id="22478-108">Das **Get-AzCosmosDBSqlStoredProcedure-Cmdlet** ruft die Liste aller vorhandenen CosmosDB Sql StoredProcedures für einen bestimmten ResourceGroupName, AccountName, DatabaseName und ContainerName ab und ruft eine einzelne CosmosDB Sql StoredProcedure für einen bestimmten ResourceGroupName, AccountName, DatabaseName, ContainerName und StoredProcedureName ab.</span><span class="sxs-lookup"><span data-stu-id="22478-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="22478-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22478-109">EXAMPLES</span></span>

### <span data-ttu-id="22478-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22478-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="22478-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="22478-111">PARAMETERS</span></span>

### <span data-ttu-id="22478-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22478-112">-AccountName</span></span>
<span data-ttu-id="22478-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="22478-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="22478-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="22478-114">-ContainerName</span></span>
<span data-ttu-id="22478-115">Containername.</span><span class="sxs-lookup"><span data-stu-id="22478-115">Container name.</span></span>

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

### <span data-ttu-id="22478-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="22478-116">-DatabaseName</span></span>
<span data-ttu-id="22478-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="22478-117">Database name.</span></span>

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

### <span data-ttu-id="22478-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22478-118">-DefaultProfile</span></span>
<span data-ttu-id="22478-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22478-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22478-120">-Name</span><span class="sxs-lookup"><span data-stu-id="22478-120">-Name</span></span>
<span data-ttu-id="22478-121">Gespeicherter Prcodecure-Name.</span><span class="sxs-lookup"><span data-stu-id="22478-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="22478-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="22478-122">-ParentObject</span></span>
<span data-ttu-id="22478-123">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="22478-123">Sql Container object.</span></span>

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

### <span data-ttu-id="22478-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22478-124">-ResourceGroupName</span></span>
<span data-ttu-id="22478-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="22478-125">Name of resource group.</span></span>

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

### <span data-ttu-id="22478-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22478-126">CommonParameters</span></span>
<span data-ttu-id="22478-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22478-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22478-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22478-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22478-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22478-129">INPUTS</span></span>

### <span data-ttu-id="22478-130">Keine</span><span class="sxs-lookup"><span data-stu-id="22478-130">None</span></span>

## <span data-ttu-id="22478-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22478-131">OUTPUTS</span></span>

### <span data-ttu-id="22478-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="22478-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="22478-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="22478-133">NOTES</span></span>

## <span data-ttu-id="22478-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="22478-134">RELATED LINKS</span></span>
