---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 8f66117d4ae2909617a6215c1c154ba22d469b21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932744"
---
# <span data-ttu-id="9e0a7-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="9e0a7-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="9e0a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e0a7-102">SYNOPSIS</span></span>
<span data-ttu-id="9e0a7-103">Fügt eine Webtestbenachrichtigungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="9e0a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e0a7-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e0a7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e0a7-105">DESCRIPTION</span></span>
<span data-ttu-id="9e0a7-106">Das **Add-AzWebtestAlertRule-Cmdlet** fügt eine Warnungsregel vom Metrik-, Ereignis- oder Webtesttyp hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="9e0a7-107">Die hinzugefügte Regel ist einer Ressourcengruppe zugeordnet und hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="9e0a7-108">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h. es kann eine Bestätigung vom Benutzer anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="9e0a7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e0a7-109">EXAMPLES</span></span>

### <span data-ttu-id="9e0a7-110">Beispiel 1: Hinzufügen einer Webtestbenachrichtigungsregel</span><span class="sxs-lookup"><span data-stu-id="9e0a7-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="9e0a7-111">Mit diesem Befehl wird eine Webtestbenachrichtigungsregel addiert oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="9e0a7-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9e0a7-112">PARAMETERS</span></span>

### <span data-ttu-id="9e0a7-113">-Aktion</span><span class="sxs-lookup"><span data-stu-id="9e0a7-113">-Action</span></span>
<span data-ttu-id="9e0a7-114">Gibt eine durch Kommas getrennte Liste von Aktionen an.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="9e0a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e0a7-115">-DefaultProfile</span></span>
<span data-ttu-id="9e0a7-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9e0a7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e0a7-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e0a7-117">-Description</span></span>
<span data-ttu-id="9e0a7-118">Gibt eine Beschreibung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="9e0a7-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="9e0a7-119">-DisableRule</span></span>
<span data-ttu-id="9e0a7-120">Deaktiviert die Regel.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-120">Disables the rule.</span></span>
<span data-ttu-id="9e0a7-121">Wenn Sie diesen Parameter nicht angeben, ist die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="9e0a7-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="9e0a7-122">-FailedLocationCount</span></span>
<span data-ttu-id="9e0a7-123">Gibt die Anzahl der fehlgeschlagenen Speicherorte für die Webtestregeln an.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="9e0a7-124">Dies ist mit dem Schwellenwert in den anderen Arten von Regeln vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="9e0a7-125">-Location</span><span class="sxs-lookup"><span data-stu-id="9e0a7-125">-Location</span></span>
<span data-ttu-id="9e0a7-126">Gibt den Speicherort an, an dem die Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="9e0a7-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="9e0a7-127">-MetricName</span></span>
<span data-ttu-id="9e0a7-128">Gibt den Namen der Metrik an.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="9e0a7-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="9e0a7-129">-MetricNamespace</span></span>
<span data-ttu-id="9e0a7-130">Gibt den Metriknamespace für regel an.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="9e0a7-131">-Name</span><span class="sxs-lookup"><span data-stu-id="9e0a7-131">-Name</span></span>
<span data-ttu-id="9e0a7-132">Gibt den Namen der Regel an.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="9e0a7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e0a7-133">-ResourceGroupName</span></span>
<span data-ttu-id="9e0a7-134">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9e0a7-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="9e0a7-135">-TargetResourceUri</span></span>
<span data-ttu-id="9e0a7-136">Gibt die Ressourcen-ID des Webtests an.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="9e0a7-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="9e0a7-137">-WindowSize</span></span>
<span data-ttu-id="9e0a7-138">Gibt die Zeitfenstergröße für die Regel an, um ihre Daten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="9e0a7-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e0a7-139">-Confirm</span></span>
<span data-ttu-id="9e0a7-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e0a7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e0a7-141">-WhatIf</span></span>
<span data-ttu-id="9e0a7-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e0a7-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e0a7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e0a7-144">CommonParameters</span></span>
<span data-ttu-id="9e0a7-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e0a7-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e0a7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e0a7-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e0a7-147">INPUTS</span></span>

### <span data-ttu-id="9e0a7-148">System.String</span><span class="sxs-lookup"><span data-stu-id="9e0a7-148">System.String</span></span>

### <span data-ttu-id="9e0a7-149">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="9e0a7-149">System.TimeSpan</span></span>

### <span data-ttu-id="9e0a7-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9e0a7-150">System.Int32</span></span>

### <span data-ttu-id="9e0a7-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9e0a7-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9e0a7-152">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9e0a7-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9e0a7-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e0a7-153">OUTPUTS</span></span>

### <span data-ttu-id="9e0a7-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9e0a7-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="9e0a7-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9e0a7-155">NOTES</span></span>

## <span data-ttu-id="9e0a7-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9e0a7-156">RELATED LINKS</span></span>

[<span data-ttu-id="9e0a7-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9e0a7-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="9e0a7-158">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="9e0a7-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="9e0a7-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="9e0a7-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="9e0a7-160">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="9e0a7-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


