---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 9a215195ada1d804d2c139ed748eb844df46eed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665037"
---
# <span data-ttu-id="7e43e-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="7e43e-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="7e43e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e43e-102">SYNOPSIS</span></span>
<span data-ttu-id="7e43e-103">Fügt eine Metrik-basierte Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="7e43e-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e43e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e43e-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e43e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e43e-105">DESCRIPTION</span></span>
<span data-ttu-id="7e43e-106">Das **Add-AzureRmMetricAlertRule-** Cmdlet fügt eine Metrik-basierte Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="7e43e-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="7e43e-107">Die hinzugefügte Regel ist einer Ressourcengruppe zugeordnet und hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="7e43e-107">The added rule is associated with a resource group and has a name.</span></span>

## <span data-ttu-id="7e43e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e43e-108">EXAMPLES</span></span>

### <span data-ttu-id="7e43e-109">Beispiel 1: Hinzufügen einer Metrik-Warnungsregel zu einer Website</span><span class="sxs-lookup"><span data-stu-id="7e43e-109">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="7e43e-110">Dieser Befehl erstellt eine Metrik-Warnungsregel für eine Website.</span><span class="sxs-lookup"><span data-stu-id="7e43e-110">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="7e43e-111">Beispiel 2: Deaktivieren einer Regel</span><span class="sxs-lookup"><span data-stu-id="7e43e-111">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="7e43e-112">Mit diesem Befehl wird eine Regel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7e43e-112">This command disables a rule.</span></span>
<span data-ttu-id="7e43e-113">Wenn die Regel nicht vorhanden ist, wird Sie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7e43e-113">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="7e43e-114">Wenn die Regel vorhanden ist, wird Sie nur deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7e43e-114">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="7e43e-115">Beispiel 3: Hinzufügen einer Regel mit Aktionen</span><span class="sxs-lookup"><span data-stu-id="7e43e-115">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="7e43e-116">Dieser Befehl erstellt eine Metrik-Warnungsregel für eine Website.</span><span class="sxs-lookup"><span data-stu-id="7e43e-116">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="7e43e-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e43e-117">PARAMETERS</span></span>

### <span data-ttu-id="7e43e-118">-Aktionen</span><span class="sxs-lookup"><span data-stu-id="7e43e-118">-Actions</span></span>
<span data-ttu-id="7e43e-119">Gibt eine durch trennzeichengetrennte Liste von Aktionen an.</span><span class="sxs-lookup"><span data-stu-id="7e43e-119">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="7e43e-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e43e-120">-Description</span></span>
<span data-ttu-id="7e43e-121">Gibt eine Beschreibung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="7e43e-121">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="7e43e-122">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="7e43e-122">-DisableRule</span></span>
<span data-ttu-id="7e43e-123">Deaktiviert die Regel.</span><span class="sxs-lookup"><span data-stu-id="7e43e-123">Disables the rule.</span></span>
<span data-ttu-id="7e43e-124">Wenn Sie diesen Parameter nicht angeben, wird die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7e43e-124">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="7e43e-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="7e43e-125">-Location</span></span>
<span data-ttu-id="7e43e-126">Gibt den Ort an, an dem die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7e43e-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="7e43e-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="7e43e-127">-MetricName</span></span>
<span data-ttu-id="7e43e-128">Gibt den Namen der Metrik an, die die Regel überwacht.</span><span class="sxs-lookup"><span data-stu-id="7e43e-128">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="7e43e-129">Geben Sie diesen Parameter nur für metrische Regeln an.</span><span class="sxs-lookup"><span data-stu-id="7e43e-129">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="7e43e-130">-Name</span><span class="sxs-lookup"><span data-stu-id="7e43e-130">-Name</span></span>
<span data-ttu-id="7e43e-131">Gibt den Namen der Regel an.</span><span class="sxs-lookup"><span data-stu-id="7e43e-131">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="7e43e-132">-Operator</span><span class="sxs-lookup"><span data-stu-id="7e43e-132">-Operator</span></span>
<span data-ttu-id="7e43e-133">Gibt den relationalen Operator für die Bedingung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="7e43e-133">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="7e43e-134">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7e43e-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e43e-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="7e43e-135">GreaterThan</span></span>
- <span data-ttu-id="7e43e-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="7e43e-136">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="7e43e-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="7e43e-137">LessThan</span></span>
- <span data-ttu-id="7e43e-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="7e43e-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="7e43e-139">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7e43e-139">-ResourceGroup</span></span>
<span data-ttu-id="7e43e-140">Gibt den Namen der Ressourcengruppe für die Regel an.</span><span class="sxs-lookup"><span data-stu-id="7e43e-140">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="7e43e-141">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7e43e-141">-TargetResourceId</span></span>
<span data-ttu-id="7e43e-142">Gibt die ID der Ressource an, die von der Regel überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="7e43e-142">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="7e43e-143">Hinweis: Diese Eigenschaft kann für eine vorhandene Warnungsregel nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7e43e-143">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="7e43e-144">-Threshold</span><span class="sxs-lookup"><span data-stu-id="7e43e-144">-Threshold</span></span>
<span data-ttu-id="7e43e-145">Gibt den Schwellenwert für die Regel an.</span><span class="sxs-lookup"><span data-stu-id="7e43e-145">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="7e43e-146">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="7e43e-146">-TimeAggregationOperator</span></span>
<span data-ttu-id="7e43e-147">Gibt den Aggregations Operator an, der auf das Zeitfenster angewendet werden soll, wenn die Regel ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="7e43e-147">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="7e43e-148">-Windowsisieren</span><span class="sxs-lookup"><span data-stu-id="7e43e-148">-WindowSize</span></span>
<span data-ttu-id="7e43e-149">Gibt die Zeitfenster Größe für die Regel an, um die Daten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="7e43e-149">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="7e43e-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e43e-150">-DefaultProfile</span></span>
<span data-ttu-id="7e43e-151">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e43e-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e43e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e43e-152">CommonParameters</span></span>
<span data-ttu-id="7e43e-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e43e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e43e-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e43e-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e43e-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e43e-155">INPUTS</span></span>

## <span data-ttu-id="7e43e-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e43e-156">OUTPUTS</span></span>

### <span data-ttu-id="7e43e-157">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7e43e-157">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="7e43e-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e43e-158">NOTES</span></span>

## <span data-ttu-id="7e43e-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e43e-159">RELATED LINKS</span></span>

[<span data-ttu-id="7e43e-160">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="7e43e-160">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="7e43e-161">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="7e43e-161">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="7e43e-162">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="7e43e-162">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="7e43e-163">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="7e43e-163">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="7e43e-164">Neu – AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="7e43e-164">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="7e43e-165">Neu – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="7e43e-165">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="7e43e-166">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="7e43e-166">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


