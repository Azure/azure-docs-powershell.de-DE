---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 790d22fbf08da8c03b35b7f53559a92924cadd6f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823971"
---
# Get-AzPolicyState

## Synopsis
Ruft Richtlinien Kompatibilitätsstatus für Ressourcen ab.

## Syntax

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

## Beschreibung
Ruft Richtlinien Kompatibilitätsstatus für Ressourcen ab. Richtlinien Zustandsdaten Sätze können in verschiedenen Bereichen abgefragt werden. Basierend auf dem angegebenen Zeitintervall (standardmäßig auf den letzten Tag) können entweder die neuesten Richtlinienzustände oder alle Richtlinien Zustandsübergänge abgefragt werden. Ergebnisse können gefiltert, gruppiert und Gruppen Aggregationen berechnet werden.

## Beispiele

### Beispiel 1: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich
```powershell
PS C:\> Get-AzPolicyState
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.

### Beispiel 2: Abrufen der neuesten Richtlinienstatus im angegebenen Abonnement Bereich
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.

### Beispiel 3: Abrufen aller Richtlinienzustände im aktuellen Abonnement Bereich
```powershell
PS C:\> Get-AzPolicyState -All
```

Ruft alle Verlaufs Richtlinien Zustandsdaten Sätze (einschließlich der neuesten) ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.

### Beispiel 4: Abrufen der neuesten Richtlinienstatus im Verwaltungsgruppen Bereich
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Verwaltungsgruppe generiert wurden.

### Beispiel 5: Abrufen der neuesten Richtlinienstatus im Ressourcengruppen Bereich im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Kontext des Abonnements im aktuellen Sitzungskontext) generiert wurden.

### Beispiel 6: Abrufen der neuesten Richtlinienstatus im Ressourcengruppen Bereich im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.

### Beispiel 7: Abrufen der neuesten Richtlinienstatus für eine Ressource
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für die angegebene Ressource generiert wurden.

### Beispiel 8: Abrufen der neuesten Richtlinienstatus für eine Richtliniensatz Definition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatz Definition (die im aktuellen Sitzungskontext im Abonnement vorhanden ist) erzeugt wurden.

### Beispiel 9: Abrufen der neuesten Richtlinienstatus für eine Richtliniensatz Definition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatz Definition (die im angegebenen Abonnement vorhanden ist) erzeugt wurden.

### Beispiel 10: Abrufen der neuesten Richtlinienstatus für eine Richtliniendefinition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniendefinition (die in dem Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.

### Beispiel 11: Abrufen der neuesten Richtlinienstatus für eine Richtliniendefinition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) bewirkt wurden.

### Beispiel 12: Abrufen der neuesten Richtlinienstatus für eine Richtlinien Aufgabe im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die in dem Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.

### Beispiel 13: Abrufen der neuesten Richtlinienstatus für eine Richtlinien Aufgabe im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die im angegebenen Abonnement vorhanden ist) erzeugt wurden.

### Beispiel 14: Abrufen der neuesten Richtlinienstatus für eine Richtlinienzuweisung in der angegebenen Ressourcengruppe im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.

### Beispiel 15: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich mit OrderBy, Top und Auswählen von Abfrageoptionen
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl ordnet die Ergebnisse nach Timestamp-und Richtlinien Zuordnungsnamen-Eigenschaften an und nimmt nur die ersten fünf der in dieser Reihenfolge aufgelisteten Daten an.
Außerdem wird ausgewählt, um nur eine Teilmenge der Spalten für jeden Datensatz aufzulisten.

### Beispiel 16: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich mit den Optionen von und zu Abfrage
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die innerhalb des für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext angegebenen Datumsbereichs generiert wurden.

### Beispiel 17: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich mit der Option "Filter Abfrage"
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and IsCompliant eq false and ResourceLocation ne 'eastus'"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.
Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf der Richtlinien Definitions Aktion (einschließlich Deny-oder Überwachungsaktionen), dem Kompatibilitätsstatus (nur nicht kompatiblen Status) und dem Ressourcen Standort ein (schließt eastus-Standort aus).

### Beispiel 18: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich, wobei Apply die Aggregation der Zeilenanzahl angibt
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Ruft die Anzahl der neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.
Der Befehl gibt nur die Anzahl der Richtlinien Zustandsdaten Sätze zurück, die in der AdditionalProperties-Eigenschaft zurückgegeben werden.

### Beispiel 19: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich mit Apply, der die Gruppierung mit Aggregation angibt
```powershell
PS C:\> Get-AzPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf dem Kompatibilitätsstatus ein (enthält nur nicht kompatiblen Status).
Sie gruppiert die Ergebnisse basierend auf Richtlinienzuweisung, Richtliniensatz Definition und Richtliniendefinition und berechnet die Anzahl der Datensätze in jeder Gruppe, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben wird.
Sie ordnet die Ergebnisse nach der Anzahl Aggregation in absteigender Reihenfolge an und nimmt nur die ersten fünf der in dieser Reihenfolge aufgelisteten Daten auf.

