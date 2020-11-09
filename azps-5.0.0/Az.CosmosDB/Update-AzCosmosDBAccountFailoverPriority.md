---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 6a1c155a33ef704895a76dc35bf342aa47cd47ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299098"
---
# <span data-ttu-id="605c0-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="605c0-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="605c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="605c0-102">SYNOPSIS</span></span>
<span data-ttu-id="605c0-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="605c0-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="605c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="605c0-104">SYNTAX</span></span>

### <span data-ttu-id="605c0-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="605c0-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="605c0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="605c0-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="605c0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="605c0-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="605c0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="605c0-108">DESCRIPTION</span></span>
<span data-ttu-id="605c0-109">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="605c0-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="605c0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="605c0-110">EXAMPLES</span></span>

### <span data-ttu-id="605c0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="605c0-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="605c0-112">FailoverPolicies mit Regionen1 als FailoverPriority 1, Region2 als FailoverPriority 2 und Seen3 als FailoverPriority 3 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="605c0-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="605c0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="605c0-113">PARAMETERS</span></span>

### <span data-ttu-id="605c0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="605c0-114">-AsJob</span></span>
<span data-ttu-id="605c0-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="605c0-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="605c0-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="605c0-116">-Confirm</span></span>
<span data-ttu-id="605c0-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="605c0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="605c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="605c0-118">-DefaultProfile</span></span>
<span data-ttu-id="605c0-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="605c0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="605c0-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="605c0-120">-FailoverPolicy</span></span>
<span data-ttu-id="605c0-121">Array von Zeichenfolgen mit Bereichsnamen, sortiert nach Failover-Priorität.</span><span class="sxs-lookup"><span data-stu-id="605c0-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="605c0-122">Z. b. eastus, westus</span><span class="sxs-lookup"><span data-stu-id="605c0-122">E.g eastus, westus</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="605c0-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="605c0-123">-InputObject</span></span>
<span data-ttu-id="605c0-124">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="605c0-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="605c0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="605c0-125">-Name</span></span>
<span data-ttu-id="605c0-126">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="605c0-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="605c0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="605c0-127">-ResourceGroupName</span></span>
<span data-ttu-id="605c0-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="605c0-128">Name of resource group.</span></span>

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

### <span data-ttu-id="605c0-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="605c0-129">-ResourceId</span></span>
<span data-ttu-id="605c0-130">Ressourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="605c0-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="605c0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="605c0-131">-WhatIf</span></span>
<span data-ttu-id="605c0-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="605c0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="605c0-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="605c0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="605c0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605c0-134">CommonParameters</span></span>
<span data-ttu-id="605c0-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="605c0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605c0-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="605c0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605c0-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="605c0-137">INPUTS</span></span>

### <span data-ttu-id="605c0-138">Keine</span><span class="sxs-lookup"><span data-stu-id="605c0-138">None</span></span>

## <span data-ttu-id="605c0-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="605c0-139">OUTPUTS</span></span>

### <span data-ttu-id="605c0-140">System. void</span><span class="sxs-lookup"><span data-stu-id="605c0-140">System.Void</span></span>

## <span data-ttu-id="605c0-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="605c0-141">NOTES</span></span>

## <span data-ttu-id="605c0-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="605c0-142">RELATED LINKS</span></span>
