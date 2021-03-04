---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 5bf35b43db1f1d961f24c1aa2c75c9f17c333345
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922043"
---
# <span data-ttu-id="9c034-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="9c034-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="9c034-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c034-102">SYNOPSIS</span></span>
<span data-ttu-id="9c034-103">Ruft die Durchsatzeinstellungen ab, die einer CosmosDB-Sql-Datenbank entspricht.</span><span class="sxs-lookup"><span data-stu-id="9c034-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="9c034-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c034-104">SYNTAX</span></span>

### <span data-ttu-id="9c034-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9c034-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c034-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c034-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c034-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c034-107">DESCRIPTION</span></span>
<span data-ttu-id="9c034-108">Das **Cmdlet Get-AzCosmosDBSqlDatabaseThroughput** ruft die Durchsatzeinstellungen ab, die einer CosmosDB Sql-Datenbank entspricht.</span><span class="sxs-lookup"><span data-stu-id="9c034-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="9c034-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9c034-109">EXAMPLES</span></span>

### <span data-ttu-id="9c034-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9c034-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="9c034-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9c034-111">PARAMETERS</span></span>

### <span data-ttu-id="9c034-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9c034-112">-AccountName</span></span>
<span data-ttu-id="9c034-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="9c034-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9c034-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c034-114">-DefaultProfile</span></span>
<span data-ttu-id="9c034-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c034-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c034-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c034-116">-InputObject</span></span>
<span data-ttu-id="9c034-117">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="9c034-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9c034-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9c034-118">-Name</span></span>
<span data-ttu-id="9c034-119">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="9c034-119">Database name.</span></span>

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

### <span data-ttu-id="9c034-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c034-120">-ResourceGroupName</span></span>
<span data-ttu-id="9c034-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9c034-121">Name of resource group.</span></span>

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

### <span data-ttu-id="9c034-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c034-122">CommonParameters</span></span>
<span data-ttu-id="9c034-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c034-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c034-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c034-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c034-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9c034-125">INPUTS</span></span>

### <span data-ttu-id="9c034-126">Keine</span><span class="sxs-lookup"><span data-stu-id="9c034-126">None</span></span>

## <span data-ttu-id="9c034-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9c034-127">OUTPUTS</span></span>

### <span data-ttu-id="9c034-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9c034-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9c034-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9c034-129">NOTES</span></span>

## <span data-ttu-id="9c034-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9c034-130">RELATED LINKS</span></span>
