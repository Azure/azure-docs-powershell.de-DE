---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 7c9ee7af59acc90fba6a17e78ffd3dfc4822472d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937544"
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
Ruft Richtlinienauswertungsereignisse ab, die generiert werden, wenn Ressourcen erstellt oder aktualisiert werden. Richtlinienereigniseinträge können basierend auf dem angegebenen Zeitintervall (Standardwerte für den letzten Tag) in verschiedenen Bereichen abgefragt werden. Ergebnisse können gefiltert, gruppierend und Gruppenaggregationen berechnet werden.

## BEISPIELE

### Beispiel 1: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich
```powershell
PS C:\> Get-AzPolicyEvent
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.

### Beispiel 2: Erhalten von Richtlinienereignissen im angegebenen Abonnementbereich
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.

### Beispiel 3: Erhalten von Richtlinienereignissen im Verwaltungsgruppenbereich
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Verwaltungsgruppe generiert wurden.

### Beispiel 4: Erhalten von Richtlinienereignissen im Ressourcengruppenbereich im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Abonnement im aktuellen Sitzungskontext) generiert wurden.

### Beispiel 5: Erhalten von Richtlinienereignissen im Ressourcengruppenbereich im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.

### Beispiel 6: Erhalten von Richtlinienereignissen für eine Ressource
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für die angegebene Ressource generiert wurden.

### Beispiel 7: Erhalten von Richtlinienereignissen für eine Richtliniensatzdefinition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatzdefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 8: Erhalten von Richtlinienereignissen für eine Richtliniensatzdefinition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatzdefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 9: Erhalten von Richtlinienereignissen für eine Richtliniendefinition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniendefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 10: Erhalten von Richtlinienereignissen für eine Richtliniendefinition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 11: Erhalten von Richtlinienereignissen für eine Richtlinienzuordnung im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuordnung (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 12: Erhalten von Richtlinienereignissen für eine Richtlinienzuordnung im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuordnung (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 13: Erhalten von Richtlinienereignissen für eine Richtlinienzuordnung in der angegebenen Ressourcengruppe im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuordnung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 14: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit den Abfrageoptionen OrderBy, Top und Select
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl ordnet die Ergebnisse nach Zeitstempel- und Richtlinienzuordnungsnamenseigenschaften an und übernimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse.
Außerdem wird ausgewählt, dass nur eine Teilmenge der Spalten für jeden Datensatz aufgeführt wird.

### Beispiel 15: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit den Abfrageoptionen Von und An
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Ruft Richtlinienereigniseinträge ab, die innerhalb des Datumsbereichs generiert werden, der für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext angegeben ist.

### Beispiel 16: Anzeigen von Richtlinienereignissen im aktuellen Abonnementbereich mit Filterabfrageoption
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.
Der Befehl schränkt die Ergebnisse ein, die durch Filtern basierend auf richtliniendefinitionsbezogenen Aktionen (einschließlich Deny- oder Überwachungsaktionen) und Ressourcenspeicherort (ohne Ostspeicherort) zurückgegeben werden.

### Beispiel 17: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit Anwenden, die die Aggregation der Zeilenanzahl angeben
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Ruft die Anzahl der am letzten Tag generierten Richtlinienereigniseinträge für alle Ressourcen im Abonnement im aktuellen Sitzungskontext ab.
Der Befehl gibt nur die Anzahl der Richtlinienereigniseinträge zurück, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben werden.

### Beispiel 18: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit Anwenden der Angabe von Gruppierung mit Aggregation
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl schränkt die ergebnisse ein, die durch Filtern basierend auf der Richtliniendefinitionsaktion zurückgegeben werden (umfasst nur Überwachungs- und Deny-Ereignisse).
Sie gruppieren die Ergebnisse basierend auf Richtlinienzuordnung, Richtliniendefinition, Richtliniendefinitionsaktion und Ressourcen-ID und berechnet die Anzahl der Datensätze in jeder Gruppe, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben wird.
Sie ordnet die Ergebnisse nach der Aggregation der Anzahl in absteigender Reihenfolge an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse an.

### Beispiel 19: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit Anwenden der Angabe von Gruppierung ohne Aggregation
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl schränkt die ergebnisse ein, die durch Filtern basierend auf der Richtliniendefinitionsaktion zurückgegeben werden (umfasst nur Überwachungs- und Deny-Ereignisse).
Die Ergebnisse werden basierend auf der Ressourcen-ID gegruppen. Dadurch wird die Liste aller Ressourcen innerhalb des Abonnements generiert, die ein Richtlinienereignis für mindestens eine Überwachungs- oder Verweigernrichtlinie generiert haben.

### Beispiel 20: Erhalten von Richtlinienereignissen im aktuellen Abonnementbereich mit Anwenden, die mehrere Gruppierungen angeben
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Ruft Richtlinienereigniseinträge ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl schränkt die ergebnisse ein, die durch Filtern basierend auf der Richtliniendefinitionsaktion zurückgegeben werden (umfasst nur Deny-Ereignisse).
Die Ergebnisse werden zuerst basierend auf Richtlinienzuordnung, Richtliniendefinition und Ressourcen-ID gegruppen. Anschließend werden die Ergebnisse dieser Gruppierung mit denselben Eigenschaften mit Ausnahme der Ressourcen-ID weiter gruppieren und die Anzahl der Datensätze in jeder dieser Gruppen berechnet, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben werden.
Sie ordnet die Ergebnisse nach der Aggregation der Anzahl in absteigender Reihenfolge an und nimmt nur die obersten 5 der in dieser Reihenfolge aufgeführten Ergebnisse an.
Dadurch werden die fünf wichtigsten Verweigernrichtlinien mit der meisten verweigerten Ressourcen generiert.

## PARAMETER

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent

## NOTIZEN

## VERWANDTE LINKS
