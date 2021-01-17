---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472854"
---
# <span data-ttu-id="69749-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="69749-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="69749-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69749-102">SYNOPSIS</span></span>
<span data-ttu-id="69749-103">Ruft die Datenbank "DesDb MongoDB" ab</span><span class="sxs-lookup"><span data-stu-id="69749-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="69749-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69749-104">SYNTAX</span></span>

### <span data-ttu-id="69749-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="69749-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69749-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69749-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69749-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69749-107">DESCRIPTION</span></span>
<span data-ttu-id="69749-108">Das **Cmdlet "Get-AzCosmosDBMongoDBDatabase"** ruft die Datenbank "BasesDB MongoDB" ab.</span><span class="sxs-lookup"><span data-stu-id="69749-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="69749-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69749-109">EXAMPLES</span></span>

### <span data-ttu-id="69749-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69749-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="69749-111">Das Ressourcenobjekt enthält _rid, _ts und _etag Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="69749-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="69749-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69749-112">PARAMETERS</span></span>

### <span data-ttu-id="69749-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="69749-113">-AccountName</span></span>
<span data-ttu-id="69749-114">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="69749-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="69749-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69749-115">-DefaultProfile</span></span>
<span data-ttu-id="69749-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69749-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69749-117">-Name</span><span class="sxs-lookup"><span data-stu-id="69749-117">-Name</span></span>
<span data-ttu-id="69749-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="69749-118">Database name.</span></span>

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

### <span data-ttu-id="69749-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="69749-119">-ParentObject</span></span>
<span data-ttu-id="69749-120">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="69749-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69749-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69749-121">-ResourceGroupName</span></span>
<span data-ttu-id="69749-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="69749-122">Name of resource group.</span></span>

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

### <span data-ttu-id="69749-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69749-123">CommonParameters</span></span>
<span data-ttu-id="69749-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69749-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69749-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69749-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69749-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69749-126">INPUTS</span></span>

### <span data-ttu-id="69749-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="69749-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="69749-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69749-128">OUTPUTS</span></span>

### <span data-ttu-id="69749-129">Microsoft.Azure.Commands.ExesDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="69749-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="69749-130">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="69749-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="69749-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="69749-131">NOTES</span></span>

## <span data-ttu-id="69749-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="69749-132">RELATED LINKS</span></span>
