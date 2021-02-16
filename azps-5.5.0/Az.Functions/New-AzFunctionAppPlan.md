---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163508"
---
# <span data-ttu-id="923c4-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="923c4-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="923c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="923c4-102">SYNOPSIS</span></span>
<span data-ttu-id="923c4-103">Erstellt einen Funktions-App-Serviceplan.</span><span class="sxs-lookup"><span data-stu-id="923c4-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="923c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="923c4-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="923c4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="923c4-105">DESCRIPTION</span></span>
<span data-ttu-id="923c4-106">Erstellt einen Funktions-App-Serviceplan.</span><span class="sxs-lookup"><span data-stu-id="923c4-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="923c4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="923c4-107">EXAMPLES</span></span>

### <span data-ttu-id="923c4-108">Beispiel 1: Erstellen Sie einen Windows Premium-App-Plan in Westeuropa mit platzend funktionen bis zu 10 Instanzen.</span><span class="sxs-lookup"><span data-stu-id="923c4-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="923c4-109">Mit diesem Befehl wird ein Windows Premium-App-Plan in Westeuropa mit ausser geplatzten Funktionen bis zu 10 Instanzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="923c4-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="923c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="923c4-110">PARAMETERS</span></span>

### <span data-ttu-id="923c4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="923c4-111">-AsJob</span></span>
<span data-ttu-id="923c4-112">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="923c4-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="923c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="923c4-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="923c4-114">-Location</span><span class="sxs-lookup"><span data-stu-id="923c4-114">-Location</span></span>
<span data-ttu-id="923c4-115">Der Standort für den Verbrauchsplan.</span><span class="sxs-lookup"><span data-stu-id="923c4-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="923c4-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="923c4-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="923c4-117">Die maximale Anzahl von Mitarbeitern für den App-Serviceplan.</span><span class="sxs-lookup"><span data-stu-id="923c4-117">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="923c4-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="923c4-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="923c4-119">Die Mindestanzahl von Mitarbeitern für den App-Serviceplan.</span><span class="sxs-lookup"><span data-stu-id="923c4-119">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="923c4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="923c4-120">-Name</span></span>
<span data-ttu-id="923c4-121">Name des App-Service-Plans.</span><span class="sxs-lookup"><span data-stu-id="923c4-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="923c4-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="923c4-122">-NoWait</span></span>
<span data-ttu-id="923c4-123">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="923c4-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="923c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="923c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="923c4-125">Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="923c4-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="923c4-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="923c4-126">-Sku</span></span>
<span data-ttu-id="923c4-127">Die SKU des Plans.</span><span class="sxs-lookup"><span data-stu-id="923c4-127">The plan sku.</span></span>
<span data-ttu-id="923c4-128">Gültige Eingaben sind: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="923c4-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="923c4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="923c4-129">-SubscriptionId</span></span>
<span data-ttu-id="923c4-130">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="923c4-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="923c4-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="923c4-131">-Tag</span></span>
<span data-ttu-id="923c4-132">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="923c4-132">Resource tags.</span></span>

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

### <span data-ttu-id="923c4-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="923c4-133">-WorkerType</span></span>
<span data-ttu-id="923c4-134">Der Workertyp für den Plan.</span><span class="sxs-lookup"><span data-stu-id="923c4-134">The worker type for the plan.</span></span>
<span data-ttu-id="923c4-135">Gültige Eingaben sind: Windows oder Linux.</span><span class="sxs-lookup"><span data-stu-id="923c4-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="923c4-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="923c4-136">-Confirm</span></span>
<span data-ttu-id="923c4-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="923c4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="923c4-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="923c4-138">-WhatIf</span></span>
<span data-ttu-id="923c4-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="923c4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="923c4-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="923c4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="923c4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="923c4-141">CommonParameters</span></span>
<span data-ttu-id="923c4-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="923c4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="923c4-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="923c4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="923c4-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="923c4-144">INPUTS</span></span>

## <span data-ttu-id="923c4-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="923c4-145">OUTPUTS</span></span>

### <span data-ttu-id="923c4-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="923c4-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="923c4-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="923c4-147">NOTES</span></span>

<span data-ttu-id="923c4-148">ALIASE</span><span class="sxs-lookup"><span data-stu-id="923c4-148">ALIASES</span></span>

## <span data-ttu-id="923c4-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="923c4-149">RELATED LINKS</span></span>

