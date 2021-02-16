---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171018"
---
# <span data-ttu-id="284ee-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="284ee-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="284ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="284ee-102">SYNOPSIS</span></span>
<span data-ttu-id="284ee-103">Erstellt eine neue Tabelle unter "Untere Datenbank".</span><span class="sxs-lookup"><span data-stu-id="284ee-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="284ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="284ee-104">SYNTAX</span></span>

### <span data-ttu-id="284ee-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="284ee-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="284ee-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="284ee-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="284ee-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="284ee-107">DESCRIPTION</span></span>
<span data-ttu-id="284ee-108">Erstellt eine neue Tabelle unter "Untere Datenbank".</span><span class="sxs-lookup"><span data-stu-id="284ee-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="284ee-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="284ee-109">EXAMPLES</span></span>

### <span data-ttu-id="284ee-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="284ee-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="284ee-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="284ee-111">PARAMETERS</span></span>

### <span data-ttu-id="284ee-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="284ee-112">-AccountName</span></span>
<span data-ttu-id="284ee-113">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="284ee-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="284ee-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="284ee-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="284ee-115">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="284ee-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="284ee-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="284ee-116">-Confirm</span></span>
<span data-ttu-id="284ee-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="284ee-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="284ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="284ee-118">-DefaultProfile</span></span>
<span data-ttu-id="284ee-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="284ee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="284ee-120">-Name</span><span class="sxs-lookup"><span data-stu-id="284ee-120">-Name</span></span>
<span data-ttu-id="284ee-121">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="284ee-121">Name of the Table.</span></span>

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

### <span data-ttu-id="284ee-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="284ee-122">-ParentObject</span></span>
<span data-ttu-id="284ee-123">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="284ee-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="284ee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="284ee-124">-ResourceGroupName</span></span>
<span data-ttu-id="284ee-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="284ee-125">Name of resource group.</span></span>

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

### <span data-ttu-id="284ee-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="284ee-126">-Throughput</span></span>
<span data-ttu-id="284ee-127">Der Durchsatz von Tabellen (RU/s).</span><span class="sxs-lookup"><span data-stu-id="284ee-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="284ee-128">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="284ee-128">Default value is 400.</span></span>

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

### <span data-ttu-id="284ee-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="284ee-129">-WhatIf</span></span>
<span data-ttu-id="284ee-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="284ee-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="284ee-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="284ee-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="284ee-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="284ee-132">CommonParameters</span></span>
<span data-ttu-id="284ee-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="284ee-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="284ee-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="284ee-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="284ee-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="284ee-135">INPUTS</span></span>

### <span data-ttu-id="284ee-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="284ee-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="284ee-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="284ee-137">OUTPUTS</span></span>

### <span data-ttu-id="284ee-138">Microsoft.Azure.Commands.ExesDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="284ee-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="284ee-139">Microsoft.Azure.Commands.DiesDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="284ee-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="284ee-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="284ee-140">NOTES</span></span>

## <span data-ttu-id="284ee-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="284ee-141">RELATED LINKS</span></span>
