---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93474469"
---
# <span data-ttu-id="7f5ad-101">AzureRM. Insights-Modul</span><span class="sxs-lookup"><span data-stu-id="7f5ad-101">AzureRM.Insights Module</span></span>
## <span data-ttu-id="7f5ad-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f5ad-102">Description</span></span>
<span data-ttu-id="7f5ad-103">In diesem Thema werden Hilfethemen zu den Azure Insights-Cmdlets angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-103">This topic displays help topics for the Azure Insights Cmdlets.</span></span>

## <span data-ttu-id="7f5ad-104">AzureRM. Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7f5ad-104">AzureRM.Insights Cmdlets</span></span>
### [<span data-ttu-id="7f5ad-105">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7f5ad-105">Add-AzureRmAutoscaleSetting</span></span>](Add-AzureRmAutoscaleSetting.md)
<span data-ttu-id="7f5ad-106">Erstellt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-106">Creates an Autoscale setting.</span></span>

### [<span data-ttu-id="7f5ad-107">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="7f5ad-107">Add-AzureRmLogAlertRule</span></span>](Add-AzureRmLogAlertRule.md)
<span data-ttu-id="7f5ad-108">Fügt eine Protokoll Warnungsregel hinzu oder ersetzt Sie.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-108">Adds or replaces a log alert rule.</span></span>

### [<span data-ttu-id="7f5ad-109">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="7f5ad-109">Add-AzureRmLogProfile</span></span>](Add-AzureRmLogProfile.md)
<span data-ttu-id="7f5ad-110">Erstellt ein neues Aktivitätsprotokoll Profil.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-110">Creates a new activity log profile.</span></span> <span data-ttu-id="7f5ad-111">Dieses Profil wird verwendet, um das Aktivitätsprotokoll entweder in einem Azure-Speicherkonto zu archivieren oder in einem Azure-Ereignis-Hub im gleichen Abonnement zu streamen.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-111">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="7f5ad-112">**Speicher** Konto – nur das Standardspeicher Konto (das Premium Speicherkonto wird nicht unterstützt) wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-112">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="7f5ad-113">Es kann entweder vom Typ Arm oder klassisch sein.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-113">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="7f5ad-114">Wenn Sie bei einem Speicherkonto angemeldet ist, werden die Kosten für die Speicherung des Aktivitätsprotokolls zu normalen Standardspeicher Gebühren berechnet.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-114">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="7f5ad-115">Pro Abonnement kann nur jeweils ein Protokoll Profil vorhanden sein. nur ein Speicherkonto pro Abonnement kann zum Exportieren des Aktivitätsprotokolls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-115">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="7f5ad-116">**Ereignis-Hub** -es kann nur jeweils ein Protokoll Profil pro Abonnement vorhanden sein. nur ein Ereignis-Hub pro Abonnement kann zum Exportieren des Aktivitätsprotokolls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-116">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="7f5ad-117">Wenn das Aktivitätsprotokoll zu einem Ereignis-Hub gestreamt wird, gelten die standardmäßigen Event Hub-Preise.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-117">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="7f5ad-118">Im Aktivitätsprotokoll können Ereignisse zu einer Region gehören oder "Global" sein.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-118">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="7f5ad-119">Global bedeutet im Wesentlichen, dass diese Ereignisse Regions Agnostiker sind und unabhängig von der Region sind, wobei die Mehrzahl der Ereignisse in diese Kategorie fällt.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-119">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="7f5ad-120">Wenn das Aktivitätsprotokoll Profil aus dem Portal gesetzt wird, wird implizit "Global" zusammen mit allen anderen in der Benutzeroberfläche ausgewählten Regionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-120">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="7f5ad-121">Wenn Sie das Cmdlet verwenden, muss der Speicherort als "Global" explizit außer in einer anderen Region erwähnt werden.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-121">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="7f5ad-122">**Hinweis** : Wenn Sie **"Global" nicht in den Speicherorten festgelegt haben, wird der Großteil des Aktivitätsprotokolls nicht exportiert.**</span><span class="sxs-lookup"><span data-stu-id="7f5ad-122">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

### [<span data-ttu-id="7f5ad-123">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="7f5ad-123">Add-AzureRmMetricAlertRule</span></span>](Add-AzureRmMetricAlertRule.md)
<span data-ttu-id="7f5ad-124">Fügt eine Metrik-basierte Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-124">Adds or updates a metric-based alert rule.</span></span>

### [<span data-ttu-id="7f5ad-125">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="7f5ad-125">Add-AzureRmWebtestAlertRule</span></span>](Add-AzureRmWebtestAlertRule.md)
<span data-ttu-id="7f5ad-126">Fügt eine Webtest-Warnungsregel hinzu oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-126">Adds or updates a webtest alert rule.</span></span>

### [<span data-ttu-id="7f5ad-127">Deaktivieren-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f5ad-127">Disable-AzureRmActivityLogAlert</span></span>](Disable-AzureRmActivityLogAlert.md)
<span data-ttu-id="7f5ad-128">Deaktiviert eine Aktivitätsprotokoll Benachrichtigung und legt ihre Tags fest.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-128">Disables an activity log alert and sets its tags.</span></span>

