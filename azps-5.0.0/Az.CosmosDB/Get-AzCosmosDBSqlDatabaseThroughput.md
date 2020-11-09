---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299494"
---
# <span data-ttu-id="9431b-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="9431b-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="9431b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9431b-102">SYNOPSIS</span></span>
<span data-ttu-id="9431b-103">Ruft die Durchsatz Einstellungen ab, die einer CosmosDB SQL-Datenbank entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9431b-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="9431b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9431b-104">SYNTAX</span></span>

### <span data-ttu-id="9431b-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9431b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9431b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9431b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9431b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9431b-107">DESCRIPTION</span></span>
<span data-ttu-id="9431b-108">Das Cmdlet " **Get-AzCosmosDBSqlDatabaseThroughput** " Ruft die Durchsatz Einstellungen ab, die einer CosmosDB SQL-Datenbank entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9431b-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="9431b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9431b-109">EXAMPLES</span></span>

### <span data-ttu-id="9431b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9431b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="9431b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9431b-111">PARAMETERS</span></span>

### <span data-ttu-id="9431b-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="9431b-112">-AccountName</span></span>
<span data-ttu-id="9431b-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="9431b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9431b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9431b-114">-DefaultProfile</span></span>
<span data-ttu-id="9431b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9431b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9431b-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9431b-116">-InputObject</span></span>
<span data-ttu-id="9431b-117">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="9431b-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9431b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9431b-118">-Name</span></span>
<span data-ttu-id="9431b-119">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="9431b-119">Database name.</span></span>

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

### <span data-ttu-id="9431b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9431b-120">-ResourceGroupName</span></span>
<span data-ttu-id="9431b-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9431b-121">Name of resource group.</span></span>

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

### <span data-ttu-id="9431b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9431b-122">CommonParameters</span></span>
<span data-ttu-id="9431b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9431b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9431b-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9431b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9431b-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9431b-125">INPUTS</span></span>

### <span data-ttu-id="9431b-126">Keine</span><span class="sxs-lookup"><span data-stu-id="9431b-126">None</span></span>

## <span data-ttu-id="9431b-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9431b-127">OUTPUTS</span></span>

### <span data-ttu-id="9431b-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9431b-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9431b-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="9431b-129">NOTES</span></span>

## <span data-ttu-id="9431b-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9431b-130">RELATED LINKS</span></span>
