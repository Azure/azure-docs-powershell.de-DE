---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: da395b66cb4d63593c097f214701365370e06b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482914"
---
# <span data-ttu-id="e3f0e-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e3f0e-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="e3f0e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f0e-103">Fügt eine Webtest-Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3f0e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3f0e-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3f0e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3f0e-105">DESCRIPTION</span></span>
<span data-ttu-id="e3f0e-106">Das **Add-AzureRmWebtestAlertRule-** Cmdlet fügt eine Warnungsregel des Typs Metric, Event oder Webtest hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="e3f0e-107">Die hinzugefügte Regel ist einer Ressourcengruppe zugeordnet und hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="e3f0e-108">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e3f0e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3f0e-109">EXAMPLES</span></span>

### <span data-ttu-id="e3f0e-110">Beispiel 1: Hinzufügen einer Webtest-Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="e3f0e-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="e3f0e-111">Dieser Befehl fügt eine Webtest-Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="e3f0e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3f0e-112">PARAMETERS</span></span>

### <span data-ttu-id="e3f0e-113">– Aktion</span><span class="sxs-lookup"><span data-stu-id="e3f0e-113">-Action</span></span>
<span data-ttu-id="e3f0e-114">Gibt eine durch trennzeichengetrennte Liste von Aktionen an.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="e3f0e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f0e-115">-DefaultProfile</span></span>
<span data-ttu-id="e3f0e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e3f0e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3f0e-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3f0e-117">-Description</span></span>
<span data-ttu-id="e3f0e-118">Gibt eine Beschreibung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="e3f0e-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="e3f0e-119">-DisableRule</span></span>
<span data-ttu-id="e3f0e-120">Deaktiviert die Regel.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-120">Disables the rule.</span></span>
<span data-ttu-id="e3f0e-121">Wenn Sie diesen Parameter nicht angeben, wird die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="e3f0e-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="e3f0e-122">-FailedLocationCount</span></span>
<span data-ttu-id="e3f0e-123">Gibt die Anzahl der fehlgeschlagenen Standorte für die Webtest Regeln an.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="e3f0e-124">Dies ist mit dem Schwellenwert in den anderen Regeltypen vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f0e-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="e3f0e-125">-Location</span></span>
<span data-ttu-id="e3f0e-126">Gibt den Ort an, an dem die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="e3f0e-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="e3f0e-127">-MetricName</span></span>
<span data-ttu-id="e3f0e-128">Gibt den Namen der Metrik an.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="e3f0e-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="e3f0e-129">-MetricNamespace</span></span>
<span data-ttu-id="e3f0e-130">Gibt den metrischen Namespace für Regel an.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="e3f0e-131">-Name</span><span class="sxs-lookup"><span data-stu-id="e3f0e-131">-Name</span></span>
<span data-ttu-id="e3f0e-132">Gibt den Namen der Regel an.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="e3f0e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3f0e-133">-ResourceGroupName</span></span>
<span data-ttu-id="e3f0e-134">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e3f0e-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="e3f0e-135">-TargetResourceUri</span></span>
<span data-ttu-id="e3f0e-136">Gibt die Ressourcen-ID des Webtests an.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="e3f0e-137">-Windowsisieren</span><span class="sxs-lookup"><span data-stu-id="e3f0e-137">-WindowSize</span></span>
<span data-ttu-id="e3f0e-138">Gibt die Zeitfenster Größe für die Regel an, um die Daten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="e3f0e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f0e-139">CommonParameters</span></span>
<span data-ttu-id="e3f0e-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f0e-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3f0e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f0e-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3f0e-142">INPUTS</span></span>

### <span data-ttu-id="e3f0e-143">Keine</span><span class="sxs-lookup"><span data-stu-id="e3f0e-143">None</span></span>
<span data-ttu-id="e3f0e-144">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e3f0e-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e3f0e-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3f0e-145">OUTPUTS</span></span>

### <span data-ttu-id="e3f0e-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e3f0e-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="e3f0e-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3f0e-147">NOTES</span></span>

## <span data-ttu-id="e3f0e-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3f0e-148">RELATED LINKS</span></span>

[<span data-ttu-id="e3f0e-149">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e3f0e-149">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e3f0e-150">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e3f0e-150">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="e3f0e-151">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="e3f0e-151">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="e3f0e-152">Neu – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e3f0e-152">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


