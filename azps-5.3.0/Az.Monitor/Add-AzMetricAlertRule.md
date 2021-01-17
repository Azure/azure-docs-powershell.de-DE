---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: cb3669c955182e54b6ddd3623f732402a15ea906
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470027"
---
# <span data-ttu-id="2e6de-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="2e6de-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="2e6de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e6de-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6de-103">Fügt eine metrisch-basierte Warnungsregel hinzu oder aktualisiert diese.</span><span class="sxs-lookup"><span data-stu-id="2e6de-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="2e6de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e6de-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e6de-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e6de-105">DESCRIPTION</span></span>
<span data-ttu-id="2e6de-106">Das **Cmdlet "Add-AzMetricAlertRule"** fügt eine metrisch-basierte Warnungsregel hinzu bzw. aktualisiert diese.</span><span class="sxs-lookup"><span data-stu-id="2e6de-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="2e6de-107">Die hinzugefügte Regel ist einer Ressourcengruppe zugeordnet und hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="2e6de-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="2e6de-108">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung vom Benutzer anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2e6de-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="2e6de-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2e6de-109">EXAMPLES</span></span>

### <span data-ttu-id="2e6de-110">Beispiel 1: Hinzufügen einer metrischen Warnungsregel zu einer Website</span><span class="sxs-lookup"><span data-stu-id="2e6de-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="2e6de-111">Mit diesem Befehl wird eine metrische Warnungsregel für eine Website erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e6de-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="2e6de-112">Beispiel 2: Deaktivieren einer Regel</span><span class="sxs-lookup"><span data-stu-id="2e6de-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="2e6de-113">Mit diesem Befehl wird eine Regel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2e6de-113">This command disables a rule.</span></span>
<span data-ttu-id="2e6de-114">Wenn die Regel nicht vorhanden ist, wird sie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2e6de-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="2e6de-115">Wenn die Regel vorhanden ist, wird sie einfach deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2e6de-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="2e6de-116">Beispiel 3: Hinzufügen einer Regel mit Aktionen</span><span class="sxs-lookup"><span data-stu-id="2e6de-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="2e6de-117">Mit diesem Befehl wird eine metrische Warnungsregel für eine Website erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e6de-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="2e6de-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e6de-118">PARAMETERS</span></span>

