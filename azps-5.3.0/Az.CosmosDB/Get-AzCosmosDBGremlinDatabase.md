---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: ba1f6b1ca309226433120ea6a68ec330cabd034c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472859"
---
# <span data-ttu-id="f4895-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="f4895-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="f4895-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4895-102">SYNOPSIS</span></span>
<span data-ttu-id="f4895-103">Ruft die Datenbank DestallEndb-Gremlin ab.</span><span class="sxs-lookup"><span data-stu-id="f4895-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="f4895-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4895-104">SYNTAX</span></span>

### <span data-ttu-id="f4895-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4895-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4895-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4895-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4895-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4895-107">DESCRIPTION</span></span>
<span data-ttu-id="f4895-108">Das **Cmdlet "Get-AzCosmosDBGremlinDatabase"** ruft dieBasesDB -Gremlin-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="f4895-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="f4895-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4895-109">EXAMPLES</span></span>

### <span data-ttu-id="f4895-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4895-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="f4895-111">Das Ressourcenobjekt enthält _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="f4895-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="f4895-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4895-112">PARAMETERS</span></span>

### <span data-ttu-id="f4895-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f4895-113">-AccountName</span></span>
<span data-ttu-id="f4895-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="f4895-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f4895-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4895-115">-DefaultProfile</span></span>
<span data-ttu-id="f4895-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4895-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4895-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f4895-117">-Name</span></span>
<span data-ttu-id="f4895-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="f4895-118">Database name.</span></span>

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

### <span data-ttu-id="f4895-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f4895-119">-ParentObject</span></span>
<span data-ttu-id="f4895-120">Objekt "Buchhalterungskonto"</span><span class="sxs-lookup"><span data-stu-id="f4895-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f4895-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4895-121">-ResourceGroupName</span></span>
<span data-ttu-id="f4895-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f4895-122">Name of resource group.</span></span>

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

### <span data-ttu-id="f4895-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4895-123">CommonParameters</span></span>
<span data-ttu-id="f4895-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4895-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4895-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4895-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4895-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4895-126">INPUTS</span></span>

### <span data-ttu-id="f4895-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f4895-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="f4895-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4895-128">OUTPUTS</span></span>

### <span data-ttu-id="f4895-129">Microsoft.Azure.Commands.ExesDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f4895-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="f4895-130">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f4895-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f4895-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f4895-131">NOTES</span></span>

## <span data-ttu-id="f4895-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f4895-132">RELATED LINKS</span></span>
