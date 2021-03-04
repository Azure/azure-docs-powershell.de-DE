---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 0dfcffe55eb3214f4be9d6ccfb34231d1c9ea50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940571"
---
# <span data-ttu-id="8e3a5-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="8e3a5-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="8e3a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e3a5-102">SYNOPSIS</span></span>
<span data-ttu-id="8e3a5-103">Ruft die CosmosDB-MongoDB-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="8e3a5-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="8e3a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e3a5-104">SYNTAX</span></span>

### <span data-ttu-id="8e3a5-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e3a5-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e3a5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e3a5-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e3a5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e3a5-107">DESCRIPTION</span></span>
<span data-ttu-id="8e3a5-108">Das **Cmdlet Get-AzCosmosDBMongoDBDatabase** ruft die CosmosDB MongoDB-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="8e3a5-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="8e3a5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e3a5-109">EXAMPLES</span></span>

### <span data-ttu-id="8e3a5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e3a5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="8e3a5-111">Ressourcenobjekt enthält _rid-, _ts-, _etag-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8e3a5-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="8e3a5-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8e3a5-112">PARAMETERS</span></span>

### <span data-ttu-id="8e3a5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e3a5-113">-AccountName</span></span>
<span data-ttu-id="8e3a5-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="8e3a5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8e3a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e3a5-115">-DefaultProfile</span></span>
<span data-ttu-id="8e3a5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e3a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e3a5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8e3a5-117">-Name</span></span>
<span data-ttu-id="8e3a5-118">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="8e3a5-118">Database name.</span></span>

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

### <span data-ttu-id="8e3a5-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e3a5-119">-ParentObject</span></span>
<span data-ttu-id="8e3a5-120">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="8e3a5-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8e3a5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e3a5-121">-ResourceGroupName</span></span>
<span data-ttu-id="8e3a5-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e3a5-122">Name of resource group.</span></span>

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

### <span data-ttu-id="8e3a5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e3a5-123">CommonParameters</span></span>
<span data-ttu-id="8e3a5-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e3a5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e3a5-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e3a5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e3a5-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e3a5-126">INPUTS</span></span>

### <span data-ttu-id="8e3a5-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="8e3a5-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="8e3a5-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e3a5-128">OUTPUTS</span></span>

### <span data-ttu-id="8e3a5-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8e3a5-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="8e3a5-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8e3a5-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8e3a5-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8e3a5-131">NOTES</span></span>

## <span data-ttu-id="8e3a5-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8e3a5-132">RELATED LINKS</span></span>