### <span data-ttu-id="2e6de-119">-Aktion</span><span class="sxs-lookup"><span data-stu-id="2e6de-119">-Action</span></span>
<span data-ttu-id="2e6de-120">Gibt eine durch Kommas getrennte Liste von Aktionen an.</span><span class="sxs-lookup"><span data-stu-id="2e6de-120">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6de-121">-DefaultProfile</span></span>
<span data-ttu-id="2e6de-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2e6de-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e6de-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e6de-123">-Description</span></span>
<span data-ttu-id="2e6de-124">Gibt eine Beschreibung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="2e6de-124">Specifies a description of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6de-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="2e6de-125">-DisableRule</span></span>
<span data-ttu-id="2e6de-126">Deaktiviert die Regel.</span><span class="sxs-lookup"><span data-stu-id="2e6de-126">Disables the rule.</span></span>
<span data-ttu-id="2e6de-127">Wenn Sie diesen Parameter nicht angeben, ist die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2e6de-127">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6de-128">-Location</span><span class="sxs-lookup"><span data-stu-id="2e6de-128">-Location</span></span>
<span data-ttu-id="2e6de-129">Gibt den Speicherort an, an dem die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="2e6de-129">Specifies the location where the rule is defined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6de-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="2e6de-130">-MetricName</span></span>
<span data-ttu-id="2e6de-131">Gibt den Namen der Metrik an, die von der Regel überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="2e6de-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="2e6de-132">Geben Sie diesen Parameter nur für metrische Regeln an.</span><span class="sxs-lookup"><span data-stu-id="2e6de-132">Specify this parameter only for metric-based rules.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6de-133">-Name</span><span class="sxs-lookup"><span data-stu-id="2e6de-133">-Name</span></span>
<span data-ttu-id="2e6de-134">Gibt den Namen der Regel an.</span><span class="sxs-lookup"><span data-stu-id="2e6de-134">Specifies the name of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6de-135">-Operator</span><span class="sxs-lookup"><span data-stu-id="2e6de-135">-Operator</span></span>
<span data-ttu-id="2e6de-136">Gibt den relationalen Operator für die Bedingung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="2e6de-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="2e6de-137">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="2e6de-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2e6de-138">Greater Durchf</span><span class="sxs-lookup"><span data-stu-id="2e6de-138">GreaterThan</span></span>
- <span data-ttu-id="2e6de-139">GreaterHanaOrEqual</span><span class="sxs-lookup"><span data-stu-id="2e6de-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="2e6de-140">Less Immer</span><span class="sxs-lookup"><span data-stu-id="2e6de-140">LessThan</span></span>
- <span data-ttu-id="2e6de-141">LessHanaOrEqual</span><span class="sxs-lookup"><span data-stu-id="2e6de-141">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6de-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e6de-142">-ResourceGroupName</span></span>
<span data-ttu-id="2e6de-143">Gibt den Namen der Ressourcengruppe für die Regel an.</span><span class="sxs-lookup"><span data-stu-id="2e6de-143">Specifies the name of the resource group for the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6de-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2e6de-144">-TargetResourceId</span></span>
<span data-ttu-id="2e6de-145">Gibt die ID der Ressource an, die von der Regel überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="2e6de-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="2e6de-146">HINWEIS: Diese Eigenschaft kann für eine vorhandene Warnungsregel nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2e6de-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6de-147">-Threshold</span><span class="sxs-lookup"><span data-stu-id="2e6de-147">-Threshold</span></span>
<span data-ttu-id="2e6de-148">Gibt den Schwellenwert für die Regel an.</span><span class="sxs-lookup"><span data-stu-id="2e6de-148">Specifies the threshold of the rule.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6de-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="2e6de-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="2e6de-150">Gibt den Aggregationsoperator an, der auf das Zeitfenster angewendet werden soll, wenn die Regel ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="2e6de-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator]
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6de-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="2e6de-151">-WindowSize</span></span>
<span data-ttu-id="2e6de-152">Gibt die Zeitfenstergröße für die Regel an, deren Daten berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="2e6de-152">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6de-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e6de-153">-Confirm</span></span>
<span data-ttu-id="2e6de-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e6de-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e6de-155">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2e6de-155">-WhatIf</span></span>
<span data-ttu-id="2e6de-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e6de-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e6de-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e6de-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e6de-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6de-158">CommonParameters</span></span>
<span data-ttu-id="2e6de-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e6de-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6de-160">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e6de-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6de-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2e6de-161">INPUTS</span></span>

### <span data-ttu-id="2e6de-162">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="2e6de-162">System.TimeSpan</span></span>

### <span data-ttu-id="2e6de-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="2e6de-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="2e6de-164">System.Double</span><span class="sxs-lookup"><span data-stu-id="2e6de-164">System.Double</span></span>

### <span data-ttu-id="2e6de-165">System.String</span><span class="sxs-lookup"><span data-stu-id="2e6de-165">System.String</span></span>

### <span data-ttu-id="2e6de-166">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="2e6de-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2e6de-167">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e6de-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2e6de-168">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="2e6de-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2e6de-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2e6de-169">OUTPUTS</span></span>

### <span data-ttu-id="2e6de-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2e6de-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="2e6de-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2e6de-171">NOTES</span></span>

## <span data-ttu-id="2e6de-172">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2e6de-172">RELATED LINKS</span></span>

[<span data-ttu-id="2e6de-173">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e6de-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="2e6de-174">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="2e6de-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="2e6de-175">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="2e6de-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="2e6de-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="2e6de-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="2e6de-177">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="2e6de-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="2e6de-178">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="2e6de-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="2e6de-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="2e6de-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


