---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175277"
---
# <span data-ttu-id="7fb9d-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="7fb9d-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="7fb9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7fb9d-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb9d-103">Aktualisiert den Durchsatz einer CosmosDB-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="7fb9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fb9d-104">SYNTAX</span></span>

### <span data-ttu-id="7fb9d-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7fb9d-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb9d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb9d-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb9d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb9d-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7fb9d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7fb9d-108">DESCRIPTION</span></span>
<span data-ttu-id="7fb9d-109">Aktualisiert den Durchsatz einer CosmosDB-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="7fb9d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fb9d-110">EXAMPLES</span></span>

### <span data-ttu-id="7fb9d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7fb9d-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="7fb9d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fb9d-112">PARAMETERS</span></span>

### <span data-ttu-id="7fb9d-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="7fb9d-113">-AccountName</span></span>
<span data-ttu-id="7fb9d-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7fb9d-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7fb9d-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7fb9d-116">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="7fb9d-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7fb9d-117">-Confirm</span></span>
<span data-ttu-id="7fb9d-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb9d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb9d-119">-DefaultProfile</span></span>
<span data-ttu-id="7fb9d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fb9d-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7fb9d-121">-InputObject</span></span>
<span data-ttu-id="7fb9d-122">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="7fb9d-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7fb9d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7fb9d-123">-Name</span></span>
<span data-ttu-id="7fb9d-124">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-124">Name of the Table.</span></span>

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

### <span data-ttu-id="7fb9d-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7fb9d-125">-ParentObject</span></span>
<span data-ttu-id="7fb9d-126">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="7fb9d-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7fb9d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb9d-127">-ResourceGroupName</span></span>
<span data-ttu-id="7fb9d-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-128">Name of resource group.</span></span>

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

### <span data-ttu-id="7fb9d-129">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="7fb9d-129">-Throughput</span></span>
<span data-ttu-id="7fb9d-130">Der Durchsatz der Tabelle (ru/s).</span><span class="sxs-lookup"><span data-stu-id="7fb9d-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="7fb9d-131">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-131">Default value is 400.</span></span>

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

### <span data-ttu-id="7fb9d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb9d-132">-WhatIf</span></span>
<span data-ttu-id="7fb9d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fb9d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb9d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb9d-135">CommonParameters</span></span>
<span data-ttu-id="7fb9d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb9d-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fb9d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb9d-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7fb9d-138">INPUTS</span></span>

### <span data-ttu-id="7fb9d-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7fb9d-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="7fb9d-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7fb9d-140">OUTPUTS</span></span>

### <span data-ttu-id="7fb9d-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7fb9d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7fb9d-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="7fb9d-142">NOTES</span></span>

## <span data-ttu-id="7fb9d-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7fb9d-143">RELATED LINKS</span></span>
