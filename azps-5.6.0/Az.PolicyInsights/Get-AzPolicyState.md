---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 82aa08a3d4b4eb42638e1b9def55b5d936f176b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937499"
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
Ruft Richtlinienkonformitätszustände für Ressourcen ab. Richtlinienstatuseinträge können in verschiedenen Bereichen abgefragt werden. Basierend auf dem angegebenen Zeitintervall (standardmäßig bis zum letzten Tag) können entweder die neuesten Richtlinienzustände oder alle Richtlinienstatusübergänge abgefragt werden. Ergebnisse können gefiltert, gruppierend und Gruppenaggregationen berechnet werden.

## BEISPIELE

### Beispiel 1: Erhalten der neuesten Richtlinienzustände im aktuellen Abonnementbereich
```powershell
PS C:\> Get-AzPolicyState
```

Ruft die neuesten Am letzten Tag generierten Richtlinienstatusdatensätze für alle Ressourcen im Abonnement im aktuellen Sitzungskontext ab.

### Beispiel 2: Holen Sie sich die neuesten Richtlinienzustände im angegebenen Abonnementbereich.
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Ruft die neuesten Am letzten Tag generierten Richtlinienstatusdatensätze für alle Ressourcen innerhalb des angegebenen Abonnements ab.

### Beispiel 3: Alle Richtlinienzustände im aktuellen Abonnementbereich erhalten
```powershell
PS C:\> Get-AzPolicyState -All
```

Ruft alle datensätze des historischen Richtlinienzustands (einschließlich der letzten) ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.

### Beispiel 4: Holen Sie sich die neuesten Richtlinienzustände im Bereich der Verwaltungsgruppe.
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Ruft die neuesten Am letzten Tag generierten Richtlinienstatusdatensätze für alle Ressourcen in der angegebenen Verwaltungsgruppe ab.

### Beispiel 5: Aktuelle Richtlinienzustände im Ressourcengruppenbereich im aktuellen Abonnement erhalten
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

Ruft die neuesten Am letzten Tag generierten Richtlinienstatusdatensätze für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Abonnement im aktuellen Sitzungskontext) ab.

### Beispiel 6: Holen Sie sich die neuesten Richtlinienzustände im Ressourcengruppenbereich im angegebenen Abonnement.
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Ruft die neuesten Am letzten Tag generierten Richtlinienstatusdatensätze für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) ab.

### Beispiel 7: Holen Sie sich die neuesten Richtlinienzustände für eine Ressource.
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Ruft die neuesten Am letzten Tag generierten Richtlinienstatusdatensätze für die angegebene Ressource ab.

