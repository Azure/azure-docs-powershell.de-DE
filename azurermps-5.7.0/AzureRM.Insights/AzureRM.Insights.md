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
# AzureRM. Insights-Modul
## Beschreibung
In diesem Thema werden Hilfethemen zu den Azure Insights-Cmdlets angezeigt.

## AzureRM. Insights-Cmdlets
### [Add-AzureRmAutoscaleSetting](Add-AzureRmAutoscaleSetting.md)
Erstellt eine AutoScale-Einstellung.

### [Add-AzureRmLogAlertRule](Add-AzureRmLogAlertRule.md)
Fügt eine Protokoll Warnungsregel hinzu oder ersetzt Sie.

### [Add-AzureRmLogProfile](Add-AzureRmLogProfile.md)
Erstellt ein neues Aktivitätsprotokoll Profil. Dieses Profil wird verwendet, um das Aktivitätsprotokoll entweder in einem Azure-Speicherkonto zu archivieren oder in einem Azure-Ereignis-Hub im gleichen Abonnement zu streamen. 

- **Speicher** Konto – nur das Standardspeicher Konto (das Premium Speicherkonto wird nicht unterstützt) wird unterstützt. Es kann entweder vom Typ Arm oder klassisch sein. Wenn Sie bei einem Speicherkonto angemeldet ist, werden die Kosten für die Speicherung des Aktivitätsprotokolls zu normalen Standardspeicher Gebühren berechnet. Pro Abonnement kann nur jeweils ein Protokoll Profil vorhanden sein. nur ein Speicherkonto pro Abonnement kann zum Exportieren des Aktivitätsprotokolls verwendet werden. 

- **Ereignis-Hub** -es kann nur jeweils ein Protokoll Profil pro Abonnement vorhanden sein. nur ein Ereignis-Hub pro Abonnement kann zum Exportieren des Aktivitätsprotokolls verwendet werden. Wenn das Aktivitätsprotokoll zu einem Ereignis-Hub gestreamt wird, gelten die standardmäßigen Event Hub-Preise. 

Im Aktivitätsprotokoll können Ereignisse zu einer Region gehören oder "Global" sein. Global bedeutet im Wesentlichen, dass diese Ereignisse Regions Agnostiker sind und unabhängig von der Region sind, wobei die Mehrzahl der Ereignisse in diese Kategorie fällt. Wenn das Aktivitätsprotokoll Profil aus dem Portal gesetzt wird, wird implizit "Global" zusammen mit allen anderen in der Benutzeroberfläche ausgewählten Regionen hinzugefügt. Wenn Sie das Cmdlet verwenden, muss der Speicherort als "Global" explizit außer in einer anderen Region erwähnt werden. 

**Hinweis** : Wenn Sie **"Global" nicht in den Speicherorten festgelegt haben, wird der Großteil des Aktivitätsprotokolls nicht exportiert.** 

### [Add-AzureRmMetricAlertRule](Add-AzureRmMetricAlertRule.md)
Fügt eine Metrik-basierte Warnungsregel hinzu oder aktualisiert sie.

### [Add-AzureRmWebtestAlertRule](Add-AzureRmWebtestAlertRule.md)
Fügt eine Webtest-Warnungsregel hinzu oder aktualisiert sie.

### [Deaktivieren-AzureRmActivityLogAlert](Disable-AzureRmActivityLogAlert.md)
Deaktiviert eine Aktivitätsprotokoll Benachrichtigung und legt ihre Tags fest.

### [Enable-AzureRmActivityLogAlert](Enable-AzureRmActivityLogAlert.md)
Aktiviert eine Aktivitätsprotokoll Benachrichtigung und legt ihre Tags fest.

### [Get-AzureRmActionGroup](Get-AzureRmActionGroup.md)
Ruft die Aktionsgruppe (n) ab.

### [Get-AzureRmActivityLogAlert](Get-AzureRmActivityLogAlert.md)
Ruft eine oder mehrere Aktivitätsprotokoll-Warnungs Ressourcen ab.

### [Get-AzureRmAlertHistory](Get-AzureRmAlertHistory.md)
Ruft den Verlauf von Benachrichtigungen ab.

