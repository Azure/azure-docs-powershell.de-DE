---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 2d3555d879d05e1235fb8713e75c9b27fca46b51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947955"
---
# <span data-ttu-id="2fb67-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="2fb67-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="2fb67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fb67-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb67-103">{{ Ausfüllen der Synopsis }}</span><span class="sxs-lookup"><span data-stu-id="2fb67-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="2fb67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fb67-104">SYNTAX</span></span>

### <span data-ttu-id="2fb67-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2fb67-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fb67-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fb67-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fb67-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fb67-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fb67-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fb67-108">DESCRIPTION</span></span>
<span data-ttu-id="2fb67-109">{{ Ausfüllen der Beschreibung }}</span><span class="sxs-lookup"><span data-stu-id="2fb67-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="2fb67-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2fb67-110">EXAMPLES</span></span>

### <span data-ttu-id="2fb67-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2fb67-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="2fb67-112">FailoverPolicies mit Region1 als FailoverPriority 1, Region2 als FailoverPriority 2 und Region3 als FailoverPriority 3 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2fb67-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="2fb67-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2fb67-113">PARAMETERS</span></span>

### <span data-ttu-id="2fb67-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fb67-114">-AsJob</span></span>
<span data-ttu-id="2fb67-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2fb67-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fb67-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2fb67-116">-Confirm</span></span>
<span data-ttu-id="2fb67-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fb67-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fb67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb67-118">-DefaultProfile</span></span>
<span data-ttu-id="2fb67-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fb67-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fb67-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="2fb67-120">-FailoverPolicy</span></span>
<span data-ttu-id="2fb67-121">Array von Zeichenfolgen mit Regionnamen, nach Failoverpriorität geordnet.</span><span class="sxs-lookup"><span data-stu-id="2fb67-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="2fb67-122">Z. B. eastus, westus</span><span class="sxs-lookup"><span data-stu-id="2fb67-122">E.g eastus, westus</span></span>

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

### <span data-ttu-id="2fb67-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fb67-123">-InputObject</span></span>
<span data-ttu-id="2fb67-124">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="2fb67-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="2fb67-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2fb67-125">-Name</span></span>
<span data-ttu-id="2fb67-126">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="2fb67-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2fb67-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fb67-127">-ResourceGroupName</span></span>
<span data-ttu-id="2fb67-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2fb67-128">Name of resource group.</span></span>

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

### <span data-ttu-id="2fb67-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fb67-129">-ResourceId</span></span>
<span data-ttu-id="2fb67-130">ResourceId der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2fb67-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="2fb67-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fb67-131">-WhatIf</span></span>
<span data-ttu-id="2fb67-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fb67-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fb67-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fb67-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fb67-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb67-134">CommonParameters</span></span>
<span data-ttu-id="2fb67-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fb67-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb67-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fb67-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb67-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2fb67-137">INPUTS</span></span>

### <span data-ttu-id="2fb67-138">Keine</span><span class="sxs-lookup"><span data-stu-id="2fb67-138">None</span></span>

## <span data-ttu-id="2fb67-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2fb67-139">OUTPUTS</span></span>

### <span data-ttu-id="2fb67-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="2fb67-140">System.Void</span></span>

## <span data-ttu-id="2fb67-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2fb67-141">NOTES</span></span>

## <span data-ttu-id="2fb67-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2fb67-142">RELATED LINKS</span></span>
