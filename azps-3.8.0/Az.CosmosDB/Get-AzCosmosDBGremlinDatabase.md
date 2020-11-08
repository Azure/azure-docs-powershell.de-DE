---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 52a889ea454b5752be25ecd216f9a20e4b830b52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004331"
---
# <span data-ttu-id="78959-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="78959-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="78959-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78959-102">SYNOPSIS</span></span>
<span data-ttu-id="78959-103">Ruft die CosmosDB Gremlin-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="78959-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="78959-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78959-104">SYNTAX</span></span>

### <span data-ttu-id="78959-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="78959-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78959-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78959-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78959-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78959-107">DESCRIPTION</span></span>
<span data-ttu-id="78959-108">Das Cmdlet " **Get-AzCosmosDBGremlinDatabase** " Ruft die CosmosDB Gremlin-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="78959-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="78959-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78959-109">EXAMPLES</span></span>

### <span data-ttu-id="78959-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78959-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="78959-111">Das Ressourcenobjekt enthält _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="78959-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="78959-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="78959-112">PARAMETERS</span></span>

### <span data-ttu-id="78959-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="78959-113">-AccountName</span></span>
<span data-ttu-id="78959-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="78959-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="78959-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78959-115">-DefaultProfile</span></span>
<span data-ttu-id="78959-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78959-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78959-117">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="78959-117">-Detailed</span></span>
<span data-ttu-id="78959-118">Wenn Sie dann bereitgestellt werden, gibt das Cmdlet die Datenbank mit dem entsprechenden Durchsatz zurück.</span><span class="sxs-lookup"><span data-stu-id="78959-118">If provided then, the cmdlet returns the Database with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78959-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="78959-119">-InputObject</span></span>
<span data-ttu-id="78959-120">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="78959-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78959-121">-Name</span><span class="sxs-lookup"><span data-stu-id="78959-121">-Name</span></span>
<span data-ttu-id="78959-122">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="78959-122">Database name.</span></span>

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

### <span data-ttu-id="78959-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78959-123">-ResourceGroupName</span></span>
<span data-ttu-id="78959-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78959-124">Name of resource group.</span></span>

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

### <span data-ttu-id="78959-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78959-125">CommonParameters</span></span>
<span data-ttu-id="78959-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78959-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78959-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78959-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78959-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78959-128">INPUTS</span></span>

### <span data-ttu-id="78959-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="78959-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="78959-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78959-130">OUTPUTS</span></span>

### <span data-ttu-id="78959-131">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="78959-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="78959-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="78959-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="78959-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="78959-133">NOTES</span></span>

## <span data-ttu-id="78959-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78959-134">RELATED LINKS</span></span>
