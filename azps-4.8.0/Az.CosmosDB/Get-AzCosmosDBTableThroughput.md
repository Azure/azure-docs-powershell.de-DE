---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7fc023ddd5a986cc71ce86c05967f5253a39b26d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167098"
---
# <span data-ttu-id="79b52-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="79b52-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="79b52-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79b52-102">SYNOPSIS</span></span>
<span data-ttu-id="79b52-103">Ruft den Durchsatz einer CosmosDB-Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="79b52-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="79b52-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79b52-104">SYNTAX</span></span>

### <span data-ttu-id="79b52-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="79b52-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79b52-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79b52-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79b52-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79b52-107">DESCRIPTION</span></span>
<span data-ttu-id="79b52-108">Das Cmdlet " **Get-AzCosmosDBTableThroughput** " Ruft den Durchsatz einer CosmosDB-Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="79b52-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="79b52-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79b52-109">EXAMPLES</span></span>

### <span data-ttu-id="79b52-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79b52-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="79b52-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="79b52-111">PARAMETERS</span></span>

### <span data-ttu-id="79b52-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="79b52-112">-AccountName</span></span>
<span data-ttu-id="79b52-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="79b52-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="79b52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b52-114">-DefaultProfile</span></span>
<span data-ttu-id="79b52-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79b52-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79b52-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="79b52-116">-InputObject</span></span>
<span data-ttu-id="79b52-117">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="79b52-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="79b52-118">-Name</span><span class="sxs-lookup"><span data-stu-id="79b52-118">-Name</span></span>
<span data-ttu-id="79b52-119">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="79b52-119">Name of the Table.</span></span>

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

### <span data-ttu-id="79b52-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79b52-120">-ResourceGroupName</span></span>
<span data-ttu-id="79b52-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="79b52-121">Name of resource group.</span></span>

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

### <span data-ttu-id="79b52-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b52-122">CommonParameters</span></span>
<span data-ttu-id="79b52-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b52-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b52-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79b52-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b52-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79b52-125">INPUTS</span></span>

### <span data-ttu-id="79b52-126">Keine</span><span class="sxs-lookup"><span data-stu-id="79b52-126">None</span></span>

## <span data-ttu-id="79b52-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79b52-127">OUTPUTS</span></span>

### <span data-ttu-id="79b52-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="79b52-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="79b52-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="79b52-129">NOTES</span></span>

## <span data-ttu-id="79b52-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79b52-130">RELATED LINKS</span></span>
