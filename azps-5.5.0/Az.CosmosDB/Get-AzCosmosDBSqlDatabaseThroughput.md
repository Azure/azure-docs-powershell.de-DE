---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166233"
---
# <span data-ttu-id="063e4-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="063e4-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="063e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="063e4-102">SYNOPSIS</span></span>
<span data-ttu-id="063e4-103">Ruft die Durchsatzeinstellungen ab, die einer Datenbank des 1.</span><span class="sxs-lookup"><span data-stu-id="063e4-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="063e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="063e4-104">SYNTAX</span></span>

### <span data-ttu-id="063e4-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="063e4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="063e4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="063e4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="063e4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="063e4-107">DESCRIPTION</span></span>
<span data-ttu-id="063e4-108">Das **Cmdlet "Get-AzCosmosDBSqlDatabaseThroughput"** ruft die Durchsatzeinstellungen ab, die einerBasesDB -Sql-Datenbank entspricht.</span><span class="sxs-lookup"><span data-stu-id="063e4-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="063e4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="063e4-109">EXAMPLES</span></span>

### <span data-ttu-id="063e4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="063e4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="063e4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="063e4-111">PARAMETERS</span></span>

### <span data-ttu-id="063e4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="063e4-112">-AccountName</span></span>
<span data-ttu-id="063e4-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="063e4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="063e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="063e4-114">-DefaultProfile</span></span>
<span data-ttu-id="063e4-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="063e4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="063e4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="063e4-116">-InputObject</span></span>
<span data-ttu-id="063e4-117">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="063e4-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="063e4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="063e4-118">-Name</span></span>
<span data-ttu-id="063e4-119">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="063e4-119">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="063e4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="063e4-120">-ResourceGroupName</span></span>
<span data-ttu-id="063e4-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="063e4-121">Name of resource group.</span></span>

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

### <span data-ttu-id="063e4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="063e4-122">CommonParameters</span></span>
<span data-ttu-id="063e4-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="063e4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="063e4-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="063e4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="063e4-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="063e4-125">INPUTS</span></span>

### <span data-ttu-id="063e4-126">Keine</span><span class="sxs-lookup"><span data-stu-id="063e4-126">None</span></span>

## <span data-ttu-id="063e4-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="063e4-127">OUTPUTS</span></span>

### <span data-ttu-id="063e4-128">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="063e4-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="063e4-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="063e4-129">NOTES</span></span>

## <span data-ttu-id="063e4-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="063e4-130">RELATED LINKS</span></span>