### [<span data-ttu-id="7f5ad-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f5ad-129">Enable-AzureRmActivityLogAlert</span></span>](Enable-AzureRmActivityLogAlert.md)
<span data-ttu-id="7f5ad-130">Aktiviert eine Aktivitätsprotokoll Benachrichtigung und legt ihre Tags fest.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-130">Enables an activity log alert and sets its Tags.</span></span>

### [<span data-ttu-id="7f5ad-131">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="7f5ad-131">Get-AzureRmActionGroup</span></span>](Get-AzureRmActionGroup.md)
<span data-ttu-id="7f5ad-132">Ruft die Aktionsgruppe (n) ab.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-132">Gets action group(s).</span></span>

### [<span data-ttu-id="7f5ad-133">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f5ad-133">Get-AzureRmActivityLogAlert</span></span>](Get-AzureRmActivityLogAlert.md)
<span data-ttu-id="7f5ad-134">Ruft eine oder mehrere Aktivitätsprotokoll-Warnungs Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-134">Gets one or more activity log alert resources.</span></span>

### [<span data-ttu-id="7f5ad-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="7f5ad-135">Get-AzureRmAlertHistory</span></span>](Get-AzureRmAlertHistory.md)
<span data-ttu-id="7f5ad-136">Ruft den Verlauf von Benachrichtigungen ab.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-136">Gets the history of alerts.</span></span>

### [<span data-ttu-id="7f5ad-137">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="7f5ad-137">Get-AzureRmAlertRule</span></span>](Get-AzureRmAlertRule.md)
<span data-ttu-id="7f5ad-138">Ruft Warnungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-138">Gets alert rules.</span></span>

### [<span data-ttu-id="7f5ad-139">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="7f5ad-139">Get-AzureRmAutoscaleHistory</span></span>](Get-AzureRmAutoscaleHistory.md)
<span data-ttu-id="7f5ad-140">Ruft den AutoScale-Verlauf ab.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-140">Gets the Autoscale history.</span></span>

### [<span data-ttu-id="7f5ad-141">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7f5ad-141">Get-AzureRmAutoscaleSetting</span></span>](Get-AzureRmAutoscaleSetting.md)
<span data-ttu-id="7f5ad-142">Ruft AutoScale-Einstellungen ab.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-142">Gets Autoscale settings.</span></span>

### [<span data-ttu-id="7f5ad-143">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="7f5ad-143">Get-AzureRmDiagnosticSetting</span></span>](Get-AzureRmDiagnosticSetting.md)
<span data-ttu-id="7f5ad-144">Ruft die protokollierten Kategorien und Zeit Körner ab.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-144">Gets the logged categories and time grains.</span></span>

### [<span data-ttu-id="7f5ad-145">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="7f5ad-145">Get-AzureRmLog</span></span>](Get-AzureRmLog.md)
<span data-ttu-id="7f5ad-146">Ruft ein Protokoll von Ereignissen ab.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-146">Gets a log of events.</span></span>

### [<span data-ttu-id="7f5ad-147">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="7f5ad-147">Get-AzureRmLogProfile</span></span>](Get-AzureRmLogProfile.md)
<span data-ttu-id="7f5ad-148">Ruft ein Protokoll Profil ab.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-148">Gets a log profile.</span></span>

### [<span data-ttu-id="7f5ad-149">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="7f5ad-149">Get-AzureRmMetric</span></span>](Get-AzureRmMetric.md)
<span data-ttu-id="7f5ad-150">Ruft die metrischen Werte einer Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-150">Gets the metric values of a resource.</span></span>

### [<span data-ttu-id="7f5ad-151">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="7f5ad-151">Get-AzureRmMetricDefinition</span></span>](Get-AzureRmMetricDefinition.md)
<span data-ttu-id="7f5ad-152">Ruft metrische Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-152">Gets metric definitions.</span></span>

### [<span data-ttu-id="7f5ad-153">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="7f5ad-153">Get-AzureRmUsage</span></span>](Get-AzureRmUsage.md)
<span data-ttu-id="7f5ad-154">Ruft die Verwendungs Metriken für eine Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-154">Gets the usage metrics for a resource.</span></span>

### [<span data-ttu-id="7f5ad-155">Neu – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="7f5ad-155">New-AzureRmActionGroup</span></span>](New-AzureRmActionGroup.md)
<span data-ttu-id="7f5ad-156">Erstellt ein Aktions Gruppenverweis-Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-156">Creates an ActionGroup reference object in memory.</span></span>

### [<span data-ttu-id="7f5ad-157">Neu – AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="7f5ad-157">New-AzureRmActionGroupReceiver</span></span>](New-AzureRmActionGroupReceiver.md)
<span data-ttu-id="7f5ad-158">Erstellt einen neuen Aktionsgruppen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-158">Creates an new action group receiver.</span></span>

