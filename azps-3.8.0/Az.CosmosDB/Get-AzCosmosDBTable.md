---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: 7fb12f7413a0452a3e74f6fa03aa9a391dcacd26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005088"
---
# <span data-ttu-id="02abc-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="02abc-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="02abc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02abc-102">SYNOPSIS</span></span>
<span data-ttu-id="02abc-103">Ruft eine CosmosDB-Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="02abc-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="02abc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02abc-104">SYNTAX</span></span>

### <span data-ttu-id="02abc-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="02abc-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02abc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02abc-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02abc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02abc-107">DESCRIPTION</span></span>
<span data-ttu-id="02abc-108">Das Cmdlet " **Get-AzCosmosDBTable** " Ruft eine vorhandene Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="02abc-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="02abc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02abc-109">EXAMPLES</span></span>

### <span data-ttu-id="02abc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="02abc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="02abc-111">Das Ressourcenobjekt enthält _rid, _ts, _ ETag-Eigenschaften der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="02abc-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="02abc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="02abc-112">PARAMETERS</span></span>

### <span data-ttu-id="02abc-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="02abc-113">-AccountName</span></span>
<span data-ttu-id="02abc-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="02abc-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="02abc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02abc-115">-DefaultProfile</span></span>
<span data-ttu-id="02abc-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02abc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02abc-117">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="02abc-117">-Detailed</span></span>
<span data-ttu-id="02abc-118">Wenn Sie dann bereitgestellt werden, gibt das Cmdlet die Tabelle mit dem entsprechenden Durchsatz zurück.</span><span class="sxs-lookup"><span data-stu-id="02abc-118">If provided then, the cmdlet returns the Table with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="02abc-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="02abc-119">-InputObject</span></span>
<span data-ttu-id="02abc-120">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="02abc-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02abc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="02abc-121">-Name</span></span>
<span data-ttu-id="02abc-122">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="02abc-122">Name of the Table.</span></span>

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

### <span data-ttu-id="02abc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02abc-123">-ResourceGroupName</span></span>
<span data-ttu-id="02abc-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="02abc-124">Name of resource group.</span></span>

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

### <span data-ttu-id="02abc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02abc-125">CommonParameters</span></span>
<span data-ttu-id="02abc-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02abc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02abc-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02abc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02abc-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02abc-128">INPUTS</span></span>

### <span data-ttu-id="02abc-129">Keine</span><span class="sxs-lookup"><span data-stu-id="02abc-129">None</span></span>

## <span data-ttu-id="02abc-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02abc-130">OUTPUTS</span></span>

### <span data-ttu-id="02abc-131">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="02abc-131">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="02abc-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="02abc-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="02abc-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="02abc-133">NOTES</span></span>

## <span data-ttu-id="02abc-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02abc-134">RELATED LINKS</span></span>
