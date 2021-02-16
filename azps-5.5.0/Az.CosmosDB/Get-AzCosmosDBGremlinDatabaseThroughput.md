---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 8905f4e4ffc4268b74ce57bfaf1bcb14565f70fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166268"
---
# <span data-ttu-id="4ee71-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="4ee71-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="4ee71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ee71-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee71-103">Ruft den Durchsatz einer Durchsatzdatei von "Db Gremlin"-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="4ee71-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="4ee71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ee71-104">SYNTAX</span></span>

### <span data-ttu-id="4ee71-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ee71-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ee71-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ee71-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ee71-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ee71-107">DESCRIPTION</span></span>
<span data-ttu-id="4ee71-108">Das **Cmdlet "Get-AzCosmosDBGremlinDatabaseThroughput"** ruft den Durchsatz einerBasesDB-Gremlin-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="4ee71-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="4ee71-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ee71-109">EXAMPLES</span></span>

### <span data-ttu-id="4ee71-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ee71-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="4ee71-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ee71-111">PARAMETERS</span></span>

### <span data-ttu-id="4ee71-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4ee71-112">-AccountName</span></span>
<span data-ttu-id="4ee71-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="4ee71-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4ee71-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee71-114">-DefaultProfile</span></span>
<span data-ttu-id="4ee71-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ee71-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ee71-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ee71-116">-InputObject</span></span>
<span data-ttu-id="4ee71-117">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="4ee71-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee71-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4ee71-118">-Name</span></span>
<span data-ttu-id="4ee71-119">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="4ee71-119">Database name.</span></span>

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

### <span data-ttu-id="4ee71-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee71-120">-ResourceGroupName</span></span>
<span data-ttu-id="4ee71-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4ee71-121">Name of resource group.</span></span>

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

### <span data-ttu-id="4ee71-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee71-122">CommonParameters</span></span>
<span data-ttu-id="4ee71-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee71-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee71-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ee71-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee71-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ee71-125">INPUTS</span></span>

### <span data-ttu-id="4ee71-126">Keine</span><span class="sxs-lookup"><span data-stu-id="4ee71-126">None</span></span>

## <span data-ttu-id="4ee71-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ee71-127">OUTPUTS</span></span>

### <span data-ttu-id="4ee71-128">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4ee71-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4ee71-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4ee71-129">NOTES</span></span>

## <span data-ttu-id="4ee71-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4ee71-130">RELATED LINKS</span></span>