### [<span data-ttu-id="7f5ad-159">Neu – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="7f5ad-159">New-AzureRmActivityLogAlertCondition</span></span>](New-AzureRmActivityLogAlertCondition.md)
<span data-ttu-id="7f5ad-160">Erstellt ein neues Aktivitätsprotokoll-Warnungs Konditions Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-160">Creates an new activity log alert condition object in memory.</span></span>

### [<span data-ttu-id="7f5ad-161">Neu – AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="7f5ad-161">New-AzureRmAlertRuleEmail</span></span>](New-AzureRmAlertRuleEmail.md)
<span data-ttu-id="7f5ad-162">Erstellt eine e-Mail-Aktion für eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-162">Creates an email action for an alert rule.</span></span>

### [<span data-ttu-id="7f5ad-163">Neu – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="7f5ad-163">New-AzureRmAlertRuleWebhook</span></span>](New-AzureRmAlertRuleWebhook.md)
<span data-ttu-id="7f5ad-164">Erstellt eine Benachrichtigungsregel webhook.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-164">Creates an alert rule webhook.</span></span>

### [<span data-ttu-id="7f5ad-165">Neu – AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="7f5ad-165">New-AzureRmAutoscaleNotification</span></span>](New-AzureRmAutoscaleNotification.md)
<span data-ttu-id="7f5ad-166">Erstellt eine AutoScale-e-Mail-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-166">Creates an Autoscale email notification.</span></span>

### [<span data-ttu-id="7f5ad-167">Neu – AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="7f5ad-167">New-AzureRmAutoscaleProfile</span></span>](New-AzureRmAutoscaleProfile.md)
<span data-ttu-id="7f5ad-168">Erstellt ein AutoScale-Profil.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-168">Creates an Autoscale profile.</span></span>

### [<span data-ttu-id="7f5ad-169">Neu – AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="7f5ad-169">New-AzureRmAutoscaleRule</span></span>](New-AzureRmAutoscaleRule.md)
<span data-ttu-id="7f5ad-170">Erstellt eine AutoScale-Regel.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-170">Creates an Autoscale rule.</span></span>

### [<span data-ttu-id="7f5ad-171">Neu – AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="7f5ad-171">New-AzureRmAutoscaleWebhook</span></span>](New-AzureRmAutoscaleWebhook.md)
<span data-ttu-id="7f5ad-172">Erstellt einen AutoScale-webhook.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-172">Creates an Autoscale webhook.</span></span>

### [<span data-ttu-id="7f5ad-173">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="7f5ad-173">Remove-AzureRmActionGroup</span></span>](Remove-AzureRmActionGroup.md)
<span data-ttu-id="7f5ad-174">Entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-174">Removes an action group.</span></span>

### [<span data-ttu-id="7f5ad-175">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f5ad-175">Remove-AzureRmActivityLogAlert</span></span>](Remove-AzureRmActivityLogAlert.md)
<span data-ttu-id="7f5ad-176">Entfernt eine Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-176">Removes an activity log alert.</span></span>

### [<span data-ttu-id="7f5ad-177">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="7f5ad-177">Remove-AzureRmAlertRule</span></span>](Remove-AzureRmAlertRule.md)
<span data-ttu-id="7f5ad-178">Entfernt eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-178">Removes an alert rule.</span></span>

### [<span data-ttu-id="7f5ad-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7f5ad-179">Remove-AzureRmAutoscaleSetting</span></span>](Remove-AzureRmAutoscaleSetting.md)
<span data-ttu-id="7f5ad-180">Entfernt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-180">Removes an Autoscale setting.</span></span>

### [<span data-ttu-id="7f5ad-181">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="7f5ad-181">Remove-AzureRmLogProfile</span></span>](Remove-AzureRmLogProfile.md)
<span data-ttu-id="7f5ad-182">Entfernt ein Protokoll Profil.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-182">Removes a log profile.</span></span>

### [<span data-ttu-id="7f5ad-183">Satz-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="7f5ad-183">Set-AzureRmActionGroup</span></span>](Set-AzureRmActionGroup.md)
<span data-ttu-id="7f5ad-184">Erstellt eine neue oder aktualisiert eine vorhandene Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-184">Creates a new or updates an existing action group.</span></span>

### [<span data-ttu-id="7f5ad-185">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f5ad-185">Set-AzureRmActivityLogAlert</span></span>](Set-AzureRmActivityLogAlert.md)
<span data-ttu-id="7f5ad-186">Erstellt ein neues oder legt eine vorhandene Aktivitätsprotokoll Benachrichtigung fest.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-186">Creates a new or sets an existing activity log alert.</span></span>

### [<span data-ttu-id="7f5ad-187">Satz-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="7f5ad-187">Set-AzureRmDiagnosticSetting</span></span>](Set-AzureRmDiagnosticSetting.md)
<span data-ttu-id="7f5ad-188">Legt die Einstellungen für Protokolle und Metriken für die Ressource fest.</span><span class="sxs-lookup"><span data-stu-id="7f5ad-188">Sets the logs and metrics settings for the resource.</span></span>

