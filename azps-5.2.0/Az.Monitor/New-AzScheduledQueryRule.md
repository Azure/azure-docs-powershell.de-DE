---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293525"
---
# <span data-ttu-id="a3394-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a3394-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="a3394-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3394-102">SYNOPSIS</span></span>
<span data-ttu-id="a3394-103">Erstellt eine Protokollwarnungsregel (Typ der geplanten Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="a3394-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="a3394-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3394-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3394-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3394-105">DESCRIPTION</span></span>
<span data-ttu-id="a3394-106">Erstellt eine Protokollwarnungsregel (Typ der geplanten Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="a3394-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="a3394-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3394-107">EXAMPLES</span></span>

### <span data-ttu-id="a3394-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3394-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="a3394-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3394-109">PARAMETERS</span></span>

### <span data-ttu-id="a3394-110">-Action</span><span class="sxs-lookup"><span data-stu-id="a3394-110">-Action</span></span>
<span data-ttu-id="a3394-111">Benachrichtigungsaktion für die geplante Abfrageregel</span><span class="sxs-lookup"><span data-stu-id="a3394-111">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3394-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3394-112">-AsJob</span></span>
<span data-ttu-id="a3394-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a3394-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3394-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3394-114">-DefaultProfile</span></span>
<span data-ttu-id="a3394-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3394-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3394-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3394-116">-Description</span></span>
<span data-ttu-id="a3394-117">Die Beschreibung für diese Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="a3394-117">The description for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3394-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="a3394-118">-Enabled</span></span>
<span data-ttu-id="a3394-119">Der Azure Alert State – gültige Werte – $true, $false</span><span class="sxs-lookup"><span data-stu-id="a3394-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3394-120">-Location</span><span class="sxs-lookup"><span data-stu-id="a3394-120">-Location</span></span>
<span data-ttu-id="a3394-121">Der Speicherort für diese Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="a3394-121">The location for this alert</span></span>

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

### <span data-ttu-id="a3394-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a3394-122">-Name</span></span>
<span data-ttu-id="a3394-123">Der Benachrichtigungsname</span><span class="sxs-lookup"><span data-stu-id="a3394-123">The alert name</span></span>

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

### <span data-ttu-id="a3394-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3394-124">-ResourceGroupName</span></span>
<span data-ttu-id="a3394-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a3394-125">The resource group name</span></span>

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

### <span data-ttu-id="a3394-126">-Schedule</span><span class="sxs-lookup"><span data-stu-id="a3394-126">-Schedule</span></span>
<span data-ttu-id="a3394-127">Der Zeitplan für geplante Abfrageregel</span><span class="sxs-lookup"><span data-stu-id="a3394-127">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3394-128">-Source</span><span class="sxs-lookup"><span data-stu-id="a3394-128">-Source</span></span>
<span data-ttu-id="a3394-129">Quelle der geplanten Abfrageregel</span><span class="sxs-lookup"><span data-stu-id="a3394-129">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3394-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a3394-130">-Tag</span></span>
<span data-ttu-id="a3394-131">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="a3394-131">Resource tags</span></span>

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

### <span data-ttu-id="a3394-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3394-132">-Confirm</span></span>
<span data-ttu-id="a3394-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3394-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3394-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a3394-134">-WhatIf</span></span>
<span data-ttu-id="a3394-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3394-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3394-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3394-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3394-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3394-137">CommonParameters</span></span>
<span data-ttu-id="a3394-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3394-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3394-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3394-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3394-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3394-140">INPUTS</span></span>

### <span data-ttu-id="a3394-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a3394-141">System.String</span></span>

## <span data-ttu-id="a3394-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3394-142">OUTPUTS</span></span>

### <span data-ttu-id="a3394-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="a3394-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="a3394-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a3394-144">NOTES</span></span>

## <span data-ttu-id="a3394-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a3394-145">RELATED LINKS</span></span>
