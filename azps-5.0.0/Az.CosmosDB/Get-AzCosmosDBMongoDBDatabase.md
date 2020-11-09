---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299517"
---
# <span data-ttu-id="554b4-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="554b4-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="554b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="554b4-102">SYNOPSIS</span></span>
<span data-ttu-id="554b4-103">Ruft die CosmosDB MongoDB-Datenbank ab</span><span class="sxs-lookup"><span data-stu-id="554b4-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="554b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="554b4-104">SYNTAX</span></span>

### <span data-ttu-id="554b4-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="554b4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="554b4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="554b4-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="554b4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="554b4-107">DESCRIPTION</span></span>
<span data-ttu-id="554b4-108">Das Cmdlet " **Get-AzCosmosDBMongoDBDatabase** " Ruft die CosmosDB MongoDB-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="554b4-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="554b4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="554b4-109">EXAMPLES</span></span>

### <span data-ttu-id="554b4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="554b4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="554b4-111">Das Ressourcenobjekt enthält _rid, _ts, _etag Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="554b4-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="554b4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="554b4-112">PARAMETERS</span></span>

### <span data-ttu-id="554b4-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="554b4-113">-AccountName</span></span>
<span data-ttu-id="554b4-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="554b4-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="554b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="554b4-115">-DefaultProfile</span></span>
<span data-ttu-id="554b4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="554b4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="554b4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="554b4-117">-Name</span></span>
<span data-ttu-id="554b4-118">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="554b4-118">Database name.</span></span>

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

### <span data-ttu-id="554b4-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="554b4-119">-ParentObject</span></span>
<span data-ttu-id="554b4-120">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="554b4-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="554b4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="554b4-121">-ResourceGroupName</span></span>
<span data-ttu-id="554b4-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="554b4-122">Name of resource group.</span></span>

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

### <span data-ttu-id="554b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="554b4-123">CommonParameters</span></span>
<span data-ttu-id="554b4-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="554b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="554b4-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="554b4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="554b4-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="554b4-126">INPUTS</span></span>

### <span data-ttu-id="554b4-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="554b4-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="554b4-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="554b4-128">OUTPUTS</span></span>

### <span data-ttu-id="554b4-129">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="554b4-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="554b4-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="554b4-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="554b4-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="554b4-131">NOTES</span></span>

## <span data-ttu-id="554b4-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="554b4-132">RELATED LINKS</span></span>
