---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: cb3669c955182e54b6ddd3623f732402a15ea906
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009209"
---
# <span data-ttu-id="e36d0-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e36d0-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="e36d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e36d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e36d0-103">Fügt eine Metrik-basierte Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="e36d0-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="e36d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e36d0-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e36d0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e36d0-105">DESCRIPTION</span></span>
<span data-ttu-id="e36d0-106">Das **Add-AzMetricAlertRule-** Cmdlet fügt eine Metrik-basierte Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="e36d0-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="e36d0-107">Die hinzugefügte Regel ist einer Ressourcengruppe zugeordnet und hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="e36d0-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="e36d0-108">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e36d0-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e36d0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e36d0-109">EXAMPLES</span></span>

### <span data-ttu-id="e36d0-110">Beispiel 1: Hinzufügen einer Metrik-Warnungsregel zu einer Website</span><span class="sxs-lookup"><span data-stu-id="e36d0-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="e36d0-111">Dieser Befehl erstellt eine Metrik-Warnungsregel für eine Website.</span><span class="sxs-lookup"><span data-stu-id="e36d0-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="e36d0-112">Beispiel 2: Deaktivieren einer Regel</span><span class="sxs-lookup"><span data-stu-id="e36d0-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="e36d0-113">Mit diesem Befehl wird eine Regel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e36d0-113">This command disables a rule.</span></span>
<span data-ttu-id="e36d0-114">Wenn die Regel nicht vorhanden ist, wird Sie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e36d0-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="e36d0-115">Wenn die Regel vorhanden ist, wird Sie nur deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e36d0-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="e36d0-116">Beispiel 3: Hinzufügen einer Regel mit Aktionen</span><span class="sxs-lookup"><span data-stu-id="e36d0-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="e36d0-117">Dieser Befehl erstellt eine Metrik-Warnungsregel für eine Website.</span><span class="sxs-lookup"><span data-stu-id="e36d0-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="e36d0-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e36d0-118">PARAMETERS</span></span>

### <span data-ttu-id="e36d0-119">– Aktion</span><span class="sxs-lookup"><span data-stu-id="e36d0-119">-Action</span></span>
<span data-ttu-id="e36d0-120">Gibt eine durch trennzeichengetrennte Liste von Aktionen an.</span><span class="sxs-lookup"><span data-stu-id="e36d0-120">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="e36d0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36d0-121">-DefaultProfile</span></span>
<span data-ttu-id="e36d0-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e36d0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e36d0-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e36d0-123">-Description</span></span>
<span data-ttu-id="e36d0-124">Gibt eine Beschreibung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="e36d0-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="e36d0-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="e36d0-125">-DisableRule</span></span>
<span data-ttu-id="e36d0-126">Deaktiviert die Regel.</span><span class="sxs-lookup"><span data-stu-id="e36d0-126">Disables the rule.</span></span>
<span data-ttu-id="e36d0-127">Wenn Sie diesen Parameter nicht angeben, wird die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e36d0-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="e36d0-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="e36d0-128">-Location</span></span>
<span data-ttu-id="e36d0-129">Gibt den Ort an, an dem die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e36d0-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="e36d0-130">-Metricname</span><span class="sxs-lookup"><span data-stu-id="e36d0-130">-MetricName</span></span>
<span data-ttu-id="e36d0-131">Gibt den Namen der Metrik an, die die Regel überwacht.</span><span class="sxs-lookup"><span data-stu-id="e36d0-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="e36d0-132">Geben Sie diesen Parameter nur für metrische Regeln an.</span><span class="sxs-lookup"><span data-stu-id="e36d0-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="e36d0-133">-Name</span><span class="sxs-lookup"><span data-stu-id="e36d0-133">-Name</span></span>
<span data-ttu-id="e36d0-134">Gibt den Namen der Regel an.</span><span class="sxs-lookup"><span data-stu-id="e36d0-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="e36d0-135">-Operator</span><span class="sxs-lookup"><span data-stu-id="e36d0-135">-Operator</span></span>
<span data-ttu-id="e36d0-136">Gibt den relationalen Operator für die Bedingung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="e36d0-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="e36d0-137">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e36d0-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e36d0-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="e36d0-138">GreaterThan</span></span>
- <span data-ttu-id="e36d0-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="e36d0-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="e36d0-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="e36d0-140">LessThan</span></span>
- <span data-ttu-id="e36d0-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="e36d0-141">LessThanOrEqual</span></span>

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

