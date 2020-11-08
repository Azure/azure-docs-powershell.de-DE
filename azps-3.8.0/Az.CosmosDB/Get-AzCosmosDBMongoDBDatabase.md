---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: f1cb4a45a68758dc1209b4e30d352def8e348e9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004312"
---
# <span data-ttu-id="63282-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="63282-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="63282-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63282-102">SYNOPSIS</span></span>
<span data-ttu-id="63282-103">Ruft die CosmosDB MongoDB-Datenbank ab</span><span class="sxs-lookup"><span data-stu-id="63282-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="63282-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63282-104">SYNTAX</span></span>

### <span data-ttu-id="63282-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="63282-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63282-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63282-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63282-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63282-107">DESCRIPTION</span></span>
<span data-ttu-id="63282-108">Das Cmdlet " **Get-AzCosmosDBMongoDBDatabase** " Ruft die CosmosDB MongoDB-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="63282-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="63282-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63282-109">EXAMPLES</span></span>

### <span data-ttu-id="63282-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="63282-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="63282-111">Das Ressourcenobjekt enthält _rid, _ts, _etag Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="63282-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="63282-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="63282-112">PARAMETERS</span></span>

### <span data-ttu-id="63282-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="63282-113">-AccountName</span></span>
<span data-ttu-id="63282-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="63282-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="63282-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63282-115">-DefaultProfile</span></span>
<span data-ttu-id="63282-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="63282-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63282-117">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="63282-117">-Detailed</span></span>
<span data-ttu-id="63282-118">Wenn Sie dann bereitgestellt werden, gibt das Cmdlet die Datenbank mit dem entsprechenden Durchsatz zurück.</span><span class="sxs-lookup"><span data-stu-id="63282-118">If provided then, the cmdlet returns the database with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="63282-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="63282-119">-InputObject</span></span>
<span data-ttu-id="63282-120">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="63282-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63282-121">-Name</span><span class="sxs-lookup"><span data-stu-id="63282-121">-Name</span></span>
<span data-ttu-id="63282-122">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="63282-122">Database name.</span></span>

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

### <span data-ttu-id="63282-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63282-123">-ResourceGroupName</span></span>
<span data-ttu-id="63282-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="63282-124">Name of resource group.</span></span>

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

### <span data-ttu-id="63282-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63282-125">CommonParameters</span></span>
<span data-ttu-id="63282-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63282-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63282-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63282-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63282-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63282-128">INPUTS</span></span>

### <span data-ttu-id="63282-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="63282-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="63282-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63282-130">OUTPUTS</span></span>

### <span data-ttu-id="63282-131">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="63282-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="63282-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="63282-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="63282-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="63282-133">NOTES</span></span>

## <span data-ttu-id="63282-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63282-134">RELATED LINKS</span></span>
