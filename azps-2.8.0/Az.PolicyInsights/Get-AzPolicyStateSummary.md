---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: 93c31a9a8a1b2f161553efdabce2d97ed19caacd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823964"
---
# Get-AzPolicyStateSummary

## Synopsis
Ruft die aktuelle Zusammenfassung der Richtlinien Konformitätsstatus für Ressourcen ab.

## Syntax

### SubscriptionScope (Standard)
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Ruft eine Zusammenfassungsansicht der neuesten Richtlinien Kompatibilitätszustands Nummern in verschiedenen Bereichen ab, aufgeschlüsselt nach Richtlinienzuweisungen und Richtlinien Definitionen. Es enthält nur nicht richtlinienkonforme Richtlinienzustände.

## Beispiele

### Beispiel 1: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im aktuellen Abonnement Bereich
```powershell
PS C:\> Get-AzPolicyStateSummary
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.

### Beispiel 2: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im angegebenen Abonnement Bereich
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.

### Beispiel 3: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im Verwaltungsgruppen Bereich
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Verwaltungsgruppe generiert wurden.

### Beispiel 4: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im Ressourcengruppen Bereich im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Kontext des Abonnements im aktuellen Sitzungskontext) generiert wurden.

### Beispiel 5: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im Ressourcengruppen Bereich im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.

### Beispiel 6: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Ressource
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für die angegebene Ressource generiert wurden.

### Beispiel 7: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtliniensatz Definition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatz Definition (die in dem Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.

### Beispiel 8: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtliniensatz Definition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatz Definition (die im angegebenen Abonnement vorhanden ist) erzeugt wurden.

### Beispiel 9: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtliniendefinition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniendefinition (die in dem Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.

### Beispiel 10: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtliniendefinition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) bewirkt wurden.

### Beispiel 11: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtlinien Aufgabe im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die in den letzten Tagen für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die in dem Abonnement im aktuellen Sitzungskontext vorhanden ist) bewirkt wurden.

### Beispiel 12: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtlinien Aufgabe im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die in den letzten Tagen für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die im angegebenen Abonnement vorhanden ist) bewirkt wurden.

### Beispiel 13: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung für eine Richtlinien Aufgabe in der angegebenen Ressourcengruppe im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die in den letzten Tagen für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuweisung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) erfolgen.

### Beispiel 14: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im aktuellen Abonnement Bereich mit der Option "obere Abfrage"
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl ordnet die Richtlinien Zuordnungs Zusammenfassungen in den Ergebnissen nach nicht kompatiblen Ressourcen Zählern in absteigender Reihenfolge an und nimmt nur die ersten fünf dieser Richtlinien Zuordnungs Zusammenfassungen auf.

### Beispiel 15: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im aktuellen Abonnement Bereich mit den Optionen von und zu Abfrage
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die innerhalb des für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext angegebenen Datumsbereichs generiert wurden.

### Beispiel 16: Abrufen der letzten nicht kompatiblen Richtlinienstatus Zusammenfassung im aktuellen Abonnement Bereich mit der Option "Filter Abfrage"
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinien Konformitätsstatus ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.
Der Befehl schränkt die von Filtern zurückgegebenen Ergebnisse auf der Grundlage der Richtlinien Definitions Aktion (einschließlich Deny-oder Überwachungsaktionen) und des Ressourcen Speicherorts ein (schließt eastus-Standort aus).

## Parameter

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

### Microsoft. Azure. Commands. PolicyInsights. Models. PolicyStateSummary

## Notizen

## Verwandte Links

[Get-AzPolicyState](./Get-AzPolicyState.md)
