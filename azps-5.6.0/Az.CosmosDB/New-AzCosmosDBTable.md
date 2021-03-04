---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: d2a4dacb929587fb0f06c002ad26df3144f32f56
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923011"
---
# <span data-ttu-id="34538-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="34538-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="34538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34538-102">SYNOPSIS</span></span>
<span data-ttu-id="34538-103">Erstellt eine neue Tabelle "CosmosDB".</span><span class="sxs-lookup"><span data-stu-id="34538-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="34538-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34538-104">SYNTAX</span></span>

### <span data-ttu-id="34538-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="34538-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34538-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34538-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34538-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34538-107">DESCRIPTION</span></span>
<span data-ttu-id="34538-108">Erstellt eine neue Tabelle "CosmosDB".</span><span class="sxs-lookup"><span data-stu-id="34538-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="34538-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="34538-109">EXAMPLES</span></span>

### <span data-ttu-id="34538-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="34538-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="34538-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="34538-111">PARAMETERS</span></span>

### <span data-ttu-id="34538-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="34538-112">-AccountName</span></span>
<span data-ttu-id="34538-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="34538-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="34538-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="34538-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="34538-115">Maximaler Durchsatzwert, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="34538-115">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34538-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34538-116">-Confirm</span></span>
<span data-ttu-id="34538-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34538-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34538-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34538-118">-DefaultProfile</span></span>
<span data-ttu-id="34538-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34538-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34538-120">-Name</span><span class="sxs-lookup"><span data-stu-id="34538-120">-Name</span></span>
<span data-ttu-id="34538-121">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="34538-121">Name of the Table.</span></span>

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

### <span data-ttu-id="34538-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="34538-122">-ParentObject</span></span>
<span data-ttu-id="34538-123">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="34538-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="34538-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34538-124">-ResourceGroupName</span></span>
<span data-ttu-id="34538-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="34538-125">Name of resource group.</span></span>

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

### <span data-ttu-id="34538-126">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="34538-126">-Throughput</span></span>
<span data-ttu-id="34538-127">Der Durchsatz von Tabelle (RU/s).</span><span class="sxs-lookup"><span data-stu-id="34538-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="34538-128">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="34538-128">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34538-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34538-129">-WhatIf</span></span>
<span data-ttu-id="34538-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34538-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34538-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34538-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34538-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34538-132">CommonParameters</span></span>
<span data-ttu-id="34538-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34538-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34538-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34538-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34538-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="34538-135">INPUTS</span></span>

### <span data-ttu-id="34538-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="34538-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="34538-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="34538-137">OUTPUTS</span></span>

### <span data-ttu-id="34538-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="34538-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="34538-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="34538-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="34538-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="34538-140">NOTES</span></span>

## <span data-ttu-id="34538-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="34538-141">RELATED LINKS</span></span>
