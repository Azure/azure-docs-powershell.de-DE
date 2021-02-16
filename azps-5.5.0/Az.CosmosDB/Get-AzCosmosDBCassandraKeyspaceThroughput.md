---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166297"
---
# <span data-ttu-id="5b6ed-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="5b6ed-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="5b6ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="5b6ed-103">Ruft den Durchsatzwert des Schlüsselspaces "Destra" ab.</span><span class="sxs-lookup"><span data-stu-id="5b6ed-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="5b6ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b6ed-104">SYNTAX</span></span>

### <span data-ttu-id="5b6ed-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b6ed-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b6ed-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b6ed-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b6ed-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b6ed-107">DESCRIPTION</span></span>
<span data-ttu-id="5b6ed-108">Das **Cmdlet "Get-AzCosmosDBCasskeyspaceThroughput"** ruft das Durchsatzobjekt ab, das einem bestimmten Keyspace entspricht.</span><span class="sxs-lookup"><span data-stu-id="5b6ed-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="5b6ed-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5b6ed-109">EXAMPLES</span></span>

### <span data-ttu-id="5b6ed-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b6ed-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="5b6ed-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b6ed-111">PARAMETERS</span></span>

### <span data-ttu-id="5b6ed-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5b6ed-112">-AccountName</span></span>
<span data-ttu-id="5b6ed-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="5b6ed-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5b6ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b6ed-114">-DefaultProfile</span></span>
<span data-ttu-id="5b6ed-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b6ed-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b6ed-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b6ed-116">-InputObject</span></span>
<span data-ttu-id="5b6ed-117">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="5b6ed-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5b6ed-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5b6ed-118">-Name</span></span>
<span data-ttu-id="5b6ed-119">Der Name des Schlüsselraums.</span><span class="sxs-lookup"><span data-stu-id="5b6ed-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5b6ed-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b6ed-120">-ResourceGroupName</span></span>
<span data-ttu-id="5b6ed-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5b6ed-121">Name of resource group.</span></span>

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

### <span data-ttu-id="5b6ed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b6ed-122">CommonParameters</span></span>
<span data-ttu-id="5b6ed-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b6ed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b6ed-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b6ed-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b6ed-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5b6ed-125">INPUTS</span></span>

### <span data-ttu-id="5b6ed-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5b6ed-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5b6ed-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5b6ed-127">OUTPUTS</span></span>

### <span data-ttu-id="5b6ed-128">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5b6ed-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5b6ed-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5b6ed-129">NOTES</span></span>

## <span data-ttu-id="5b6ed-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5b6ed-130">RELATED LINKS</span></span>
