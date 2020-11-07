---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermmetricalertrule
schema: 2.0.0
ms.openlocfilehash: a54be3a4879ebb2b4e8f880dd14bb50044a0820f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849331"
---
# <span data-ttu-id="47f8f-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="47f8f-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="47f8f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="47f8f-103">Fügt eine Metrik-basierte Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="47f8f-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47f8f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47f8f-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47f8f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47f8f-105">DESCRIPTION</span></span>
<span data-ttu-id="47f8f-106">Das **Add-AzureRmMetricAlertRule-** Cmdlet fügt eine Metrik-basierte Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="47f8f-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="47f8f-107">Die hinzugefügte Regel ist einer Ressourcengruppe zugeordnet und hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="47f8f-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="47f8f-108">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="47f8f-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="47f8f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47f8f-109">EXAMPLES</span></span>

### <span data-ttu-id="47f8f-110">Beispiel 1: Hinzufügen einer Metrik-Warnungsregel zu einer Website</span><span class="sxs-lookup"><span data-stu-id="47f8f-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="47f8f-111">Dieser Befehl erstellt eine Metrik-Warnungsregel für eine Website.</span><span class="sxs-lookup"><span data-stu-id="47f8f-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="47f8f-112">Beispiel 2: Deaktivieren einer Regel</span><span class="sxs-lookup"><span data-stu-id="47f8f-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="47f8f-113">Mit diesem Befehl wird eine Regel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47f8f-113">This command disables a rule.</span></span>
<span data-ttu-id="47f8f-114">Wenn die Regel nicht vorhanden ist, wird Sie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47f8f-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="47f8f-115">Wenn die Regel vorhanden ist, wird Sie nur deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47f8f-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="47f8f-116">Beispiel 3: Hinzufügen einer Regel mit Aktionen</span><span class="sxs-lookup"><span data-stu-id="47f8f-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="47f8f-117">Dieser Befehl erstellt eine Metrik-Warnungsregel für eine Website.</span><span class="sxs-lookup"><span data-stu-id="47f8f-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="47f8f-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="47f8f-118">PARAMETERS</span></span>

### <span data-ttu-id="47f8f-119">– Aktion</span><span class="sxs-lookup"><span data-stu-id="47f8f-119">-Action</span></span>
<span data-ttu-id="47f8f-120">Gibt eine durch trennzeichengetrennte Liste von Aktionen an.</span><span class="sxs-lookup"><span data-stu-id="47f8f-120">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="47f8f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47f8f-121">-DefaultProfile</span></span>
<span data-ttu-id="47f8f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="47f8f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f8f-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47f8f-123">-Description</span></span>
<span data-ttu-id="47f8f-124">Gibt eine Beschreibung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="47f8f-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="47f8f-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="47f8f-125">-DisableRule</span></span>
<span data-ttu-id="47f8f-126">Deaktiviert die Regel.</span><span class="sxs-lookup"><span data-stu-id="47f8f-126">Disables the rule.</span></span>
<span data-ttu-id="47f8f-127">Wenn Sie diesen Parameter nicht angeben, wird die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="47f8f-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="47f8f-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="47f8f-128">-Location</span></span>
<span data-ttu-id="47f8f-129">Gibt den Ort an, an dem die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="47f8f-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="47f8f-130">-Metricname</span><span class="sxs-lookup"><span data-stu-id="47f8f-130">-MetricName</span></span>
<span data-ttu-id="47f8f-131">Gibt den Namen der Metrik an, die die Regel überwacht.</span><span class="sxs-lookup"><span data-stu-id="47f8f-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="47f8f-132">Geben Sie diesen Parameter nur für metrische Regeln an.</span><span class="sxs-lookup"><span data-stu-id="47f8f-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="47f8f-133">-Name</span><span class="sxs-lookup"><span data-stu-id="47f8f-133">-Name</span></span>
<span data-ttu-id="47f8f-134">Gibt den Namen der Regel an.</span><span class="sxs-lookup"><span data-stu-id="47f8f-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="47f8f-135">-Operator</span><span class="sxs-lookup"><span data-stu-id="47f8f-135">-Operator</span></span>
<span data-ttu-id="47f8f-136">Gibt den relationalen Operator für die Bedingung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="47f8f-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="47f8f-137">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="47f8f-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="47f8f-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="47f8f-138">GreaterThan</span></span>
- <span data-ttu-id="47f8f-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="47f8f-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="47f8f-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="47f8f-140">LessThan</span></span>
- <span data-ttu-id="47f8f-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="47f8f-141">LessThanOrEqual</span></span>

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

