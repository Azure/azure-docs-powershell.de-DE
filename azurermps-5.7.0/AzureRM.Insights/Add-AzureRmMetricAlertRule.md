---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 097f3562ca326275c050054fd07d11d349cf98d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482918"
---
# <span data-ttu-id="f1bab-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="f1bab-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="f1bab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1bab-102">SYNOPSIS</span></span>
<span data-ttu-id="f1bab-103">Fügt eine Metrik-basierte Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="f1bab-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1bab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1bab-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1bab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1bab-105">DESCRIPTION</span></span>
<span data-ttu-id="f1bab-106">Das **Add-AzureRmMetricAlertRule-** Cmdlet fügt eine Metrik-basierte Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="f1bab-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="f1bab-107">Die hinzugefügte Regel ist einer Ressourcengruppe zugeordnet und hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="f1bab-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="f1bab-108">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f1bab-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f1bab-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1bab-109">EXAMPLES</span></span>

### <span data-ttu-id="f1bab-110">Beispiel 1: Hinzufügen einer Metrik-Warnungsregel zu einer Website</span><span class="sxs-lookup"><span data-stu-id="f1bab-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="f1bab-111">Dieser Befehl erstellt eine Metrik-Warnungsregel für eine Website.</span><span class="sxs-lookup"><span data-stu-id="f1bab-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="f1bab-112">Beispiel 2: Deaktivieren einer Regel</span><span class="sxs-lookup"><span data-stu-id="f1bab-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="f1bab-113">Mit diesem Befehl wird eine Regel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1bab-113">This command disables a rule.</span></span>
<span data-ttu-id="f1bab-114">Wenn die Regel nicht vorhanden ist, wird Sie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1bab-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="f1bab-115">Wenn die Regel vorhanden ist, wird Sie nur deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1bab-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="f1bab-116">Beispiel 3: Hinzufügen einer Regel mit Aktionen</span><span class="sxs-lookup"><span data-stu-id="f1bab-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="f1bab-117">Dieser Befehl erstellt eine Metrik-Warnungsregel für eine Website.</span><span class="sxs-lookup"><span data-stu-id="f1bab-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="f1bab-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1bab-118">PARAMETERS</span></span>

### <span data-ttu-id="f1bab-119">– Aktion</span><span class="sxs-lookup"><span data-stu-id="f1bab-119">-Action</span></span>
<span data-ttu-id="f1bab-120">Gibt eine durch trennzeichengetrennte Liste von Aktionen an.</span><span class="sxs-lookup"><span data-stu-id="f1bab-120">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1bab-121">-DefaultProfile</span></span>
<span data-ttu-id="f1bab-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f1bab-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1bab-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1bab-123">-Description</span></span>
<span data-ttu-id="f1bab-124">Gibt eine Beschreibung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="f1bab-124">Specifies a description of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bab-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="f1bab-125">-DisableRule</span></span>
<span data-ttu-id="f1bab-126">Deaktiviert die Regel.</span><span class="sxs-lookup"><span data-stu-id="f1bab-126">Disables the rule.</span></span>
<span data-ttu-id="f1bab-127">Wenn Sie diesen Parameter nicht angeben, wird die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1bab-127">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bab-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="f1bab-128">-Location</span></span>
<span data-ttu-id="f1bab-129">Gibt den Ort an, an dem die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f1bab-129">Specifies the location where the rule is defined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bab-130">-Metricname</span><span class="sxs-lookup"><span data-stu-id="f1bab-130">-MetricName</span></span>
<span data-ttu-id="f1bab-131">Gibt den Namen der Metrik an, die die Regel überwacht.</span><span class="sxs-lookup"><span data-stu-id="f1bab-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="f1bab-132">Geben Sie diesen Parameter nur für metrische Regeln an.</span><span class="sxs-lookup"><span data-stu-id="f1bab-132">Specify this parameter only for metric-based rules.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bab-133">-Name</span><span class="sxs-lookup"><span data-stu-id="f1bab-133">-Name</span></span>
<span data-ttu-id="f1bab-134">Gibt den Namen der Regel an.</span><span class="sxs-lookup"><span data-stu-id="f1bab-134">Specifies the name of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bab-135">-Operator</span><span class="sxs-lookup"><span data-stu-id="f1bab-135">-Operator</span></span>
<span data-ttu-id="f1bab-136">Gibt den relationalen Operator für die Bedingung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="f1bab-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="f1bab-137">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f1bab-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1bab-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="f1bab-138">GreaterThan</span></span>
- <span data-ttu-id="f1bab-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="f1bab-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="f1bab-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="f1bab-140">LessThan</span></span>
- <span data-ttu-id="f1bab-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="f1bab-141">LessThanOrEqual</span></span>

```yaml
Type: ConditionOperator
Parameter Sets: (All)
Aliases: 
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bab-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1bab-142">-ResourceGroupName</span></span>
<span data-ttu-id="f1bab-143">Gibt den Namen der Ressourcengruppe für die Regel an.</span><span class="sxs-lookup"><span data-stu-id="f1bab-143">Specifies the name of the resource group for the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bab-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f1bab-144">-TargetResourceId</span></span>
<span data-ttu-id="f1bab-145">Gibt die ID der Ressource an, die von der Regel überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="f1bab-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="f1bab-146">Hinweis: Diese Eigenschaft kann für eine vorhandene Warnungsregel nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f1bab-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bab-147">-Threshold</span><span class="sxs-lookup"><span data-stu-id="f1bab-147">-Threshold</span></span>
<span data-ttu-id="f1bab-148">Gibt den Schwellenwert für die Regel an.</span><span class="sxs-lookup"><span data-stu-id="f1bab-148">Specifies the threshold of the rule.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bab-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="f1bab-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="f1bab-150">Gibt den Aggregations Operator an, der auf das Zeitfenster angewendet werden soll, wenn die Regel ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="f1bab-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: TimeAggregationOperator
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bab-151">-Windowsisieren</span><span class="sxs-lookup"><span data-stu-id="f1bab-151">-WindowSize</span></span>
<span data-ttu-id="f1bab-152">Gibt die Zeitfenster Größe für die Regel an, um die Daten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f1bab-152">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bab-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1bab-153">CommonParameters</span></span>
<span data-ttu-id="f1bab-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1bab-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1bab-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1bab-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1bab-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1bab-156">INPUTS</span></span>

### <span data-ttu-id="f1bab-157">Keine</span><span class="sxs-lookup"><span data-stu-id="f1bab-157">None</span></span>
<span data-ttu-id="f1bab-158">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f1bab-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1bab-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1bab-159">OUTPUTS</span></span>

### <span data-ttu-id="f1bab-160">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f1bab-160">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="f1bab-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1bab-161">NOTES</span></span>

## <span data-ttu-id="f1bab-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1bab-162">RELATED LINKS</span></span>

[<span data-ttu-id="f1bab-163">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f1bab-163">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f1bab-164">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="f1bab-164">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="f1bab-165">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="f1bab-165">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="f1bab-166">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="f1bab-166">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="f1bab-167">Neu – AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="f1bab-167">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="f1bab-168">Neu – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="f1bab-168">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="f1bab-169">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="f1bab-169">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


