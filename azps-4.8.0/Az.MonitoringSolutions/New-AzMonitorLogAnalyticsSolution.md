---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166486"
---
# New-AzMonitorLogAnalyticsSolution

## Synopsis
Erstellt eine Protokollanalyse Lösung.

## Syntax

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Beschreibung
Erstellt eine Protokollanalyse Lösung.

## Beispiele

### Beispiel 1: Erstellen einer Überwachungsprotokoll Analyse-Lösung für den Arbeitsbereich "Protokollanalyse"
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

Mit diesem Befehl wird eine Überwachungsprotokoll Analyse Lösung für den Arbeitsbereich "Protokollanalyse" erstellt.

Häufig verwendete Typen sind:

| Geben | Beschreibung |
| :-----| :----- |
| SecurityCenterFree |  Azure Security Center – ﻿kostenlose Edition |
| Sicherheits | Azure-Sicherheits Center |
| Updates | Update Verwaltung |
| ContainerInsights | Azure Monitor für Container |
| ServiceMap | Service Karte |
| Azure | Aktivitätsprotokoll Analyse |
| ChangeTracking | Änderungsnachverfolgung und Inventar |
| VMInsights | Azure Monitor für VMS |
| SecurityInsights | Azure Sentinel |
| NetworkMonitoring | Netzwerk Leistungs Monitor |
| SQLVulnerabilityAssessment | SQL-Anfälligkeitsbewertung |
| SQLAdvancedThreatProtection | Erweiterter SQL-Bedrohungsschutz |
| Antischadsoftware | Antimalware-Bewertung |
| AzureAutomation | Automatisierungs-Hybrid Worker |
| LogicAppsManagement | Verwaltung von Logic-apps |
| SQLDataClassification | SQL-Daten Ermittlungs & Klassifizierung |

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Ressourcen Standort.
Muss derselbe wie der Protokollanalyse-Arbeitsbereich sein.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe, die abgerufen werden soll.
Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Abonnement-Nr
Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.
Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Ressourcenkategorien

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Typ
Der Typ der zu erstellende Projektmappe.
Beispiel: "Container".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceResourceId
Die Azure-Ressourcen-ID für den Arbeitsbereich, in dem die Lösung bereitgestellt/aktiviert wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. MonitoringSolutions. Models. Api20151101Preview. ISolution

## Notizen

Aliase

## Verwandte Links



[Get-AzOperationalInsightsWorkspace](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

