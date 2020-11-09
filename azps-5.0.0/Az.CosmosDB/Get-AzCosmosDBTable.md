---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299469"
---
# <span data-ttu-id="009e2-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="009e2-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="009e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="009e2-102">SYNOPSIS</span></span>
<span data-ttu-id="009e2-103">Ruft eine CosmosDB-Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="009e2-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="009e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="009e2-104">SYNTAX</span></span>

### <span data-ttu-id="009e2-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="009e2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="009e2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="009e2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="009e2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="009e2-107">DESCRIPTION</span></span>
<span data-ttu-id="009e2-108">Das Cmdlet " **Get-AzCosmosDBTable** " Ruft eine vorhandene Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="009e2-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="009e2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="009e2-109">EXAMPLES</span></span>

### <span data-ttu-id="009e2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="009e2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="009e2-111">Das Ressourcenobjekt enthält _rid, _ts, _ ETag-Eigenschaften der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="009e2-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="009e2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="009e2-112">PARAMETERS</span></span>

### <span data-ttu-id="009e2-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="009e2-113">-AccountName</span></span>
<span data-ttu-id="009e2-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="009e2-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="009e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="009e2-115">-DefaultProfile</span></span>
<span data-ttu-id="009e2-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="009e2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="009e2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="009e2-117">-Name</span></span>
<span data-ttu-id="009e2-118">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="009e2-118">Name of the Table.</span></span>

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

### <span data-ttu-id="009e2-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="009e2-119">-ParentObject</span></span>
<span data-ttu-id="009e2-120">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="009e2-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="009e2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="009e2-121">-ResourceGroupName</span></span>
<span data-ttu-id="009e2-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="009e2-122">Name of resource group.</span></span>

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

### <span data-ttu-id="009e2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="009e2-123">CommonParameters</span></span>
<span data-ttu-id="009e2-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="009e2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="009e2-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="009e2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="009e2-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="009e2-126">INPUTS</span></span>

### <span data-ttu-id="009e2-127">Keine</span><span class="sxs-lookup"><span data-stu-id="009e2-127">None</span></span>

## <span data-ttu-id="009e2-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="009e2-128">OUTPUTS</span></span>

### <span data-ttu-id="009e2-129">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="009e2-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="009e2-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="009e2-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="009e2-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="009e2-131">NOTES</span></span>

## <span data-ttu-id="009e2-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="009e2-132">RELATED LINKS</span></span>
