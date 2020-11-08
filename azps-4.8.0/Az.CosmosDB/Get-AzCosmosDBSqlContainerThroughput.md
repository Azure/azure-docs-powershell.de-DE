---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174406"
---
# <span data-ttu-id="c10e1-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="c10e1-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="c10e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c10e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c10e1-103">Ruft die Durchsatz Einstellungen ab, die einem CosmosDB SQL-Container entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c10e1-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="c10e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c10e1-104">SYNTAX</span></span>

### <span data-ttu-id="c10e1-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c10e1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c10e1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c10e1-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c10e1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c10e1-107">DESCRIPTION</span></span>
<span data-ttu-id="c10e1-108">Das Cmdlet " **Get-AzCosmosDBSqlContainerThroughput** " Ruft die Durchsatz Einstellungen ab, die einem CosmosDB SQL-Container entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c10e1-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="c10e1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c10e1-109">EXAMPLES</span></span>

### <span data-ttu-id="c10e1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c10e1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="c10e1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c10e1-111">PARAMETERS</span></span>

### <span data-ttu-id="c10e1-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="c10e1-112">-AccountName</span></span>
<span data-ttu-id="c10e1-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="c10e1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c10e1-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c10e1-114">-DatabaseName</span></span>
<span data-ttu-id="c10e1-115">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="c10e1-115">Database name.</span></span>

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

### <span data-ttu-id="c10e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c10e1-116">-DefaultProfile</span></span>
<span data-ttu-id="c10e1-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c10e1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c10e1-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c10e1-118">-InputObject</span></span>
<span data-ttu-id="c10e1-119">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="c10e1-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c10e1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c10e1-120">-Name</span></span>
<span data-ttu-id="c10e1-121">Container Name.</span><span class="sxs-lookup"><span data-stu-id="c10e1-121">Container name.</span></span>

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

### <span data-ttu-id="c10e1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c10e1-122">-ResourceGroupName</span></span>
<span data-ttu-id="c10e1-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c10e1-123">Name of resource group.</span></span>

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

### <span data-ttu-id="c10e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c10e1-124">CommonParameters</span></span>
<span data-ttu-id="c10e1-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c10e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c10e1-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c10e1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c10e1-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c10e1-127">INPUTS</span></span>

### <span data-ttu-id="c10e1-128">Keine</span><span class="sxs-lookup"><span data-stu-id="c10e1-128">None</span></span>

## <span data-ttu-id="c10e1-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c10e1-129">OUTPUTS</span></span>

### <span data-ttu-id="c10e1-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c10e1-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c10e1-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c10e1-131">NOTES</span></span>

## <span data-ttu-id="c10e1-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c10e1-132">RELATED LINKS</span></span>
