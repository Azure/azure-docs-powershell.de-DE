---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: 09fce075ae0f6d8c55f5ef18d070a72daafa2cac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937496"
---
# Get-AzPolicyStateSummary

## SYNOPSIS
Ruft die neueste Zusammenfassung der Richtlinienkonformitätszustände für Ressourcen ab.

## SYNTAX

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

## BESCHREIBUNG
Ruft eine Zusammenfassungsansicht der neuesten Richtlinienkonformitätsstatusnummern in verschiedenen Bereichen ab, die in Richtlinienzuordnungen und Richtliniendefinitionen aufgeschlüsselt sind. Sie umfasst nur nicht kompatible Richtlinienzustände.

## BEISPIELE

### Beispiel 1: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände im aktuellen Abonnementbereich
```powershell
PS C:\> Get-AzPolicyStateSummary
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.

### Beispiel 2: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände im angegebenen Abonnementbereich
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.

### Beispiel 3: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände im Bereich der Verwaltungsgruppe
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Verwaltungsgruppe generiert wurden.

### Beispiel 4: Zusammenfassung der aktuellen nicht kompatiblen Richtlinienzustände im Ressourcengruppenbereich im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Abonnement im aktuellen Sitzungskontext) generiert wurden.

### Beispiel 5: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände im Ressourcengruppenbereich im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.

### Beispiel 6: Zusammenfassung der neuesten nicht kompatiblen Richtlinienzustände für eine Ressource
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für die angegebene Ressource generiert wurden.

### Beispiel 7: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtliniensatzdefinition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatzdefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 8: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtliniensatzdefinition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniensatzdefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 9: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtliniendefinition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 10: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtliniendefinition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 11: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtlinienzuordnung im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuordnung (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 12: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtlinienzuordnung im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuordnung (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 13: Aktuelle Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtlinienzuordnung in der angegebenen Ressourcengruppe im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtlinienzuordnung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 14: Holen Sie sich die neueste Zusammenfassung nicht kompatibler Richtlinienzustände im aktuellen Abonnementbereich mit der Option "Top query"
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden. Der Befehl ordnet die Richtlinienzuordnungszusammenfassungen in den Ergebnissen nach nicht kompatiblen Ressourcenanzahlen in absteigender Reihenfolge an und nimmt nur die obersten 5 dieser Richtlinienzuordnungszusammenfassungen an.

### Beispiel 15: Holen Sie sich die neueste Zusammenfassung nicht kompatibler Richtlinienzustände im aktuellen Abonnementbereich mit den Abfrageoptionen Von und An.
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die innerhalb des Datumsbereichs generiert werden, der für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext angegeben ist.

### Beispiel 16: Anzeigen der neuesten, nicht kompatiblen Richtlinienzustände im aktuellen Abonnementbereich mit Filterabfrageoption
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb des Abonnements im aktuellen Sitzungskontext generiert wurden.
Der Befehl schränkt die Ergebnisse ein, die durch Filtern basierend auf richtliniendefinitionsbezogenen Aktionen (einschließlich Deny- oder Überwachungsaktionen) und Ressourcenspeicherort (ohne Ostspeicherort) zurückgegeben werden.

## PARAMETER

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary

## NOTIZEN

## VERWANDTE LINKS

[Get-AzPolicyState](./Get-AzPolicyState.md)
