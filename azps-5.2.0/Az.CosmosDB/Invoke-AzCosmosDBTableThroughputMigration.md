---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 009048c5f37936d469fe88c5e75cab8270efa81c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361205"
---
# <span data-ttu-id="e4302-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="e4302-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="e4302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4302-102">SYNOPSIS</span></span>
<span data-ttu-id="e4302-103">Verwenden Sie diese Funktion, um den Durchsatz der automatischen Skala in den manuellen Durchsatz und umgekehrt zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="e4302-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="e4302-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4302-104">SYNTAX</span></span>

### <span data-ttu-id="e4302-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e4302-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4302-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4302-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4302-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4302-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4302-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4302-108">DESCRIPTION</span></span>
<span data-ttu-id="e4302-109">Der ThroughpyteType-Parameterer definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="e4302-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="e4302-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e4302-110">EXAMPLES</span></span>

### <span data-ttu-id="e4302-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e4302-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="e4302-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4302-112">PARAMETERS</span></span>

### <span data-ttu-id="e4302-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e4302-113">-AccountName</span></span>
<span data-ttu-id="e4302-114">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="e4302-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e4302-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4302-115">-Confirm</span></span>
<span data-ttu-id="e4302-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4302-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4302-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4302-117">-DefaultProfile</span></span>
<span data-ttu-id="e4302-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4302-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4302-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4302-119">-InputObject</span></span>
<span data-ttu-id="e4302-120">Tabellenobjekt.</span><span class="sxs-lookup"><span data-stu-id="e4302-120">Table Object.</span></span>

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

### <span data-ttu-id="e4302-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e4302-121">-Name</span></span>
<span data-ttu-id="e4302-122">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e4302-122">Name of the Table.</span></span>

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

### <span data-ttu-id="e4302-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e4302-123">-ParentObject</span></span>
<span data-ttu-id="e4302-124">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="e4302-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e4302-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4302-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4302-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e4302-126">Name of resource group.</span></span>

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

### <span data-ttu-id="e4302-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="e4302-127">-ThroughputType</span></span>
<span data-ttu-id="e4302-128">Durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4302-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="e4302-129">Mögliche Werte sind: Autoskalieren, Manuell.</span><span class="sxs-lookup"><span data-stu-id="e4302-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="e4302-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e4302-130">-WhatIf</span></span>
<span data-ttu-id="e4302-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4302-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4302-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4302-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4302-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4302-133">CommonParameters</span></span>
<span data-ttu-id="e4302-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4302-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4302-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4302-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4302-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e4302-136">INPUTS</span></span>

### <span data-ttu-id="e4302-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="e4302-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="e4302-138">Microsoft.Azure.Commands.DiesDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="e4302-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="e4302-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e4302-139">OUTPUTS</span></span>

### <span data-ttu-id="e4302-140">Microsoft.Azure.Commands.DiesDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e4302-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e4302-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e4302-141">NOTES</span></span>

## <span data-ttu-id="e4302-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e4302-142">RELATED LINKS</span></span>
