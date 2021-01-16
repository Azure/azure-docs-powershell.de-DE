---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305235"
---
# <span data-ttu-id="6f53c-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="6f53c-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="6f53c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f53c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f53c-103">Ruft die Durchsatzeinstellungen ab, die einem SkriptsDB Sql Container entspricht.</span><span class="sxs-lookup"><span data-stu-id="6f53c-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="6f53c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f53c-104">SYNTAX</span></span>

### <span data-ttu-id="6f53c-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f53c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f53c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f53c-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f53c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f53c-107">DESCRIPTION</span></span>
<span data-ttu-id="6f53c-108">Das **Cmdlet "Get-AzCosmosDBSqlContainerThroughput"** ruft die Durchsatzeinstellungen ab, die einem SkriptsDB Sql Container entspricht.</span><span class="sxs-lookup"><span data-stu-id="6f53c-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="6f53c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f53c-109">EXAMPLES</span></span>

### <span data-ttu-id="6f53c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6f53c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="6f53c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f53c-111">PARAMETERS</span></span>

### <span data-ttu-id="6f53c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6f53c-112">-AccountName</span></span>
<span data-ttu-id="6f53c-113">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="6f53c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6f53c-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6f53c-114">-DatabaseName</span></span>
<span data-ttu-id="6f53c-115">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="6f53c-115">Database name.</span></span>

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

### <span data-ttu-id="6f53c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f53c-116">-DefaultProfile</span></span>
<span data-ttu-id="6f53c-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f53c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f53c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f53c-118">-InputObject</span></span>
<span data-ttu-id="6f53c-119">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6f53c-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f53c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6f53c-120">-Name</span></span>
<span data-ttu-id="6f53c-121">Containername.</span><span class="sxs-lookup"><span data-stu-id="6f53c-121">Container name.</span></span>

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

### <span data-ttu-id="6f53c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f53c-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f53c-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6f53c-123">Name of resource group.</span></span>

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

### <span data-ttu-id="6f53c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f53c-124">CommonParameters</span></span>
<span data-ttu-id="6f53c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f53c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f53c-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f53c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f53c-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f53c-127">INPUTS</span></span>

### <span data-ttu-id="6f53c-128">Keine</span><span class="sxs-lookup"><span data-stu-id="6f53c-128">None</span></span>

## <span data-ttu-id="6f53c-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f53c-129">OUTPUTS</span></span>

### <span data-ttu-id="6f53c-130">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6f53c-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6f53c-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6f53c-131">NOTES</span></span>

## <span data-ttu-id="6f53c-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6f53c-132">RELATED LINKS</span></span>
