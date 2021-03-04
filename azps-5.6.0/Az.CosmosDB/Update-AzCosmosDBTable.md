---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: 3463a07219375db06495bd5d50a2fe3b5916e173
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947456"
---
# <span data-ttu-id="dbdab-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="dbdab-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="dbdab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbdab-102">SYNOPSIS</span></span>
<span data-ttu-id="dbdab-103">Aktualisiert die Tabelle "CosmosDB".</span><span class="sxs-lookup"><span data-stu-id="dbdab-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="dbdab-104">Führt einen clientseitigen Patchvorgang durch Lesen der vorhandenen Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="dbdab-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="dbdab-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbdab-105">SYNTAX</span></span>

### <span data-ttu-id="dbdab-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbdab-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbdab-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbdab-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbdab-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbdab-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbdab-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbdab-109">DESCRIPTION</span></span>
<span data-ttu-id="dbdab-110">Aktualisiert die Tabelle "CosmosDB".</span><span class="sxs-lookup"><span data-stu-id="dbdab-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="dbdab-111">Führt einen clientseitigen Patchvorgang durch Lesen der vorhandenen Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="dbdab-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="dbdab-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dbdab-112">EXAMPLES</span></span>

### <span data-ttu-id="dbdab-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dbdab-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="dbdab-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dbdab-114">PARAMETERS</span></span>

### <span data-ttu-id="dbdab-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dbdab-115">-AccountName</span></span>
<span data-ttu-id="dbdab-116">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="dbdab-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dbdab-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="dbdab-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="dbdab-118">Maximaler Durchsatzwert, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dbdab-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="dbdab-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dbdab-119">-Confirm</span></span>
<span data-ttu-id="dbdab-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbdab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbdab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbdab-121">-DefaultProfile</span></span>
<span data-ttu-id="dbdab-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbdab-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbdab-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbdab-123">-InputObject</span></span>
<span data-ttu-id="dbdab-124">Tabellenobjekt.</span><span class="sxs-lookup"><span data-stu-id="dbdab-124">Table Object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbdab-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dbdab-125">-Name</span></span>
<span data-ttu-id="dbdab-126">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="dbdab-126">Name of the Table.</span></span>

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

### <span data-ttu-id="dbdab-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dbdab-127">-ParentObject</span></span>
<span data-ttu-id="dbdab-128">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="dbdab-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="dbdab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbdab-129">-ResourceGroupName</span></span>
<span data-ttu-id="dbdab-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dbdab-130">Name of resource group.</span></span>

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

### <span data-ttu-id="dbdab-131">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="dbdab-131">-Throughput</span></span>
<span data-ttu-id="dbdab-132">Der Durchsatz von Tabelle (RU/s).</span><span class="sxs-lookup"><span data-stu-id="dbdab-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="dbdab-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="dbdab-133">Default value is 400.</span></span>

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

### <span data-ttu-id="dbdab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbdab-134">-WhatIf</span></span>
<span data-ttu-id="dbdab-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbdab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbdab-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbdab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbdab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbdab-137">CommonParameters</span></span>
<span data-ttu-id="dbdab-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbdab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbdab-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbdab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbdab-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dbdab-140">INPUTS</span></span>

### <span data-ttu-id="dbdab-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="dbdab-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="dbdab-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="dbdab-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="dbdab-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dbdab-143">OUTPUTS</span></span>

### <span data-ttu-id="dbdab-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="dbdab-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="dbdab-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="dbdab-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="dbdab-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dbdab-146">NOTES</span></span>

## <span data-ttu-id="dbdab-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dbdab-147">RELATED LINKS</span></span>
