---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 08d84c1f5e71c18a47e48bda1e39ce37ed0cb026
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662932"
---
# <span data-ttu-id="df1c2-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="df1c2-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="df1c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df1c2-102">SYNOPSIS</span></span>
<span data-ttu-id="df1c2-103">Fügt eine Webtest-Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="df1c2-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df1c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df1c2-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df1c2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df1c2-105">DESCRIPTION</span></span>
<span data-ttu-id="df1c2-106">Das **Add-AzureRmWebtestAlertRule-** Cmdlet fügt eine Warnungsregel des Typs Metric, Event oder Webtest hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="df1c2-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="df1c2-107">Die hinzugefügte Regel ist einer Ressourcengruppe zugeordnet und hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="df1c2-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="df1c2-108">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="df1c2-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="df1c2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df1c2-109">EXAMPLES</span></span>

### <span data-ttu-id="df1c2-110">Beispiel 1: Hinzufügen einer Webtest-Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="df1c2-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="df1c2-111">Dieser Befehl fügt eine Webtest-Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="df1c2-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="df1c2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="df1c2-112">PARAMETERS</span></span>

### <span data-ttu-id="df1c2-113">– Aktion</span><span class="sxs-lookup"><span data-stu-id="df1c2-113">-Action</span></span>
<span data-ttu-id="df1c2-114">Gibt eine durch trennzeichengetrennte Liste von Aktionen an.</span><span class="sxs-lookup"><span data-stu-id="df1c2-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="df1c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1c2-115">-DefaultProfile</span></span>
<span data-ttu-id="df1c2-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="df1c2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df1c2-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df1c2-117">-Description</span></span>
<span data-ttu-id="df1c2-118">Gibt eine Beschreibung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="df1c2-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="df1c2-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="df1c2-119">-DisableRule</span></span>
<span data-ttu-id="df1c2-120">Deaktiviert die Regel.</span><span class="sxs-lookup"><span data-stu-id="df1c2-120">Disables the rule.</span></span>
<span data-ttu-id="df1c2-121">Wenn Sie diesen Parameter nicht angeben, wird die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="df1c2-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="df1c2-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="df1c2-122">-FailedLocationCount</span></span>
<span data-ttu-id="df1c2-123">Gibt die Anzahl der fehlgeschlagenen Standorte für die Webtest Regeln an.</span><span class="sxs-lookup"><span data-stu-id="df1c2-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="df1c2-124">Dies ist mit dem Schwellenwert in den anderen Regeltypen vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="df1c2-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df1c2-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="df1c2-125">-Location</span></span>
<span data-ttu-id="df1c2-126">Gibt den Ort an, an dem die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="df1c2-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="df1c2-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="df1c2-127">-MetricName</span></span>
<span data-ttu-id="df1c2-128">Gibt den Namen der Metrik an.</span><span class="sxs-lookup"><span data-stu-id="df1c2-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="df1c2-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="df1c2-129">-MetricNamespace</span></span>
<span data-ttu-id="df1c2-130">Gibt den metrischen Namespace für Regel an.</span><span class="sxs-lookup"><span data-stu-id="df1c2-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="df1c2-131">-Name</span><span class="sxs-lookup"><span data-stu-id="df1c2-131">-Name</span></span>
<span data-ttu-id="df1c2-132">Gibt den Namen der Regel an.</span><span class="sxs-lookup"><span data-stu-id="df1c2-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="df1c2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df1c2-133">-ResourceGroupName</span></span>
<span data-ttu-id="df1c2-134">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="df1c2-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="df1c2-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="df1c2-135">-TargetResourceUri</span></span>
<span data-ttu-id="df1c2-136">Gibt die Ressourcen-ID des Webtests an.</span><span class="sxs-lookup"><span data-stu-id="df1c2-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="df1c2-137">-Windowsisieren</span><span class="sxs-lookup"><span data-stu-id="df1c2-137">-WindowSize</span></span>
<span data-ttu-id="df1c2-138">Gibt die Zeitfenster Größe für die Regel an, um die Daten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="df1c2-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="df1c2-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="df1c2-139">-Confirm</span></span>
<span data-ttu-id="df1c2-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df1c2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df1c2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df1c2-141">-WhatIf</span></span>
<span data-ttu-id="df1c2-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df1c2-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df1c2-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df1c2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df1c2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1c2-144">CommonParameters</span></span>
<span data-ttu-id="df1c2-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df1c2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1c2-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df1c2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1c2-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df1c2-147">INPUTS</span></span>

### <span data-ttu-id="df1c2-148">System. String</span><span class="sxs-lookup"><span data-stu-id="df1c2-148">System.String</span></span>

### <span data-ttu-id="df1c2-149">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="df1c2-149">System.TimeSpan</span></span>

### <span data-ttu-id="df1c2-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="df1c2-150">System.Int32</span></span>

### <span data-ttu-id="df1c2-151">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="df1c2-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="df1c2-152">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Monitor. Management. Models. RuleAction, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="df1c2-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="df1c2-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df1c2-153">OUTPUTS</span></span>

### <span data-ttu-id="df1c2-154">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="df1c2-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="df1c2-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="df1c2-155">NOTES</span></span>

## <span data-ttu-id="df1c2-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df1c2-156">RELATED LINKS</span></span>

[<span data-ttu-id="df1c2-157">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="df1c2-157">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="df1c2-158">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="df1c2-158">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="df1c2-159">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="df1c2-159">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="df1c2-160">Neu – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="df1c2-160">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


