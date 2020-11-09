---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 009048c5f37936d469fe88c5e75cab8270efa81c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299409"
---
# <span data-ttu-id="fe5fb-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="fe5fb-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="fe5fb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe5fb-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5fb-103">Verwenden Sie diese Vorgehensweise, um den AutoScale-Durchsatz auf manuellen Durchsatz zu migrieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="fe5fb-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="fe5fb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe5fb-104">SYNTAX</span></span>

### <span data-ttu-id="fe5fb-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe5fb-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe5fb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe5fb-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe5fb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe5fb-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe5fb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe5fb-108">DESCRIPTION</span></span>
<span data-ttu-id="fe5fb-109">ThroughpyteType Parameter definiert den Durchsatz, zu dem Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="fe5fb-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="fe5fb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe5fb-110">EXAMPLES</span></span>

### <span data-ttu-id="fe5fb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe5fb-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="fe5fb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe5fb-112">PARAMETERS</span></span>

### <span data-ttu-id="fe5fb-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="fe5fb-113">-AccountName</span></span>
<span data-ttu-id="fe5fb-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="fe5fb-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fe5fb-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fe5fb-115">-Confirm</span></span>
<span data-ttu-id="fe5fb-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe5fb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe5fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5fb-117">-DefaultProfile</span></span>
<span data-ttu-id="fe5fb-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe5fb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe5fb-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fe5fb-119">-InputObject</span></span>
<span data-ttu-id="fe5fb-120">Table-Objekt</span><span class="sxs-lookup"><span data-stu-id="fe5fb-120">Table Object.</span></span>

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

### <span data-ttu-id="fe5fb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fe5fb-121">-Name</span></span>
<span data-ttu-id="fe5fb-122">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fe5fb-122">Name of the Table.</span></span>

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

### <span data-ttu-id="fe5fb-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fe5fb-123">-ParentObject</span></span>
<span data-ttu-id="fe5fb-124">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="fe5fb-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fe5fb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe5fb-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe5fb-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fe5fb-126">Name of resource group.</span></span>

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

### <span data-ttu-id="fe5fb-127">-Durchsatztyp</span><span class="sxs-lookup"><span data-stu-id="fe5fb-127">-ThroughputType</span></span>
<span data-ttu-id="fe5fb-128">Der durchsatztyp, zu dem migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe5fb-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="fe5fb-129">Mögliche Werte sind: AutoScale, manuell.</span><span class="sxs-lookup"><span data-stu-id="fe5fb-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="fe5fb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe5fb-130">-WhatIf</span></span>
<span data-ttu-id="fe5fb-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe5fb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe5fb-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe5fb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe5fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5fb-133">CommonParameters</span></span>
<span data-ttu-id="fe5fb-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe5fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5fb-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe5fb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5fb-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe5fb-136">INPUTS</span></span>

### <span data-ttu-id="fe5fb-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="fe5fb-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="fe5fb-138">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="fe5fb-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="fe5fb-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe5fb-139">OUTPUTS</span></span>

### <span data-ttu-id="fe5fb-140">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="fe5fb-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fe5fb-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe5fb-141">NOTES</span></span>

## <span data-ttu-id="fe5fb-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe5fb-142">RELATED LINKS</span></span>
