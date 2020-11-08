---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175626"
---
# <span data-ttu-id="20791-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="20791-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="20791-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20791-102">SYNOPSIS</span></span>
<span data-ttu-id="20791-103">Erstellt einen Funktions-APP-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="20791-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="20791-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20791-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20791-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20791-105">DESCRIPTION</span></span>
<span data-ttu-id="20791-106">Erstellt einen Funktions-APP-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="20791-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="20791-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20791-107">EXAMPLES</span></span>

### <span data-ttu-id="20791-108">Beispiel 1: Erstellen eines Windows Premium-App-Plans in West Europa mit Kapazitäts Ausbrüchen bis zu 10 Instanzen.</span><span class="sxs-lookup"><span data-stu-id="20791-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="20791-109">Mit diesem Befehl wird ein Windows Premium-App-Plan in West Europa erstellt, in dem bis zu 10 Instanzen platzen können.</span><span class="sxs-lookup"><span data-stu-id="20791-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="20791-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="20791-110">PARAMETERS</span></span>

### <span data-ttu-id="20791-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20791-111">-AsJob</span></span>
<span data-ttu-id="20791-112">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="20791-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="20791-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20791-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="20791-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="20791-114">-Location</span></span>
<span data-ttu-id="20791-115">Der Speicherort für den Verbrauchs Plan.</span><span class="sxs-lookup"><span data-stu-id="20791-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="20791-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="20791-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="20791-117">Die maximale Anzahl von Arbeitskräften für den App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="20791-117">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="20791-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="20791-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="20791-119">Die Mindestanzahl von Arbeitskräften für den App-Service Plan.</span><span class="sxs-lookup"><span data-stu-id="20791-119">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="20791-120">-Name</span><span class="sxs-lookup"><span data-stu-id="20791-120">-Name</span></span>
<span data-ttu-id="20791-121">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="20791-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="20791-122">-Nowait</span><span class="sxs-lookup"><span data-stu-id="20791-122">-NoWait</span></span>
<span data-ttu-id="20791-123">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="20791-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="20791-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20791-124">-ResourceGroupName</span></span>
<span data-ttu-id="20791-125">Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="20791-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="20791-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="20791-126">-Sku</span></span>
<span data-ttu-id="20791-127">Die Plan-SKU.</span><span class="sxs-lookup"><span data-stu-id="20791-127">The plan sku.</span></span>
<span data-ttu-id="20791-128">Gültige Eingaben sind: EP1, ep2, EP3</span><span class="sxs-lookup"><span data-stu-id="20791-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="20791-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="20791-129">-SubscriptionId</span></span>
<span data-ttu-id="20791-130">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="20791-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="20791-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="20791-131">-Tag</span></span>
<span data-ttu-id="20791-132">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="20791-132">Resource tags.</span></span>

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

### <span data-ttu-id="20791-133">-Workertype</span><span class="sxs-lookup"><span data-stu-id="20791-133">-WorkerType</span></span>
<span data-ttu-id="20791-134">Der Worker-Typ für den Plan.</span><span class="sxs-lookup"><span data-stu-id="20791-134">The worker type for the plan.</span></span>
<span data-ttu-id="20791-135">Gültige Eingaben sind: Windows oder Linux.</span><span class="sxs-lookup"><span data-stu-id="20791-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="20791-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20791-136">-Confirm</span></span>
<span data-ttu-id="20791-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20791-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20791-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20791-138">-WhatIf</span></span>
<span data-ttu-id="20791-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20791-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20791-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20791-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20791-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20791-141">CommonParameters</span></span>
<span data-ttu-id="20791-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20791-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20791-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20791-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20791-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20791-144">INPUTS</span></span>

## <span data-ttu-id="20791-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20791-145">OUTPUTS</span></span>

### <span data-ttu-id="20791-146">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="20791-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="20791-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="20791-147">NOTES</span></span>

<span data-ttu-id="20791-148">Aliase</span><span class="sxs-lookup"><span data-stu-id="20791-148">ALIASES</span></span>

## <span data-ttu-id="20791-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20791-149">RELATED LINKS</span></span>

