---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: c83e1d2edba5f34a4d8478ae97cee09b57f823ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936240"
---
# <span data-ttu-id="96ea6-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="96ea6-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="96ea6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="96ea6-103">Ruft eine CosmosDB-Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="96ea6-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="96ea6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96ea6-104">SYNTAX</span></span>

### <span data-ttu-id="96ea6-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="96ea6-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96ea6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96ea6-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96ea6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96ea6-107">DESCRIPTION</span></span>
<span data-ttu-id="96ea6-108">Das **Get-AzCosmosDBTable-Cmdlet** ruft eine vorhandene Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="96ea6-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="96ea6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="96ea6-109">EXAMPLES</span></span>

### <span data-ttu-id="96ea6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="96ea6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="96ea6-111">Das Ressourcenobjekt enthält _rid-, _ts-, _-etag-Eigenschaften der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="96ea6-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="96ea6-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="96ea6-112">PARAMETERS</span></span>

### <span data-ttu-id="96ea6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="96ea6-113">-AccountName</span></span>
<span data-ttu-id="96ea6-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="96ea6-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="96ea6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96ea6-115">-DefaultProfile</span></span>
<span data-ttu-id="96ea6-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96ea6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96ea6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="96ea6-117">-Name</span></span>
<span data-ttu-id="96ea6-118">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="96ea6-118">Name of the Table.</span></span>

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

### <span data-ttu-id="96ea6-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="96ea6-119">-ParentObject</span></span>
<span data-ttu-id="96ea6-120">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="96ea6-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="96ea6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96ea6-121">-ResourceGroupName</span></span>
<span data-ttu-id="96ea6-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="96ea6-122">Name of resource group.</span></span>

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

### <span data-ttu-id="96ea6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96ea6-123">CommonParameters</span></span>
<span data-ttu-id="96ea6-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96ea6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96ea6-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96ea6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96ea6-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="96ea6-126">INPUTS</span></span>

### <span data-ttu-id="96ea6-127">Keine</span><span class="sxs-lookup"><span data-stu-id="96ea6-127">None</span></span>

## <span data-ttu-id="96ea6-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="96ea6-128">OUTPUTS</span></span>

### <span data-ttu-id="96ea6-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="96ea6-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="96ea6-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="96ea6-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="96ea6-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="96ea6-131">NOTES</span></span>

## <span data-ttu-id="96ea6-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="96ea6-132">RELATED LINKS</span></span>
