---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472761"
---
# <span data-ttu-id="fe2f7-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="fe2f7-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="fe2f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe2f7-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2f7-103">Aktualisiert den Durchsatzwert einer Datenbank-Db-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="fe2f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe2f7-104">SYNTAX</span></span>

### <span data-ttu-id="fe2f7-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe2f7-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe2f7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe2f7-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe2f7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe2f7-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe2f7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe2f7-108">DESCRIPTION</span></span>
<span data-ttu-id="fe2f7-109">Aktualisiert den Durchsatzwert einer Datenbank-Db-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="fe2f7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe2f7-110">EXAMPLES</span></span>

### <span data-ttu-id="fe2f7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe2f7-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="fe2f7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe2f7-112">PARAMETERS</span></span>

### <span data-ttu-id="fe2f7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fe2f7-113">-AccountName</span></span>
<span data-ttu-id="fe2f7-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fe2f7-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="fe2f7-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="fe2f7-116">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="fe2f7-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe2f7-117">-Confirm</span></span>
<span data-ttu-id="fe2f7-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe2f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2f7-119">-DefaultProfile</span></span>
<span data-ttu-id="fe2f7-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe2f7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe2f7-121">-InputObject</span></span>
<span data-ttu-id="fe2f7-122">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="fe2f7-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fe2f7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fe2f7-123">-Name</span></span>
<span data-ttu-id="fe2f7-124">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-124">Name of the Table.</span></span>

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

### <span data-ttu-id="fe2f7-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fe2f7-125">-ParentObject</span></span>
<span data-ttu-id="fe2f7-126">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="fe2f7-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fe2f7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe2f7-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe2f7-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-128">Name of resource group.</span></span>

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

### <span data-ttu-id="fe2f7-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="fe2f7-129">-Throughput</span></span>
<span data-ttu-id="fe2f7-130">Der Durchsatz von Tabellen (RU/s).</span><span class="sxs-lookup"><span data-stu-id="fe2f7-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="fe2f7-131">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-131">Default value is 400.</span></span>

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

### <span data-ttu-id="fe2f7-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fe2f7-132">-WhatIf</span></span>
<span data-ttu-id="fe2f7-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe2f7-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe2f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2f7-135">CommonParameters</span></span>
<span data-ttu-id="fe2f7-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2f7-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe2f7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2f7-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe2f7-138">INPUTS</span></span>

### <span data-ttu-id="fe2f7-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="fe2f7-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="fe2f7-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe2f7-140">OUTPUTS</span></span>

### <span data-ttu-id="fe2f7-141">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="fe2f7-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fe2f7-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fe2f7-142">NOTES</span></span>

## <span data-ttu-id="fe2f7-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fe2f7-143">RELATED LINKS</span></span>
