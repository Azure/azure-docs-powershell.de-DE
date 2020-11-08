---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 21a32bc2c3251d0069dcdb05d9eea29c52207ae8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004336"
---
# <span data-ttu-id="7a362-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="7a362-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="7a362-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a362-102">SYNOPSIS</span></span>
<span data-ttu-id="7a362-103">Ruft den Durchsatz Wert des Cassandra-keyspaces ab.</span><span class="sxs-lookup"><span data-stu-id="7a362-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="7a362-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a362-104">SYNTAX</span></span>

### <span data-ttu-id="7a362-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a362-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a362-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a362-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a362-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a362-107">DESCRIPTION</span></span>
<span data-ttu-id="7a362-108">Das Cmdlet " **Get-AzCosmosDBCassandraKeyspaceThroughput** " Ruft das Durchsatz Objekt ab, das einem angegebenen Keyspace entspricht.</span><span class="sxs-lookup"><span data-stu-id="7a362-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="7a362-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a362-109">EXAMPLES</span></span>

### <span data-ttu-id="7a362-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7a362-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="7a362-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a362-111">PARAMETERS</span></span>

### <span data-ttu-id="7a362-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="7a362-112">-AccountName</span></span>
<span data-ttu-id="7a362-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="7a362-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7a362-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a362-114">-DefaultProfile</span></span>
<span data-ttu-id="7a362-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7a362-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a362-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7a362-116">-InputObject</span></span>
<span data-ttu-id="7a362-117">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="7a362-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7a362-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7a362-118">-Name</span></span>
<span data-ttu-id="7a362-119">Cassandra-Keyspace-Name.</span><span class="sxs-lookup"><span data-stu-id="7a362-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="7a362-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a362-120">-ResourceGroupName</span></span>
<span data-ttu-id="7a362-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7a362-121">Name of resource group.</span></span>

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

### <span data-ttu-id="7a362-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a362-122">CommonParameters</span></span>
<span data-ttu-id="7a362-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a362-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a362-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a362-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a362-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a362-125">INPUTS</span></span>

### <span data-ttu-id="7a362-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7a362-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="7a362-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a362-127">OUTPUTS</span></span>

### <span data-ttu-id="7a362-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7a362-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7a362-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a362-129">NOTES</span></span>

## <span data-ttu-id="7a362-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a362-130">RELATED LINKS</span></span>
