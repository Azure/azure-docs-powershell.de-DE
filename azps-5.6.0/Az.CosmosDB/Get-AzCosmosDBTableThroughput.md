---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7b48190a9ef01d468e762d93d7bc63a96e831de8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936232"
---
# <span data-ttu-id="44219-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="44219-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="44219-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44219-102">SYNOPSIS</span></span>
<span data-ttu-id="44219-103">Ruft den Durchsatz einer CosmosDB-Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="44219-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="44219-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44219-104">SYNTAX</span></span>

### <span data-ttu-id="44219-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="44219-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44219-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44219-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44219-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44219-107">DESCRIPTION</span></span>
<span data-ttu-id="44219-108">Das **Cmdlet Get-AzCosmosDBTableThroughput** ruft den Durchsatz einer CosmosDB-Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="44219-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="44219-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="44219-109">EXAMPLES</span></span>

### <span data-ttu-id="44219-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="44219-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="44219-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="44219-111">PARAMETERS</span></span>

### <span data-ttu-id="44219-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="44219-112">-AccountName</span></span>
<span data-ttu-id="44219-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="44219-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="44219-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44219-114">-DefaultProfile</span></span>
<span data-ttu-id="44219-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44219-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44219-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44219-116">-InputObject</span></span>
<span data-ttu-id="44219-117">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="44219-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="44219-118">-Name</span><span class="sxs-lookup"><span data-stu-id="44219-118">-Name</span></span>
<span data-ttu-id="44219-119">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="44219-119">Name of the Table.</span></span>

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

### <span data-ttu-id="44219-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44219-120">-ResourceGroupName</span></span>
<span data-ttu-id="44219-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="44219-121">Name of resource group.</span></span>

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

### <span data-ttu-id="44219-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44219-122">CommonParameters</span></span>
<span data-ttu-id="44219-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44219-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44219-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44219-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44219-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="44219-125">INPUTS</span></span>

### <span data-ttu-id="44219-126">Keine</span><span class="sxs-lookup"><span data-stu-id="44219-126">None</span></span>

## <span data-ttu-id="44219-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="44219-127">OUTPUTS</span></span>

### <span data-ttu-id="44219-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="44219-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="44219-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="44219-129">NOTES</span></span>

## <span data-ttu-id="44219-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="44219-130">RELATED LINKS</span></span>