### [Get-AzureRmAlertRule](Get-AzureRmAlertRule.md)
Ruft Warnungsregeln ab.

### [Get-AzureRmAutoscaleHistory](Get-AzureRmAutoscaleHistory.md)
Ruft den AutoScale-Verlauf ab.

### [Get-AzureRmAutoscaleSetting](Get-AzureRmAutoscaleSetting.md)
Ruft AutoScale-Einstellungen ab.

### [Get-AzureRmDiagnosticSetting](Get-AzureRmDiagnosticSetting.md)
Ruft die protokollierten Kategorien und Zeit Körner ab.

### [Get-AzureRmLog](Get-AzureRmLog.md)
Ruft ein Protokoll von Ereignissen ab.

### [Get-AzureRmLogProfile](Get-AzureRmLogProfile.md)
Ruft ein Protokoll Profil ab.

### [Get-AzureRmMetric](Get-AzureRmMetric.md)
Ruft die metrischen Werte einer Ressource ab.

### [Get-AzureRmMetricDefinition](Get-AzureRmMetricDefinition.md)
Ruft metrische Definitionen ab.

### [Get-AzureRmUsage](Get-AzureRmUsage.md)
Ruft die Verwendungs Metriken für eine Ressource ab.

### [Neu – AzureRmActionGroup](New-AzureRmActionGroup.md)
Erstellt ein Aktions Gruppenverweis-Objekt im Arbeitsspeicher.

### [Neu – AzureRmActionGroupReceiver](New-AzureRmActionGroupReceiver.md)
Erstellt einen neuen Aktionsgruppen Empfänger.

### [Neu – AzureRmActivityLogAlertCondition](New-AzureRmActivityLogAlertCondition.md)
Erstellt ein neues Aktivitätsprotokoll-Warnungs Konditions Objekt im Arbeitsspeicher.

### [Neu – AzureRmAlertRuleEmail](New-AzureRmAlertRuleEmail.md)
Erstellt eine e-Mail-Aktion für eine Warnungsregel.

### [Neu – AzureRmAlertRuleWebhook](New-AzureRmAlertRuleWebhook.md)
Erstellt eine Benachrichtigungsregel webhook.

### [Neu – AzureRmAutoscaleNotification](New-AzureRmAutoscaleNotification.md)
Erstellt eine AutoScale-e-Mail-Benachrichtigung.

### [Neu – AzureRmAutoscaleProfile](New-AzureRmAutoscaleProfile.md)
Erstellt ein AutoScale-Profil.

### [Neu – AzureRmAutoscaleRule](New-AzureRmAutoscaleRule.md)
Erstellt eine AutoScale-Regel.

### [Neu – AzureRmAutoscaleWebhook](New-AzureRmAutoscaleWebhook.md)
Erstellt einen AutoScale-webhook.

### [Remove-AzureRmActionGroup](Remove-AzureRmActionGroup.md)
Entfernt eine Aktionsgruppe.

### [Remove-AzureRmActivityLogAlert](Remove-AzureRmActivityLogAlert.md)
Entfernt eine Aktivitätsprotokoll Benachrichtigung.

### [Remove-AzureRmAlertRule](Remove-AzureRmAlertRule.md)
Entfernt eine Warnungsregel.

### [Remove-AzureRmAutoscaleSetting](Remove-AzureRmAutoscaleSetting.md)
Entfernt eine AutoScale-Einstellung.

### [Remove-AzureRmLogProfile](Remove-AzureRmLogProfile.md)
Entfernt ein Protokoll Profil.

### [Satz-AzureRmActionGroup](Set-AzureRmActionGroup.md)
Erstellt eine neue oder aktualisiert eine vorhandene Aktionsgruppe.

### [Satz-AzureRmActivityLogAlert](Set-AzureRmActivityLogAlert.md)
Erstellt ein neues oder legt eine vorhandene Aktivitätsprotokoll Benachrichtigung fest.

### [Satz-AzureRmDiagnosticSetting](Set-AzureRmDiagnosticSetting.md)
Legt die Einstellungen für Protokolle und Metriken für die Ressource fest.

