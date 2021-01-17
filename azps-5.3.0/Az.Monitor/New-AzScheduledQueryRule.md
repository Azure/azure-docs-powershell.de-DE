---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472297"
---
# <span data-ttu-id="70aa4-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="70aa4-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="70aa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="70aa4-103">Erstellt eine Protokollwarnungsregel (Typ der geplanten Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="70aa4-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="70aa4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70aa4-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70aa4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="70aa4-106">Erstellt eine Protokollwarnungsregel (Typ der geplanten Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="70aa4-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="70aa4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70aa4-107">EXAMPLES</span></span>

### <span data-ttu-id="70aa4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70aa4-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="70aa4-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70aa4-109">PARAMETERS</span></span>

### <span data-ttu-id="70aa4-110">-Aktion</span><span class="sxs-lookup"><span data-stu-id="70aa4-110">-Action</span></span>
<span data-ttu-id="70aa4-111">Benachrichtigungsaktion für die geplante Abfrageregel</span><span class="sxs-lookup"><span data-stu-id="70aa4-111">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="70aa4-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70aa4-112">-AsJob</span></span>
<span data-ttu-id="70aa4-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="70aa4-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70aa4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70aa4-114">-DefaultProfile</span></span>
<span data-ttu-id="70aa4-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70aa4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70aa4-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70aa4-116">-Description</span></span>
<span data-ttu-id="70aa4-117">Die Beschreibung für diese Warnung</span><span class="sxs-lookup"><span data-stu-id="70aa4-117">The description for this alert</span></span>

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

### <span data-ttu-id="70aa4-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="70aa4-118">-Enabled</span></span>
<span data-ttu-id="70aa4-119">Der Azure Alert State – gültige Werte – $true, $false</span><span class="sxs-lookup"><span data-stu-id="70aa4-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="70aa4-120">-Location</span><span class="sxs-lookup"><span data-stu-id="70aa4-120">-Location</span></span>
<span data-ttu-id="70aa4-121">Der Speicherort für diese Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="70aa4-121">The location for this alert</span></span>

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

### <span data-ttu-id="70aa4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="70aa4-122">-Name</span></span>
<span data-ttu-id="70aa4-123">Der Benachrichtigungsname</span><span class="sxs-lookup"><span data-stu-id="70aa4-123">The alert name</span></span>

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

### <span data-ttu-id="70aa4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70aa4-124">-ResourceGroupName</span></span>
<span data-ttu-id="70aa4-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="70aa4-125">The resource group name</span></span>

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

### <span data-ttu-id="70aa4-126">-Schedule</span><span class="sxs-lookup"><span data-stu-id="70aa4-126">-Schedule</span></span>
<span data-ttu-id="70aa4-127">Der Zeitplan für geplante Abfrageregel</span><span class="sxs-lookup"><span data-stu-id="70aa4-127">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="70aa4-128">-Source</span><span class="sxs-lookup"><span data-stu-id="70aa4-128">-Source</span></span>
<span data-ttu-id="70aa4-129">Quelle der geplanten Abfrageregel</span><span class="sxs-lookup"><span data-stu-id="70aa4-129">The scheduled query rule source</span></span>

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

### <span data-ttu-id="70aa4-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="70aa4-130">-Tag</span></span>
<span data-ttu-id="70aa4-131">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="70aa4-131">Resource tags</span></span>

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

### <span data-ttu-id="70aa4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70aa4-132">-Confirm</span></span>
<span data-ttu-id="70aa4-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70aa4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70aa4-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="70aa4-134">-WhatIf</span></span>
<span data-ttu-id="70aa4-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70aa4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70aa4-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70aa4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70aa4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70aa4-137">CommonParameters</span></span>
<span data-ttu-id="70aa4-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70aa4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70aa4-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70aa4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70aa4-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70aa4-140">INPUTS</span></span>

### <span data-ttu-id="70aa4-141">System.String</span><span class="sxs-lookup"><span data-stu-id="70aa4-141">System.String</span></span>

## <span data-ttu-id="70aa4-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70aa4-142">OUTPUTS</span></span>

### <span data-ttu-id="70aa4-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="70aa4-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="70aa4-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="70aa4-144">NOTES</span></span>

## <span data-ttu-id="70aa4-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="70aa4-145">RELATED LINKS</span></span>
