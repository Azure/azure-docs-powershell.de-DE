---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 3a58102eb3a0fa92b176e75135c1170cd621278e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822692"
---
# <span data-ttu-id="0fd02-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0fd02-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="0fd02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0fd02-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd02-103">Erstellt eine Protokoll Warnungsregel (geplanter Abfrage Regeltyp)</span><span class="sxs-lookup"><span data-stu-id="0fd02-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="0fd02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fd02-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fd02-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fd02-105">DESCRIPTION</span></span>
<span data-ttu-id="0fd02-106">Erstellt eine Protokoll Warnungsregel (geplanter Abfrage Regeltyp)</span><span class="sxs-lookup"><span data-stu-id="0fd02-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="0fd02-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fd02-107">EXAMPLES</span></span>

### <span data-ttu-id="0fd02-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0fd02-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="0fd02-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fd02-109">PARAMETERS</span></span>

### <span data-ttu-id="0fd02-110">– Aktion</span><span class="sxs-lookup"><span data-stu-id="0fd02-110">-Action</span></span>
<span data-ttu-id="0fd02-111">Warnungsaktion für geplante Abfrageregel</span><span class="sxs-lookup"><span data-stu-id="0fd02-111">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="0fd02-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fd02-112">-AsJob</span></span>
<span data-ttu-id="0fd02-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0fd02-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fd02-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd02-114">-DefaultProfile</span></span>
<span data-ttu-id="0fd02-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0fd02-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fd02-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fd02-116">-Description</span></span>
<span data-ttu-id="0fd02-117">Die Beschreibung für diese Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="0fd02-117">The description for this alert</span></span>

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

### <span data-ttu-id="0fd02-118">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="0fd02-118">-Enabled</span></span>
<span data-ttu-id="0fd02-119">Der Azure-Warnungszustand – gültige Werte – $true, $false</span><span class="sxs-lookup"><span data-stu-id="0fd02-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="0fd02-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="0fd02-120">-Location</span></span>
<span data-ttu-id="0fd02-121">Der Speicherort für diese Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="0fd02-121">The location for this alert</span></span>

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

### <span data-ttu-id="0fd02-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0fd02-122">-Name</span></span>
<span data-ttu-id="0fd02-123">Der Warnungsname</span><span class="sxs-lookup"><span data-stu-id="0fd02-123">The alert name</span></span>

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

### <span data-ttu-id="0fd02-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fd02-124">-ResourceGroupName</span></span>
<span data-ttu-id="0fd02-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0fd02-125">The resource group name</span></span>

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

### <span data-ttu-id="0fd02-126">-Terminplan</span><span class="sxs-lookup"><span data-stu-id="0fd02-126">-Schedule</span></span>
<span data-ttu-id="0fd02-127">Zeitplan für regelmäßige Abfrageregeln</span><span class="sxs-lookup"><span data-stu-id="0fd02-127">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="0fd02-128">-Source</span><span class="sxs-lookup"><span data-stu-id="0fd02-128">-Source</span></span>
<span data-ttu-id="0fd02-129">Die geplante Abfrageregel Quelle</span><span class="sxs-lookup"><span data-stu-id="0fd02-129">The scheduled query rule source</span></span>

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

### <span data-ttu-id="0fd02-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="0fd02-130">-Tag</span></span>
<span data-ttu-id="0fd02-131">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="0fd02-131">Resource tags</span></span>

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

### <span data-ttu-id="0fd02-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0fd02-132">-Confirm</span></span>
<span data-ttu-id="0fd02-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0fd02-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fd02-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fd02-134">-WhatIf</span></span>
<span data-ttu-id="0fd02-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fd02-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fd02-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fd02-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fd02-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd02-137">CommonParameters</span></span>
<span data-ttu-id="0fd02-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fd02-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd02-139">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fd02-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd02-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0fd02-140">INPUTS</span></span>

### <span data-ttu-id="0fd02-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0fd02-141">System.String</span></span>

## <span data-ttu-id="0fd02-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0fd02-142">OUTPUTS</span></span>

### <span data-ttu-id="0fd02-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="0fd02-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="0fd02-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="0fd02-144">NOTES</span></span>

## <span data-ttu-id="0fd02-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0fd02-145">RELATED LINKS</span></span>
