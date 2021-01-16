---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356417"
---
# <span data-ttu-id="d431d-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="d431d-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="d431d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d431d-102">SYNOPSIS</span></span>
<span data-ttu-id="d431d-103">Ruft eine Tabelle für UntereDb ab.</span><span class="sxs-lookup"><span data-stu-id="d431d-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="d431d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d431d-104">SYNTAX</span></span>

### <span data-ttu-id="d431d-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d431d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d431d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d431d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d431d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d431d-107">DESCRIPTION</span></span>
<span data-ttu-id="d431d-108">Das **Cmdlet "Get-AzCosmosDBTable"** ruft eine vorhandene Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="d431d-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="d431d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d431d-109">EXAMPLES</span></span>

### <span data-ttu-id="d431d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d431d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="d431d-111">Das Ressourcenobjekt enthält _rid, _ts _ etag-Eigenschaften der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d431d-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="d431d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d431d-112">PARAMETERS</span></span>

### <span data-ttu-id="d431d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d431d-113">-AccountName</span></span>
<span data-ttu-id="d431d-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="d431d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d431d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d431d-115">-DefaultProfile</span></span>
<span data-ttu-id="d431d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d431d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d431d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d431d-117">-Name</span></span>
<span data-ttu-id="d431d-118">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d431d-118">Name of the Table.</span></span>

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

### <span data-ttu-id="d431d-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d431d-119">-ParentObject</span></span>
<span data-ttu-id="d431d-120">Objekt "Buchhalterungskonto"</span><span class="sxs-lookup"><span data-stu-id="d431d-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d431d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d431d-121">-ResourceGroupName</span></span>
<span data-ttu-id="d431d-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d431d-122">Name of resource group.</span></span>

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

### <span data-ttu-id="d431d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d431d-123">CommonParameters</span></span>
<span data-ttu-id="d431d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d431d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d431d-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d431d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d431d-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d431d-126">INPUTS</span></span>

### <span data-ttu-id="d431d-127">Keine</span><span class="sxs-lookup"><span data-stu-id="d431d-127">None</span></span>

## <span data-ttu-id="d431d-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d431d-128">OUTPUTS</span></span>

### <span data-ttu-id="d431d-129">Microsoft.Azure.Commands.DiesDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="d431d-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="d431d-130">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d431d-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d431d-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d431d-131">NOTES</span></span>

## <span data-ttu-id="d431d-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d431d-132">RELATED LINKS</span></span>
