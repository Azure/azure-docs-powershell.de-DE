---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160417"
---
# Get-AzPolicyEvent

## SYNOPSIS
Ruft Richtlinienauswertungsereignisse ab, die generiert werden, wenn Ressourcen erstellt oder aktualisiert werden.

## SYNTAX

### SubscriptionScope (Standard)
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Ruft Richtlinienauswertungsereignisse ab, die generiert werden, wenn Ressourcen erstellt oder aktualisiert werden. Richtlinienereignisdatensätze können basierend auf dem angegebenen Zeitintervall (Standardwert auf "Letzter Tag"). Ergebnisse können gefiltert, grouped und Gruppenaggregationen berechnet werden.

## BEISPIELE

### Beispiel 1: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich
```powershell
PS C:\> Get-AzPolicyEvent
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.

### Beispiel 2: Erhalten von Richtlinienereignissen im angegebenen Abonnementbereich
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.

### Beispiel 3: Erhalten von Richtlinienereignissen im Bereich der Verwaltungsgruppe
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen in der angegebenen Verwaltungsgruppe generiert wurden.

### Beispiel 4: Erhalten von Richtlinienereignissen im Ressourcengruppenbereich im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Abonnement im aktuellen Sitzungskontext) generiert wurden.

### Beispiel 5: Erhalten von Richtlinienereignissen im Ressourcengruppenbereich im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.

### Beispiel 6: Erhalten von Richtlinienereignissen für eine Ressource
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für die angegebene Ressource generiert wurden.

### Beispiel 7: Erhalten von Richtlinienereignissen für eine Richtliniensatzdefinition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatzdefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 8: Erhalten von Richtlinienereignissen für eine Richtliniensatzdefinition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatzdefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 9: Erhalten von Richtlinienereignissen für eine Richtliniendefinition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 10: Erhalten von Richtlinienereignissen für eine Richtliniendefinition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 11: Erhalten von Richtlinienereignissen für eine Richtlinienzuweisung im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 12: Erhalten von Richtlinienereignissen für eine Richtlinienzuweisung im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 13: Erhalten von Richtlinienereignissen für eine Richtlinienzuweisung in der angegebenen Ressourcengruppe im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 14: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit den Abfrageoptionen "OrderBy", "Top" und "Select"
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden. Der Befehl ordnet die Ergebnisse nach Zeitstempel und Eigenschaften des Namens der Richtlinienzuweisung an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgelisteten Ergebnisse an.
Außerdem wird ausgewählt, dass nur eine Teilmenge der Spalten für jeden Datensatz aufgeführt wird.

### Beispiel 15: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit den Abfrageoptionen "Von" und "An"
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Ruft Richtlinienereignisdatensätze ab, die innerhalb des datumsbezogenen Bereichs generiert werden, der für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext angegeben ist.

### Beispiel 16: Anzeigen von Richtlinienereignissen im aktuellen Abonnementbereich mit Filterabfrageoption
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.
Der Befehl beschränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf einer Richtliniendefinitionsaktion (einschließlich Verweigern- oder Überwachungsaktionen) und dem Ressourcenspeicherort (schließt den Oststandort aus).

### Beispiel 17: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit "Anwenden" als Aggregation der Zeilenanzahl
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Ruft die Anzahl der am letzten Tag generierten Richtlinienereignisdatensätze für alle Ressourcen im Abonnement im aktuellen Sitzungskontext ab.
Der Befehl gibt nur die Anzahl der Richtlinienereigniseinträge zurück, die in der Eigenschaft "AdditionalProperties" zurückgegeben wird.

### Beispiel 18: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich, mit "Anwenden" als Gruppierung mit Aggregation
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden. Der Befehl beschränkt die durch das Filtern auf Basis einer Richtliniendefinitionsaktion zurückgegebenen Ergebnisse (umfasst nur Überwachungs- und Verweigernereignisse).
Sie gruppieren die Ergebnisse basierend auf Richtlinienzuordnung, Richtliniendefinition, Richtliniendefinitionsaktion und Ressourcen-ID und berechnen die Anzahl von Datensätzen in jeder Gruppe, die in der Eigenschaft "AdditionalProperties" zurückgegeben wird.
Er ordnet die Ergebnisse nach der Anzahlaggregation in absteigender Reihenfolge an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse an.

### Beispiel 19: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich, mit "Anwenden" als Gruppierung ohne Aggregation
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden. Der Befehl beschränkt die durch das Filtern auf Basis einer Richtliniendefinitionsaktion zurückgegebenen Ergebnisse (umfasst nur Überwachungs- und Verweigernereignisse).
Die Ergebnisse werden basierend auf der Ressourcen-ID gruppenweise. Dadurch wird die Liste aller Ressourcen innerhalb des Abonnements generiert, von dem ein Richtlinienereignis für mindestens eine Überwachungs- oder Verweigernrichtlinie generiert wurde.

### Beispiel 20: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit "Anwenden" mit Angabe mehrerer Gruppierungen
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Ruft Richtlinienereignisdatensätze ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden. Der Befehl schränkt die von der Filterung auf Grundlage einer Richtliniendefinitionsaktion zurückgegebenen Ergebnisse ein (umfasst nur "Verweigern"-Ereignisse).
Die Ergebnisse werden zuerst basierend auf Richtlinienzuweisung, Richtliniendefinition und Ressourcen-ID gruppenweise. Anschließend werden die Ergebnisse dieser Gruppierung mit denselben Eigenschaften mit Ausnahme der Ressourcen-ID weiter gruppieren und die Anzahl von Datensätzen in jeder dieser Gruppen berechnet, die in der Eigenschaft "AdditionalProperties" zurückgegeben wird.
Er ordnet die Ergebnisse nach der Anzahlaggregation in absteigender Reihenfolge an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse an.
Dadurch werden die 5 am häufigsten abgelehnten Richtlinien mit der größten Anzahl verweigerter Ressourcen generiert.

## PARAMETERS

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
