---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: 3ceb7ccbb789c21fc0fdb51244260e6a54b3e900
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943083"
---
# <span data-ttu-id="cb8b2-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="cb8b2-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="cb8b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb8b2-102">SYNOPSIS</span></span>
<span data-ttu-id="cb8b2-103">Ruft die Durchsatzeinstellungen ab, die einem CosmosDB Sql Container entspricht.</span><span class="sxs-lookup"><span data-stu-id="cb8b2-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="cb8b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb8b2-104">SYNTAX</span></span>

### <span data-ttu-id="cb8b2-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb8b2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb8b2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb8b2-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb8b2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb8b2-107">DESCRIPTION</span></span>
<span data-ttu-id="cb8b2-108">Das **Cmdlet Get-AzCosmosDBSqlContainerThroughput** ruft die Durchsatzeinstellungen ab, die einem CosmosDB Sql Container entspricht.</span><span class="sxs-lookup"><span data-stu-id="cb8b2-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="cb8b2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cb8b2-109">EXAMPLES</span></span>

### <span data-ttu-id="cb8b2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cb8b2-110">Example 1</span></span>
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

## <span data-ttu-id="cb8b2-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cb8b2-111">PARAMETERS</span></span>

### <span data-ttu-id="cb8b2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cb8b2-112">-AccountName</span></span>
<span data-ttu-id="cb8b2-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="cb8b2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cb8b2-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cb8b2-114">-DatabaseName</span></span>
<span data-ttu-id="cb8b2-115">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="cb8b2-115">Database name.</span></span>

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

### <span data-ttu-id="cb8b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb8b2-116">-DefaultProfile</span></span>
<span data-ttu-id="cb8b2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb8b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb8b2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb8b2-118">-InputObject</span></span>
<span data-ttu-id="cb8b2-119">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cb8b2-119">Sql Container object.</span></span>

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

### <span data-ttu-id="cb8b2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cb8b2-120">-Name</span></span>
<span data-ttu-id="cb8b2-121">Containername.</span><span class="sxs-lookup"><span data-stu-id="cb8b2-121">Container name.</span></span>

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

### <span data-ttu-id="cb8b2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb8b2-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb8b2-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cb8b2-123">Name of resource group.</span></span>

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

### <span data-ttu-id="cb8b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb8b2-124">CommonParameters</span></span>
<span data-ttu-id="cb8b2-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb8b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb8b2-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb8b2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb8b2-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cb8b2-127">INPUTS</span></span>

### <span data-ttu-id="cb8b2-128">Keine</span><span class="sxs-lookup"><span data-stu-id="cb8b2-128">None</span></span>

## <span data-ttu-id="cb8b2-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cb8b2-129">OUTPUTS</span></span>

### <span data-ttu-id="cb8b2-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="cb8b2-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="cb8b2-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cb8b2-131">NOTES</span></span>

## <span data-ttu-id="cb8b2-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cb8b2-132">RELATED LINKS</span></span>