### <span data-ttu-id="e36d0-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e36d0-142">-ResourceGroupName</span></span>
<span data-ttu-id="e36d0-143">Gibt den Namen der Ressourcengruppe für die Regel an.</span><span class="sxs-lookup"><span data-stu-id="e36d0-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="e36d0-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e36d0-144">-TargetResourceId</span></span>
<span data-ttu-id="e36d0-145">Gibt die ID der Ressource an, die von der Regel überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="e36d0-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="e36d0-146">Hinweis: Diese Eigenschaft kann für eine vorhandene Warnungsregel nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e36d0-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="e36d0-147">-Threshold</span><span class="sxs-lookup"><span data-stu-id="e36d0-147">-Threshold</span></span>
<span data-ttu-id="e36d0-148">Gibt den Schwellenwert für die Regel an.</span><span class="sxs-lookup"><span data-stu-id="e36d0-148">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="e36d0-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="e36d0-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="e36d0-150">Gibt den Aggregations Operator an, der auf das Zeitfenster angewendet werden soll, wenn die Regel ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="e36d0-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="e36d0-151">-Windowsisieren</span><span class="sxs-lookup"><span data-stu-id="e36d0-151">-WindowSize</span></span>
<span data-ttu-id="e36d0-152">Gibt die Zeitfenster Größe für die Regel an, um die Daten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="e36d0-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="e36d0-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e36d0-153">-Confirm</span></span>
<span data-ttu-id="e36d0-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e36d0-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e36d0-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e36d0-155">-WhatIf</span></span>
<span data-ttu-id="e36d0-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e36d0-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e36d0-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e36d0-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e36d0-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36d0-158">CommonParameters</span></span>
<span data-ttu-id="e36d0-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e36d0-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36d0-160">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e36d0-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36d0-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e36d0-161">INPUTS</span></span>

### <span data-ttu-id="e36d0-162">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="e36d0-162">System.TimeSpan</span></span>

### <span data-ttu-id="e36d0-163">Microsoft. Azure. Management. Monitor. Management. Models. ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="e36d0-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="e36d0-164">System. Double</span><span class="sxs-lookup"><span data-stu-id="e36d0-164">System.Double</span></span>

### <span data-ttu-id="e36d0-165">System. String</span><span class="sxs-lookup"><span data-stu-id="e36d0-165">System.String</span></span>

### <span data-ttu-id="e36d0-166">System. Nullable ' 1 [[Microsoft. Azure. Management. Monitor. Management. Models. TimeAggregationOperator, Microsoft. Azure. PowerShell. Cmdlets. Monitor, Version = 1.0.0.0, Kultur = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e36d0-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e36d0-167">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="e36d0-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e36d0-168">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Monitor. Management. Models. RuleAction, Microsoft. Azure. PowerShell. Cmdlets. Monitor, Version = 1.0.0.0, Kultur = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e36d0-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e36d0-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e36d0-169">OUTPUTS</span></span>

### <span data-ttu-id="e36d0-170">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e36d0-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="e36d0-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="e36d0-171">NOTES</span></span>

## <span data-ttu-id="e36d0-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e36d0-172">RELATED LINKS</span></span>

[<span data-ttu-id="e36d0-173">Satz-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e36d0-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="e36d0-174">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e36d0-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="e36d0-175">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="e36d0-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="e36d0-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="e36d0-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="e36d0-177">Neu – AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="e36d0-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="e36d0-178">Neu – AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e36d0-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="e36d0-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="e36d0-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