### <span data-ttu-id="47f8f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47f8f-142">-ResourceGroupName</span></span>
<span data-ttu-id="47f8f-143">Gibt den Namen der Ressourcengruppe für die Regel an.</span><span class="sxs-lookup"><span data-stu-id="47f8f-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="47f8f-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="47f8f-144">-TargetResourceId</span></span>
<span data-ttu-id="47f8f-145">Gibt die ID der Ressource an, die von der Regel überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="47f8f-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="47f8f-146">Hinweis: Diese Eigenschaft kann für eine vorhandene Warnungsregel nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="47f8f-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="47f8f-147">-Threshold</span><span class="sxs-lookup"><span data-stu-id="47f8f-147">-Threshold</span></span>
<span data-ttu-id="47f8f-148">Gibt den Schwellenwert für die Regel an.</span><span class="sxs-lookup"><span data-stu-id="47f8f-148">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="47f8f-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="47f8f-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="47f8f-150">Gibt den Aggregations Operator an, der auf das Zeitfenster angewendet werden soll, wenn die Regel ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="47f8f-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="47f8f-151">-Windowsisieren</span><span class="sxs-lookup"><span data-stu-id="47f8f-151">-WindowSize</span></span>
<span data-ttu-id="47f8f-152">Gibt die Zeitfenster Größe für die Regel an, um die Daten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="47f8f-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="47f8f-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47f8f-153">-Confirm</span></span>
<span data-ttu-id="47f8f-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47f8f-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47f8f-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47f8f-155">-WhatIf</span></span>
<span data-ttu-id="47f8f-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47f8f-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47f8f-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47f8f-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47f8f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f8f-158">CommonParameters</span></span>
<span data-ttu-id="47f8f-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47f8f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47f8f-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47f8f-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f8f-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47f8f-161">INPUTS</span></span>

### <span data-ttu-id="47f8f-162">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="47f8f-162">System.TimeSpan</span></span>

### <span data-ttu-id="47f8f-163">Microsoft. Azure. Management. Monitor. Management. Models. ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="47f8f-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="47f8f-164">System. Double</span><span class="sxs-lookup"><span data-stu-id="47f8f-164">System.Double</span></span>

### <span data-ttu-id="47f8f-165">System. String</span><span class="sxs-lookup"><span data-stu-id="47f8f-165">System.String</span></span>

### <span data-ttu-id="47f8f-166">System. Nullable ' 1 [[Microsoft. Azure. Management. Monitor. Management. Models. TimeAggregationOperator, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="47f8f-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="47f8f-167">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="47f8f-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="47f8f-168">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Monitor. Management. Models. RuleAction, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="47f8f-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="47f8f-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47f8f-169">OUTPUTS</span></span>

### <span data-ttu-id="47f8f-170">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="47f8f-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="47f8f-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="47f8f-171">NOTES</span></span>

## <span data-ttu-id="47f8f-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47f8f-172">RELATED LINKS</span></span>

[<span data-ttu-id="47f8f-173">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="47f8f-173">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="47f8f-174">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="47f8f-174">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="47f8f-175">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="47f8f-175">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="47f8f-176">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="47f8f-176">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="47f8f-177">Neu – AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="47f8f-177">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="47f8f-178">Neu – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="47f8f-178">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="47f8f-179">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="47f8f-179">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


