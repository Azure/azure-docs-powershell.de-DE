---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148625"
---
# <span data-ttu-id="24866-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="24866-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="24866-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24866-102">SYNOPSIS</span></span>
<span data-ttu-id="24866-103">Ruft die Datenbank "Tondb MongoDB" ab</span><span class="sxs-lookup"><span data-stu-id="24866-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="24866-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24866-104">SYNTAX</span></span>

### <span data-ttu-id="24866-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="24866-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24866-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24866-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24866-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24866-107">DESCRIPTION</span></span>
<span data-ttu-id="24866-108">Das **Cmdlet "Get-AzCosmosDBMongoDBDatabase"** ruft die Datenbank "BasesDB MongoDB" ab.</span><span class="sxs-lookup"><span data-stu-id="24866-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="24866-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="24866-109">EXAMPLES</span></span>

### <span data-ttu-id="24866-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="24866-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="24866-111">Das Ressourcenobjekt enthält _rid, _ts und _etag Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="24866-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="24866-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24866-112">PARAMETERS</span></span>

### <span data-ttu-id="24866-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24866-113">-AccountName</span></span>
<span data-ttu-id="24866-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="24866-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="24866-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24866-115">-DefaultProfile</span></span>
<span data-ttu-id="24866-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24866-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24866-117">-Name</span><span class="sxs-lookup"><span data-stu-id="24866-117">-Name</span></span>
<span data-ttu-id="24866-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="24866-118">Database name.</span></span>

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

### <span data-ttu-id="24866-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="24866-119">-ParentObject</span></span>
<span data-ttu-id="24866-120">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="24866-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="24866-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24866-121">-ResourceGroupName</span></span>
<span data-ttu-id="24866-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="24866-122">Name of resource group.</span></span>

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

### <span data-ttu-id="24866-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24866-123">CommonParameters</span></span>
<span data-ttu-id="24866-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24866-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24866-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24866-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24866-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="24866-126">INPUTS</span></span>

### <span data-ttu-id="24866-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="24866-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="24866-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="24866-128">OUTPUTS</span></span>

### <span data-ttu-id="24866-129">Microsoft.Azure.Commands.ExesDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="24866-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="24866-130">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="24866-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="24866-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="24866-131">NOTES</span></span>

## <span data-ttu-id="24866-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="24866-132">RELATED LINKS</span></span>
