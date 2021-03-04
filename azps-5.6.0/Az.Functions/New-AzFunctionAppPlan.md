---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 465c4b366990bb69d437fbdbe51fe2c5f4316758
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927128"
---
# <span data-ttu-id="427f4-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="427f4-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="427f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="427f4-102">SYNOPSIS</span></span>
<span data-ttu-id="427f4-103">Erstellt einen Funktions-App-Dienstplan.</span><span class="sxs-lookup"><span data-stu-id="427f4-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="427f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="427f4-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="427f4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="427f4-105">DESCRIPTION</span></span>
<span data-ttu-id="427f4-106">Erstellt einen Funktions-App-Dienstplan.</span><span class="sxs-lookup"><span data-stu-id="427f4-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="427f4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="427f4-107">EXAMPLES</span></span>

### <span data-ttu-id="427f4-108">Beispiel 1: Erstellen Sie einen Windows Premium-App-Plan in Westeuropa mit einer Burst-out-Funktion von bis zu 10 Instanzen.</span><span class="sxs-lookup"><span data-stu-id="427f4-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="427f4-109">Mit diesem Befehl wird ein Windows Premium-App-Plan in Westeuropa mit einer Burst-Out-Funktion von bis zu 10 Instanzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="427f4-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="427f4-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="427f4-110">PARAMETERS</span></span>

### <span data-ttu-id="427f4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="427f4-111">-AsJob</span></span>
<span data-ttu-id="427f4-112">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="427f4-112">Run the command as a job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="427f4-113">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-114">-Location</span><span class="sxs-lookup"><span data-stu-id="427f4-114">-Location</span></span>
<span data-ttu-id="427f4-115">Der Speicherort für den Verbrauchsplan.</span><span class="sxs-lookup"><span data-stu-id="427f4-115">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="427f4-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="427f4-117">Die maximale Anzahl von Mitarbeitern für den App-Dienstplan.</span><span class="sxs-lookup"><span data-stu-id="427f4-117">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="427f4-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="427f4-119">Die Mindestanzahl von Mitarbeitern für den App-Dienstplan.</span><span class="sxs-lookup"><span data-stu-id="427f4-119">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="427f4-120">-Name</span></span>
<span data-ttu-id="427f4-121">Name des App Service-Plans.</span><span class="sxs-lookup"><span data-stu-id="427f4-121">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="427f4-122">-NoWait</span></span>
<span data-ttu-id="427f4-123">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="427f4-123">Run the command asynchronously.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="427f4-124">-ResourceGroupName</span></span>
<span data-ttu-id="427f4-125">Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="427f4-125">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="427f4-126">-Sku</span></span>
<span data-ttu-id="427f4-127">Die Sku des Plans.</span><span class="sxs-lookup"><span data-stu-id="427f4-127">The plan sku.</span></span>
<span data-ttu-id="427f4-128">Gültige Eingaben sind: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="427f4-128">Valid inputs are: EP1, EP2, EP3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="427f4-129">-SubscriptionId</span></span>
<span data-ttu-id="427f4-130">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="427f4-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="427f4-131">-Tag</span></span>
<span data-ttu-id="427f4-132">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="427f4-132">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="427f4-133">-WorkerType</span></span>
<span data-ttu-id="427f4-134">Der Workertyp für den Plan.</span><span class="sxs-lookup"><span data-stu-id="427f4-134">The worker type for the plan.</span></span>
<span data-ttu-id="427f4-135">Gültige Eingaben sind: Windows oder Linux.</span><span class="sxs-lookup"><span data-stu-id="427f4-135">Valid inputs are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="427f4-136">-Confirm</span></span>
<span data-ttu-id="427f4-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="427f4-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="427f4-138">-WhatIf</span></span>
<span data-ttu-id="427f4-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="427f4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="427f4-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="427f4-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427f4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="427f4-141">CommonParameters</span></span>
<span data-ttu-id="427f4-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="427f4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="427f4-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="427f4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="427f4-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="427f4-144">INPUTS</span></span>

## <span data-ttu-id="427f4-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="427f4-145">OUTPUTS</span></span>

### <span data-ttu-id="427f4-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="427f4-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="427f4-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="427f4-147">NOTES</span></span>

<span data-ttu-id="427f4-148">ALIASE</span><span class="sxs-lookup"><span data-stu-id="427f4-148">ALIASES</span></span>

## <span data-ttu-id="427f4-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="427f4-149">RELATED LINKS</span></span>

