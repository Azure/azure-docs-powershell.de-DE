---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372894"
---
# <span data-ttu-id="ff0af-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="ff0af-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="ff0af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff0af-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0af-103">Aktualisiert den Durchsatzwert einer Datenbank-Db-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ff0af-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="ff0af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff0af-104">SYNTAX</span></span>

### <span data-ttu-id="ff0af-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff0af-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff0af-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff0af-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff0af-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff0af-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff0af-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff0af-108">DESCRIPTION</span></span>
<span data-ttu-id="ff0af-109">Aktualisiert den Durchsatzwert einer Datenbank-Db-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ff0af-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="ff0af-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ff0af-110">EXAMPLES</span></span>

### <span data-ttu-id="ff0af-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ff0af-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="ff0af-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff0af-112">PARAMETERS</span></span>

### <span data-ttu-id="ff0af-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff0af-113">-AccountName</span></span>
<span data-ttu-id="ff0af-114">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="ff0af-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ff0af-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ff0af-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ff0af-116">Maximaler Durchsatzwert, wenn die Autoskala aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ff0af-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ff0af-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff0af-117">-Confirm</span></span>
<span data-ttu-id="ff0af-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ff0af-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff0af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0af-119">-DefaultProfile</span></span>
<span data-ttu-id="ff0af-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff0af-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff0af-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff0af-121">-InputObject</span></span>
<span data-ttu-id="ff0af-122">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="ff0af-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ff0af-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ff0af-123">-Name</span></span>
<span data-ttu-id="ff0af-124">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ff0af-124">Name of the Table.</span></span>

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

### <span data-ttu-id="ff0af-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ff0af-125">-ParentObject</span></span>
<span data-ttu-id="ff0af-126">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="ff0af-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ff0af-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff0af-127">-ResourceGroupName</span></span>
<span data-ttu-id="ff0af-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ff0af-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ff0af-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="ff0af-129">-Throughput</span></span>
<span data-ttu-id="ff0af-130">Der Durchsatz von Tabellen (RU/s).</span><span class="sxs-lookup"><span data-stu-id="ff0af-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="ff0af-131">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="ff0af-131">Default value is 400.</span></span>

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

### <span data-ttu-id="ff0af-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ff0af-132">-WhatIf</span></span>
<span data-ttu-id="ff0af-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff0af-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff0af-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff0af-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff0af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0af-135">CommonParameters</span></span>
<span data-ttu-id="ff0af-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff0af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0af-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff0af-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0af-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ff0af-138">INPUTS</span></span>

### <span data-ttu-id="ff0af-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ff0af-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="ff0af-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ff0af-140">OUTPUTS</span></span>

### <span data-ttu-id="ff0af-141">Microsoft.Azure.Commands.ExesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ff0af-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ff0af-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ff0af-142">NOTES</span></span>

## <span data-ttu-id="ff0af-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ff0af-143">RELATED LINKS</span></span>
