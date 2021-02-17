---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172266"
---
# Get-AzPolicyState

## SYNOPSIS
Ruft Richtlinienkonformitätszustände für Ressourcen ab.

## SYNTAX

### SubscriptionScope (Standard)
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Ruft Richtlinienkonformitätszustände für Ressourcen ab. Datensätze des Richtlinienstatus können in verschiedenen Bereichen abgefragt werden. Basierend auf dem angegebenen Zeitintervall (standardmäßig auf "Letzter Tag" festgelegt) können entweder die neuesten Richtlinienzustände oder alle Übergänge des Richtlinienstatus abgefragt werden. Ergebnisse können gefiltert, grouped und Gruppenaggregationen berechnet werden.

## BEISPIELE

### Beispiel 1: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich
```powershell
PS C:\> Get-AzPolicyState
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.

### Beispiel 2: Erhalten der neuesten Richtlinienzustände im angegebenen Abonnementbereich
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.

### Beispiel 3: Alle Richtlinienzustände im aktuellen Abonnementbereich erhalten
```powershell
PS C:\> Get-AzPolicyState -All
```

Ruft alle Datensätze des vergangenen Richtlinienstatus (einschließlich der letzten) ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.

### Beispiel 4: Erhalten der neuesten Richtlinienzustände im Bereich der Verwaltungsgruppe
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen in der angegebenen Verwaltungsgruppe generiert wurden.

### Beispiel 5: Erhalten der neuesten Richtlinienzustände im Ressourcengruppenbereich im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Abonnement im aktuellen Sitzungskontext) generiert wurden.

### Beispiel 6: Erhalten der neuesten Richtlinienzustände im Ressourcengruppenbereich im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.

### Beispiel 7: Erhalten der neuesten Richtlinienzustände für eine Ressource
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für die angegebene Ressource generiert wurden.

### Beispiel 8: Erhalten der neuesten Richtlinienzustände für eine Richtliniensatzdefinition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatzdefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 9: Erhalten der neuesten Richtlinienzustände für eine Richtliniensatzdefinition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatzdefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 10: Erhalten der neuesten Richtlinienzustände für eine Richtliniendefinition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 11: Erhalten der neuesten Richtlinienzustände für eine Richtliniendefinition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 12: Erhalten der neuesten Richtlinienzustände für eine Richtlinienzuweisung im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 13: Erhalten der neuesten Richtlinienzustände für eine Richtlinienzuweisung im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 14: Erhalten der neuesten Richtlinienzustände für eine Richtlinienzuweisung in der angegebenen Ressourcengruppe im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 15: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit den Abfrageoptionen "OrderBy", "Top" und "Select"
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden. Der Befehl ordnet die Ergebnisse nach Zeitstempel und Eigenschaften des Namens der Richtlinienzuweisung an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgelisteten Ergebnisse an.
Außerdem wird ausgewählt, dass nur eine Teilmenge der Spalten für jeden Datensatz aufgeführt wird.

### Beispiel 16: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit den Abfrageoptionen "Von" und "An"
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die innerhalb des datumsbezogenen Bereichs generiert werden, der im aktuellen Sitzungskontext für alle Ressourcen im Abonnement angegeben ist.

### Beispiel 17: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit Filterabfrageoption
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.
Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse auf Grundlage einer Richtliniendefinitionsaktion (einschließlich Verweigern- oder Überwachungsaktionen), dem Compliancestatus (einschließlich nicht kompatiblem Status) und dem Ressourcenspeicherort ein (schließt den Oststandort aus).

### Beispiel 18: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit "Anwenden" als Aggregation der Zeilenanzahl
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Ruft die Anzahl der neuesten Richtlinienstatusdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.
Der Befehl gibt nur die Anzahl der Richtlinienstatusdatensätze zurück, die in der Eigenschaft "AdditionalProperties" zurückgegeben wird.

### Beispiel 19: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit "Anwenden" als Angabe der Gruppierung mit Aggregation
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden. Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf dem Compliancestatus ein (umfasst nur den nicht kompatiblen Status).
Sie gruppieren die Ergebnisse basierend auf Richtlinienzuweisung, Richtliniensatzdefinition und Richtliniendefinition und berechnen die Anzahl von Datensätzen in jeder Gruppe, die in der Eigenschaft "AdditionalProperties" zurückgegeben wird.
Er ordnet die Ergebnisse nach der Anzahlaggregation in absteigender Reihenfolge an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse an.

### Beispiel 20: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit "Anwenden" als Angabe der Gruppierung ohne Aggregation
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden. Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf dem Compliancestatus ein (umfasst nur den nicht kompatiblen Status).
Die Ergebnisse werden basierend auf der Ressourcen-ID gruppenweise. Dadurch wird die Liste aller Ressourcen im Abonnement generiert, die für mindestens eine Richtlinie nicht kompatibel sind.

### Beispiel 21: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich mit "Anwenden" mit Angabe mehrerer Gruppierungen
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### Beispiel 22: Erhalten der neuesten Richtlinienzustände, einschließlich Richtlinienauswertungsdetails für eine Ressource
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Ruft die neuesten Datensätze zum Richtlinienstatus ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden. Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf dem Compliancestatus ein (umfasst nur den nicht kompatiblen Status).
Die Ergebnisse werden zuerst basierend auf Richtlinienzuweisung, Richtliniensatzdefinition, Richtliniendefinition und Ressourcen-ID gruppen. Anschließend werden die Ergebnisse dieser Gruppierung mit denselben Eigenschaften mit Ausnahme der Ressourcen-ID weiter gruppieren und die Anzahl von Datensätzen in jeder dieser Gruppen berechnet, die in der Eigenschaft "AdditionalProperties" zurückgegeben wird.
Er ordnet die Ergebnisse nach der Anzahlaggregation in absteigender Reihenfolge an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse an.
Dadurch werden die 5 wichtigsten Richtlinien mit der meisten nicht kompatiblen Ressourcen generiert.

## PARAMETERS

### -Alle
Innerhalb des angegebenen Zeitintervalls alle Richtlinienzustände anstelle der neuesten erhalten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Apply
Anwenden von Ausdrücken auf Aggregationen mithilfe der OData-Notation.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -Expand
Erweitern sie den Ausdruck mithilfe der OData-Notation.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Filtern von Ausdrücken mithilfe der OData-Notation.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Von
IN ISO 8601 formatierter Zeitstempel, der die Startzeit des zu abfragenden Intervalls an gibt.
Ist diese Einstellung nicht angegeben, wird standardmäßig der Parameterwert "An" minus 1 Tag verwendet.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupName
Name der Verwaltungsgruppe.

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrderBy
Sortierung des Ausdrucks mithilfe der OData-Notation.
Ein oder mehrere durch Kommas getrennte Spaltennamen mit einem optionalen "Desc" (Standard) oder "asc".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyAssignmentName
Name der Richtlinienzuweisung.

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionName
Name der Richtliniendefinition.

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicySetDefinitionName
Name der Richtliniensatzdefinition.

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Ressourcengruppenname.

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Ressourcen-ID.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Select
Auswählen von Ausdrücken mithilfe der OData-Notation.
Mindestens ein durch Kommas getrennte Spaltennamen.
Beschränkt die Spalten in jedem Datensatz auf die angeforderten Spalten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Abonnement-ID.

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -To
IN ISO 8601 formatierter Zeitstempel, der die Endzeit des zu abfragenden Intervalls an gibt.
Ist diese Angabe nicht angegeben, wird standardmäßig der Zeitpunkt der Anforderung verwendet.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
Maximale Anzahl der zurückzukehrende Datensätze.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
