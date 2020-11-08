---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 8905f4e4ffc4268b74ce57bfaf1bcb14565f70fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009967"
---
# <span data-ttu-id="8b6bc-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="8b6bc-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="8b6bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b6bc-102">SYNOPSIS</span></span>
<span data-ttu-id="8b6bc-103">Ruft den Durchsatz einer CosmosDB Gremlin-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="8b6bc-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="8b6bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b6bc-104">SYNTAX</span></span>

### <span data-ttu-id="8b6bc-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b6bc-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b6bc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b6bc-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b6bc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b6bc-107">DESCRIPTION</span></span>
<span data-ttu-id="8b6bc-108">Das Cmdlet " **Get-AzCosmosDBGremlinDatabaseThroughput** " Ruft den Durchsatz einer CosmosDB Gremlin-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="8b6bc-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="8b6bc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b6bc-109">EXAMPLES</span></span>

### <span data-ttu-id="8b6bc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b6bc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="8b6bc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b6bc-111">PARAMETERS</span></span>

### <span data-ttu-id="8b6bc-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="8b6bc-112">-AccountName</span></span>
<span data-ttu-id="8b6bc-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="8b6bc-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8b6bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b6bc-114">-DefaultProfile</span></span>
<span data-ttu-id="8b6bc-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b6bc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b6bc-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8b6bc-116">-InputObject</span></span>
<span data-ttu-id="8b6bc-117">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="8b6bc-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8b6bc-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8b6bc-118">-Name</span></span>
<span data-ttu-id="8b6bc-119">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="8b6bc-119">Database name.</span></span>

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

### <span data-ttu-id="8b6bc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b6bc-120">-ResourceGroupName</span></span>
<span data-ttu-id="8b6bc-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8b6bc-121">Name of resource group.</span></span>

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

### <span data-ttu-id="8b6bc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b6bc-122">CommonParameters</span></span>
<span data-ttu-id="8b6bc-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b6bc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b6bc-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b6bc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b6bc-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b6bc-125">INPUTS</span></span>

### <span data-ttu-id="8b6bc-126">Keine</span><span class="sxs-lookup"><span data-stu-id="8b6bc-126">None</span></span>

## <span data-ttu-id="8b6bc-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b6bc-127">OUTPUTS</span></span>

### <span data-ttu-id="8b6bc-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8b6bc-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8b6bc-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b6bc-129">NOTES</span></span>

## <span data-ttu-id="8b6bc-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b6bc-130">RELATED LINKS</span></span>
