---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
ms.openlocfilehash: 0c4e4f531dac3f75f0eff69ba1dcfc644473ea06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498205"
---
# Get-AzureRmPolicyEvent

## Synopsis
Ruft Richtlinien Auswertungs Ereignisse ab, die beim Erstellen oder Aktualisieren von Ressourcen generiert wurden.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### SubscriptionScope (Standard)
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzureRmPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzureRmPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Ruft Richtlinien Auswertungs Ereignisse ab, die beim Erstellen oder Aktualisieren von Ressourcen generiert wurden. Richtlinien Ereigniseinträge können anhand des angegebenen Zeitintervalls in unterschiedlichen Bereichen abgefragt werden (Standardmäßig ist der letzte Tag). Ergebnisse können gefiltert, gruppiert und Gruppen Aggregationen berechnet werden.

## Beispiele

### Beispiel 1: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich
```powershell
PS C:\> Get-AzureRmPolicyEvent
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.

### Beispiel 2: Abrufen von Richtlinien Ereignissen im angegebenen Abonnement Bereich
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.

### Beispiel 3: Abrufen von Richtlinien Ereignissen im Verwaltungsgruppen Bereich
```powershell
PS C:\> Get-AzureRmPolicyEvent -ManagementGroupName "myManagementGroup"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Verwaltungsgruppe generiert wurden.

### Beispiel 4: Abrufen von Richtlinien Ereignissen im Ressourcengruppen Bereich im aktuellen Abonnement
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Kontext des Abonnements im aktuellen Sitzungskontext) generiert wurden.

### Beispiel 5: Abrufen von Richtlinien Ereignissen im Ressourcengruppen Bereich des angegebenen Abonnements
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.

### Beispiel 6: Abrufen von Richtlinien Ereignissen für eine Ressource
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für die angegebene Ressource generiert wurden.

### Beispiel 7: Abrufen von Richtlinien Ereignissen für eine Richtliniensatz Definition im aktuellen Abonnement
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatz Definition (die im aktuellen Sitzungskontext im Abonnement vorhanden ist) generiert wurden.

### Beispiel 8: Abrufen von Richtlinien Ereignissen für eine Richtliniensatz Definition im angegebenen Abonnement
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatz Definition (die im angegebenen Abonnement vorhanden ist) erzeugt wurden.

### Beispiel 9: Abrufen von Richtlinien Ereignissen für eine Richtliniendefinition im aktuellen Abonnement
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniendefinition (die im aktuellen Sitzungskontext im Abonnement vorhanden ist) erzeugt wurden.

### Beispiel 10: Abrufen von Richtlinien Ereignissen für eine Richtliniendefinition im angegebenen Abonnement
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) erzeugt wurden.

### Beispiel 11: Abrufen von Richtlinien Ereignissen für eine Richtlinien Aufgabe im aktuellen Abonnement
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die im aktuellen Sitzungskontext im Abonnement vorhanden ist) erzeugt wurden.

### Beispiel 12: Abrufen von Richtlinien Ereignissen für eine Richtlinien Aufgabe im angegebenen Abonnement
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die im angegebenen Abonnement vorhanden ist) erzeugt wurden.

### Beispiel 13: Abrufen von Richtlinien Ereignissen für eine Richtlinienzuweisung in der angegebenen Ressourcengruppe im aktuellen Abonnement
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.

### Beispiel 14: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich mit OrderBy, Top und Auswählen von Abfrageoptionen
```powershell
PS C:\> Get-AzureRmPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl ordnet die Ergebnisse nach Timestamp-und Richtlinien Zuordnungsnamen-Eigenschaften an und nimmt nur die ersten fünf der in dieser Reihenfolge aufgelisteten Daten an.
Außerdem wird ausgewählt, um nur eine Teilmenge der Spalten für jeden Datensatz aufzulisten.

### Beispiel 15: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich mit den Abfrageoptionen "von" und "zu"
```powershell
PS C:\> Get-AzureRmPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Ruft Richtlinien Ereignisdatensätze ab, die innerhalb des für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext angegebenen Datumsbereichs generiert wurden.

### Beispiel 16: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich mit der Option "Filter Abfrage"
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.
Der Befehl schränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf der Richtlinien Definitions Aktion (einschließlich Deny-oder Überwachungsaktionen) und dem Ressourcen Standort ein (schließt eastus-Standort aus).

### Beispiel 17: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich, wobei Apply die Aggregation der Zeilenanzahl angibt
```powershell
PS C:\> Get-AzureRmPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Ruft die Anzahl von Richtlinien Ereignisdatensätzen ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.
Der Befehl gibt nur die Anzahl der Richtlinien Ereignisdatensätze zurück, die in der AdditionalProperties-Eigenschaft zurückgegeben werden.

### Beispiel 18: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich mit Apply, der die Gruppierung mit Aggregation angibt
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl schränkt die von Filtern zurückgegebenen Ergebnisse basierend auf der Richtlinien Definitions Aktion ein (umfasst nur Überwachungs-und ablehnungsereignisse).
Sie gruppiert die Ergebnisse basierend auf Richtlinienzuweisung, Richtliniendefinition, Richtlinien Definitions Aktion und Ressourcen-ID und berechnet die Anzahl der Datensätze in jeder Gruppe, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben wird.
Sie ordnet die Ergebnisse nach der Anzahl Aggregation in absteigender Reihenfolge an und nimmt nur die ersten fünf der in dieser Reihenfolge aufgelisteten Daten auf.

### Beispiel 19: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich mit Apply, der die Gruppierung ohne Aggregation angibt
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl schränkt die von Filtern zurückgegebenen Ergebnisse basierend auf der Richtlinien Definitions Aktion ein (umfasst nur Überwachungs-und ablehnungsereignisse).
Sie gruppiert die Ergebnisse auf der Grundlage der Ressourcen-ID. Dadurch wird die Liste aller Ressourcen innerhalb des Abonnements generiert, die ein Richtlinien Ereignis für mindestens eine Überwachungs-oder Ablehnungs Richtlinie generiert haben.

### Beispiel 20: Abrufen von Richtlinien Ereignissen im aktuellen Abonnement Bereich mit Apply, der mehrere Gruppierungen angibt
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Ruft Richtlinien Ereignisdatensätze ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl schränkt die von Filtern zurückgegebenen Ergebnisse auf der Grundlage der Richtlinien Definitions Aktion ein (enthält nur Deny-Ereignisse).
Sie gruppiert die Ergebnisse zuerst basierend auf Richtlinienzuweisung, Richtliniendefinition und Ressourcen-ID. Anschließend werden die Ergebnisse dieser Gruppierung mit den gleichen Eigenschaften, mit Ausnahme der Ressourcen-ID, gruppiert, und die Anzahl der Datensätze in jeder dieser Gruppen wird berechnet, die innerhalb der AdditionalProperties-Eigenschaft zurückgegeben wird.
Sie ordnet die Ergebnisse nach der Anzahl Aggregation in absteigender Reihenfolge an und nimmt nur die ersten fünf der in dieser Reihenfolge aufgelisteten Daten auf.
Dadurch werden die obersten 5 Deny-Richtlinien mit der meisten Anzahl verweigerter Ressourcen generiert.

## Parameter

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. PolicyInsights. Models. PolicyEvent

## Notizen

## Verwandte Links
