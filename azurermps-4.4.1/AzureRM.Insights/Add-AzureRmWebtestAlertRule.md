---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 52b3d39aef4c117fe8b26bb35f1bf50143e5fec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504950"
---
# <span data-ttu-id="e1e49-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1e49-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="e1e49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1e49-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e49-103">Fügt eine Webtest-Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="e1e49-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1e49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1e49-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1e49-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1e49-105">DESCRIPTION</span></span>
<span data-ttu-id="e1e49-106">Das **Add-AzureRmWebtestAlertRule-** Cmdlet fügt eine Warnungsregel des Typs Metric, Event oder Webtest hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="e1e49-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="e1e49-107">Die hinzugefügte Regel ist einer Ressourcengruppe zugeordnet und hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="e1e49-107">The added rule is associated to a resource group and has a name.</span></span>

## <span data-ttu-id="e1e49-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1e49-108">EXAMPLES</span></span>

### <span data-ttu-id="e1e49-109">Beispiel 1: Hinzufügen einer Webtest-Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="e1e49-109">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="e1e49-110">Dieser Befehl fügt eine Webtest-Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="e1e49-110">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="e1e49-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1e49-111">PARAMETERS</span></span>

### <span data-ttu-id="e1e49-112">-Aktionen</span><span class="sxs-lookup"><span data-stu-id="e1e49-112">-Actions</span></span>
<span data-ttu-id="e1e49-113">Gibt eine durch trennzeichengetrennte Liste von Aktionen an.</span><span class="sxs-lookup"><span data-stu-id="e1e49-113">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="e1e49-114">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1e49-114">-Description</span></span>
<span data-ttu-id="e1e49-115">Gibt eine Beschreibung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="e1e49-115">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="e1e49-116">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="e1e49-116">-DisableRule</span></span>
<span data-ttu-id="e1e49-117">Deaktiviert die Regel.</span><span class="sxs-lookup"><span data-stu-id="e1e49-117">Disables the rule.</span></span>
<span data-ttu-id="e1e49-118">Wenn Sie diesen Parameter nicht angeben, wird die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e1e49-118">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="e1e49-119">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="e1e49-119">-FailedLocationCount</span></span>
<span data-ttu-id="e1e49-120">Gibt die Anzahl der fehlgeschlagenen Standorte für die Webtest Regeln an.</span><span class="sxs-lookup"><span data-stu-id="e1e49-120">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="e1e49-121">Dies ist mit dem Schwellenwert in den anderen Regeltypen vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="e1e49-121">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="e1e49-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="e1e49-122">-Location</span></span>
<span data-ttu-id="e1e49-123">Gibt den Ort an, an dem die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e1e49-123">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="e1e49-124">-Metricname</span><span class="sxs-lookup"><span data-stu-id="e1e49-124">-MetricName</span></span>
<span data-ttu-id="e1e49-125">Gibt den Namen der Metrik an.</span><span class="sxs-lookup"><span data-stu-id="e1e49-125">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="e1e49-126">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="e1e49-126">-MetricNamespace</span></span>
<span data-ttu-id="e1e49-127">Gibt den metrischen Namespace für Regel an.</span><span class="sxs-lookup"><span data-stu-id="e1e49-127">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="e1e49-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e1e49-128">-Name</span></span>
<span data-ttu-id="e1e49-129">Gibt den Namen der Regel an.</span><span class="sxs-lookup"><span data-stu-id="e1e49-129">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="e1e49-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e1e49-130">-ResourceGroup</span></span>
<span data-ttu-id="e1e49-131">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e1e49-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e1e49-132">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="e1e49-132">-TargetResourceUri</span></span>
<span data-ttu-id="e1e49-133">Gibt die Ressourcen-ID des Webtests an.</span><span class="sxs-lookup"><span data-stu-id="e1e49-133">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="e1e49-134">-Windowsisieren</span><span class="sxs-lookup"><span data-stu-id="e1e49-134">-WindowSize</span></span>
<span data-ttu-id="e1e49-135">Gibt die Zeitfenster Größe für die Regel an, um die Daten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="e1e49-135">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="e1e49-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1e49-136">-DefaultProfile</span></span>
<span data-ttu-id="e1e49-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1e49-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1e49-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e49-138">CommonParameters</span></span>
<span data-ttu-id="e1e49-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1e49-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e49-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1e49-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e49-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1e49-141">INPUTS</span></span>

## <span data-ttu-id="e1e49-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1e49-142">OUTPUTS</span></span>

### <span data-ttu-id="e1e49-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e1e49-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="e1e49-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1e49-144">NOTES</span></span>

## <span data-ttu-id="e1e49-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1e49-145">RELATED LINKS</span></span>

[<span data-ttu-id="e1e49-146">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1e49-146">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="e1e49-147">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1e49-147">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="e1e49-148">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="e1e49-148">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="e1e49-149">Neu – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e1e49-149">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


