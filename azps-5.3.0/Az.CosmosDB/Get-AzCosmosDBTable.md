---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470752"
---
# <span data-ttu-id="ea937-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="ea937-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="ea937-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea937-102">SYNOPSIS</span></span>
<span data-ttu-id="ea937-103">Ruft eine Tabelle für UntereDb ab.</span><span class="sxs-lookup"><span data-stu-id="ea937-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="ea937-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea937-104">SYNTAX</span></span>

### <span data-ttu-id="ea937-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea937-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea937-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea937-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea937-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea937-107">DESCRIPTION</span></span>
<span data-ttu-id="ea937-108">Das **Cmdlet "Get-AzCosmosDBTable"** ruft eine vorhandene Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="ea937-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="ea937-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea937-109">EXAMPLES</span></span>

### <span data-ttu-id="ea937-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea937-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="ea937-111">Das Ressourcenobjekt enthält _rid, _ts _ etag-Eigenschaften der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ea937-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="ea937-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea937-112">PARAMETERS</span></span>

### <span data-ttu-id="ea937-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ea937-113">-AccountName</span></span>
<span data-ttu-id="ea937-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="ea937-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ea937-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea937-115">-DefaultProfile</span></span>
<span data-ttu-id="ea937-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea937-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea937-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ea937-117">-Name</span></span>
<span data-ttu-id="ea937-118">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ea937-118">Name of the Table.</span></span>

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

### <span data-ttu-id="ea937-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ea937-119">-ParentObject</span></span>
<span data-ttu-id="ea937-120">Objekt "Buchhalterungskonto"</span><span class="sxs-lookup"><span data-stu-id="ea937-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ea937-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea937-121">-ResourceGroupName</span></span>
<span data-ttu-id="ea937-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ea937-122">Name of resource group.</span></span>

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

### <span data-ttu-id="ea937-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea937-123">CommonParameters</span></span>
<span data-ttu-id="ea937-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea937-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea937-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea937-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea937-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea937-126">INPUTS</span></span>

### <span data-ttu-id="ea937-127">Keine</span><span class="sxs-lookup"><span data-stu-id="ea937-127">None</span></span>

## <span data-ttu-id="ea937-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea937-128">OUTPUTS</span></span>

### <span data-ttu-id="ea937-129">Microsoft.Azure.Commands.ExesDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="ea937-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="ea937-130">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ea937-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ea937-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ea937-131">NOTES</span></span>

## <span data-ttu-id="ea937-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ea937-132">RELATED LINKS</span></span>