### Beispiel 20: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich mit Apply, der die Gruppierung ohne Aggregation angibt
```powershell
PS C:\> Get-AzPolicyState -Filter "IsCompliant eq false" -Apply "groupby((ResourceId))"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf dem Kompatibilitätsstatus ein (enthält nur nicht kompatiblen Status).
Sie gruppiert die Ergebnisse auf der Grundlage der Ressourcen-ID. Dadurch wird die Liste aller Ressourcen innerhalb des Abonnements generiert, die für mindestens eine Richtlinie nicht kompatibel sind.

### Beispiel 21: Abrufen der neuesten Richtlinienzustände im aktuellen Abonnement Bereich mit Apply, der mehrere Gruppierungen angibt
```powershell
PS C:\> Get-AzPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### Beispiel 22: Abrufen der neuesten Richtlinienzustände einschließlich Richtlinien Auswertungs Details für eine Ressource 
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Ruft die neuesten Richtlinien Zustandsdaten Sätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf dem Kompatibilitätsstatus ein (enthält nur nicht kompatiblen Status).
Sie gruppiert die Ergebnisse zuerst basierend auf Richtlinienzuweisung, Richtliniensatz Definition, Richtliniendefinition und Ressourcen-ID. Anschließend werden die Ergebnisse dieser Gruppierung mit den gleichen Eigenschaften, mit Ausnahme der Ressourcen-ID, gruppiert, und die Anzahl der Datensätze in jeder dieser Gruppen wird berechnet, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben wird.
Sie ordnet die Ergebnisse nach der Anzahl Aggregation in absteigender Reihenfolge an und nimmt nur die ersten fünf der in dieser Reihenfolge aufgelisteten Daten auf.
Dadurch werden die obersten fünf Richtlinien mit der größten Anzahl nicht kompatibler Ressourcen generiert.

## Parameter

### – Alle
Rufen Sie innerhalb des angegebenen Zeitintervalls alle Richtlinienzustände anstelle der neuesten ab.

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
Anwenden des Ausdrucks für Aggregationen mithilfe der OData-Notation

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### – Erweitern
Erweitern des Ausdrucks mithilfe der OData-Notation

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
Filter Ausdruck mit OData-Notation

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

### -Ab
ISO 8601 formatierter Zeitstempel, der die Startzeit des abzufragenden Intervalls angibt.
Wenn Sie nicht angegeben wird, wird standardmäßig "bis"-Parameterwert minus 1 Tag angegeben.

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
Sortierausdruck mit OData-Notation
Eine oder mehrere durch trennzeichengetrennte Spaltennamen mit einem optionalen "DESC" (Standardwert) oder "ASC".

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
Name der Richtlinienzuordnung

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
Name der Richtliniendefinition

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
Richtliniensatz-Definitionsname

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

### -Resourcen-Nr
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

### -Wählen Sie
Wählen Sie Ausdruck mit OData-Notation aus.
Ein oder mehrere durch trennzeichengetrennte Spaltennamen.
Schränkt die Spalten für jeden Datensatz auf nur die angeforderten ein.

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

### -Abonnement-Nr
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
ISO 8601 formatierter Zeitstempel, der die Endzeit des abzufragenden Intervalls angibt.
Wenn keine Angabe erfolgt, wird standardmäßig der Zeitpunkt der Anforderung angegeben.

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
Die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. PolicyInsights. Models. PolicyState

## Notizen

## Verwandte Links

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