### Beispiel 8: Holen Sie sich die neuesten Richtlinienzustände für eine Richtliniensatzdefinition im aktuellen Abonnement.
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die neuesten Richtlinienstatuseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatzdefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 9: Holen Sie sich die neuesten Richtlinienzustände für eine Richtliniensatzdefinition im angegebenen Abonnement.
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die neuesten Richtlinienstatuseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatzdefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 10: Holen Sie sich die neuesten Richtlinienzustände für eine Richtliniendefinition im aktuellen Abonnement.
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die neuesten Richtlinienstatuseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 11: Holen Sie sich die neuesten Richtlinienzustände für eine Richtliniendefinition im angegebenen Abonnement.
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die neuesten Richtlinienstatuseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 12: Erhalten der neuesten Richtlinienzustände für eine Richtlinienzuweisung im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die neuesten Richtlinienstatuseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuordnung (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 13: Holen Sie sich die neuesten Richtlinienzustände für eine Richtlinienzuweisung im angegebenen Abonnement.
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die neuesten Richtlinienstatuseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuordnung (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 14: Holen Sie sich die neuesten Richtlinienzustände für eine Richtlinienzuordnung in der angegebenen Ressourcengruppe im aktuellen Abonnement.
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die neuesten Richtlinienstatuseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuordnung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 15: Holen Sie sich die neuesten Richtlinienzustände im aktuellen Abonnementbereich mit den Abfrageoptionen OrderBy, Top und Select.
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Ruft die neuesten Am letzten Tag generierten Richtlinienstatusdatensätze für alle Ressourcen im Abonnement im aktuellen Sitzungskontext ab. Der Befehl ordnet die Ergebnisse nach Zeitstempel- und Richtlinienzuordnungsnamenseigenschaften an und übernimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse.
Außerdem wird ausgewählt, dass nur eine Teilmenge der Spalten für jeden Datensatz aufgeführt wird.

### Beispiel 16: Holen Sie sich die neuesten Richtlinienzustände im aktuellen Abonnementbereich mit den Abfrageoptionen Von und An
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Ruft die neuesten Richtlinienstatusdatensätze ab, die innerhalb des datumsbezogenen Bereichs generiert werden, der für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext angegeben ist.

### Beispiel 17: Aktuelle Richtlinienzustände im aktuellen Abonnementbereich mit Filterabfrageoption
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Ruft die neuesten Am letzten Tag generierten Richtlinienstatusdatensätze für alle Ressourcen im Abonnement im aktuellen Sitzungskontext ab.
Der Befehl schränkt die Ergebnisse ein, die durch Filtern basierend auf Richtliniendefinitionsaktionen (einschließlich Deny- oder Überwachungsaktionen), Compliancestatus (nur nicht kompatibler Status) und Ressourcenspeicherort (schließt den Ostspeicherort aus) zurückgegeben werden.

### Beispiel 18: Holen Sie sich die neuesten Richtlinienzustände im aktuellen Abonnementbereich, mit Anwenden, der die Aggregation der Zeilenanzahl an gibt.
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Ruft die Anzahl der neuesten Richtlinienstatuseinträge ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.
Der Befehl gibt nur die Anzahl der Richtlinienstatuseinträge zurück, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben werden.

### Beispiel 19: Holen Sie sich die neuesten Richtlinienzustände im aktuellen Abonnementbereich, und geben Sie anwenden die Gruppierung mit Aggregation an.
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Ruft die neuesten Am letzten Tag generierten Richtlinienstatusdatensätze für alle Ressourcen im Abonnement im aktuellen Sitzungskontext ab. Der Befehl schränkt die ergebnisse ein, die durch Filtern basierend auf dem Compliancestatus zurückgegeben werden (umfasst nur den nicht kompatiblen Status).
Sie gruppieren die Ergebnisse basierend auf Richtlinienzuordnung, Richtliniensatzdefinition und Richtliniendefinition und berechnet die Anzahl der Datensätze in jeder Gruppe, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben wird.
Sie ordnet die Ergebnisse nach der Aggregation der Anzahl in absteigender Reihenfolge an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse an.

### Beispiel 20: Holen Sie sich die neuesten Richtlinienzustände im aktuellen Abonnementbereich, mit Anwenden, die Gruppierung ohne Aggregation angeben
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Ruft die neuesten Am letzten Tag generierten Richtlinienstatusdatensätze für alle Ressourcen im Abonnement im aktuellen Sitzungskontext ab. Der Befehl schränkt die ergebnisse ein, die durch Filtern basierend auf dem Compliancestatus zurückgegeben werden (umfasst nur den nicht kompatiblen Status).
Die Ergebnisse werden basierend auf der Ressourcen-ID gegruppen. Dadurch wird die Liste aller Ressourcen innerhalb des Abonnements generiert, die für mindestens eine Richtlinie nicht kompatibel sind.

### Beispiel 21: Holen Sie sich die neuesten Richtlinienzustände im aktuellen Abonnementbereich, und Anwenden gibt mehrere Gruppierungen an.
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### Beispiel 22: Erhalten der neuesten Richtlinienzustände einschließlich Richtlinienauswertungsdetails für eine Ressource
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Ruft die neuesten Am letzten Tag generierten Richtlinienstatusdatensätze für alle Ressourcen im Abonnement im aktuellen Sitzungskontext ab. Der Befehl schränkt die ergebnisse ein, die durch Filtern basierend auf dem Compliancestatus zurückgegeben werden (umfasst nur den nicht kompatiblen Status).
Die Ergebnisse werden zuerst basierend auf Richtlinienzuordnung, Richtliniensatzdefinition, Richtliniendefinition und Ressourcen-ID unterteilt. Anschließend werden die Ergebnisse dieser Gruppierung mit denselben Eigenschaften mit Ausnahme der Ressourcen-ID weiter gruppieren und die Anzahl der Datensätze in jeder dieser Gruppen berechnet, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben werden.
Sie ordnet die Ergebnisse nach der Aggregation der Anzahl in absteigender Reihenfolge an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse an.
Dadurch werden die fünf wichtigsten Richtlinien mit der meisten nicht kompatiblen Ressourcen generiert.

## PARAMETER

### -Alle
Erhalten Sie innerhalb des angegebenen Zeitintervalls alle Richtlinienzustände anstelle der neuesten.

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

### -Erweitern
Erweitern Des Ausdrucks mithilfe der OData-Notation.

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
Filtern sie Ausdruck mithilfe der OData-Notation.

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
Nach ISO 8601 formatierter Zeitstempel, der die Startzeit des Abfrageintervalls an gibt.
Wenn nicht angegeben, wird standardmäßig der Parameterwert "An" minus 1 Tag festgelegt.

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
Sortierausdruck mithilfe der OData-Notation.
Ein oder mehrere durch Kommas getrennte Spaltennamen mit einem optionalen "desc" (standard) oder "asc".

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
Richtliniendefinitionsname.

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
Name der Ressourcengruppe.

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
Wählen Sie Ausdruck mithilfe der OData-Notation aus.
Mindestens ein durch Kommas getrennte Spaltennamen.
Beschränkt die Spalten für jeden Datensatz auf nur die angeforderten.

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
Nach ISO 8601 formatierter Zeitstempel, der die Endzeit des Abfrageintervalls an gibt.
Wenn nicht angegeben, wird standardmäßig die Uhrzeit der Anforderung festgelegt.

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
Maximale Anzahl von Datensätzen, die zurückzukehren sind.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState

## NOTIZEN

## VERWANDTE LINKS

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
