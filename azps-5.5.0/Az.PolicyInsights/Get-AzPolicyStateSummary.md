---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172260"
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
Ruft eine Zusammenfassungsansicht der neuesten Nummern von Richtlinienkonformitätsstatus in verschiedenen Bereichen ab, aufgeschlüsselt in Richtlinienzuweisungen und Richtliniendefinitionen. Sie umfasst nur nicht kompatible Richtlinienzustände.

## BEISPIELE

### Beispiel 1: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände im aktuellen Abonnementbereich
```powershell
PS C:\> Get-AzPolicyStateSummary
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.

### Beispiel 2: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände im angegebenen Abonnementbereich
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb des angegebenen Abonnements generiert wurden.

### Beispiel 3: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände im Bereich der Verwaltungsgruppe
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen in der angegebenen Verwaltungsgruppe generiert wurden.

### Beispiel 4: Erhalten der aktuellen Zusammenfassung der nicht kompatiblen Richtlinienzustände im Bereich "Ressourcengruppe" im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im Abonnement im aktuellen Sitzungskontext) generiert wurden.

### Beispiel 5: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände im Ressourcengruppenbereich im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen innerhalb der angegebenen Ressourcengruppe (im angegebenen Abonnement) generiert wurden.

### Beispiel 6: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände für eine Ressource
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für die angegebene Ressource generiert wurden.

### Beispiel 7: Erhalten der neuesten Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtliniensatzdefinition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatzdefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 8: Erhalten der neuesten Zusammenfassung nicht kompatibler Richtlinienzustände für eine Richtliniensatzdefinition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtliniensatzdefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 9: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände für eine Richtliniendefinition im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 10: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände für eine Richtliniendefinition im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die durch die angegebene Richtliniendefinition (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 11: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände für eine Richtlinienzuweisung im aktuellen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 12: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände für eine Richtlinienzuweisung im angegebenen Abonnement
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die im angegebenen Abonnement vorhanden ist) ausgeführt werden.

### Beispiel 13: Aktuelle Zusammenfassung der nicht kompatiblen Richtlinienzustände für eine Richtlinienzuweisung in der angegebenen Ressourcengruppe im aktuellen Abonnement erhalten
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen (innerhalb des Mandanten im aktuellen Sitzungskontext) generiert wurden, die von der angegebenen Richtlinienzuweisung (die in der Ressourcengruppe im Abonnement im aktuellen Sitzungskontext vorhanden ist) ausgeführt werden.

### Beispiel 14: Holen Sie sich die neueste Zusammenfassung der nicht kompatiblen Richtlinienzustände im aktuellen Abonnementbereich mit der Option "Spitzenabfrage".
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden. Der Befehl ordnet die Richtlinienzuweisung in den Ergebnissen nach nicht kompatibler Ressourcenanzahl in absteigender Reihenfolge und nimmt nur die Obersten 5 dieser Zusammenfassungen für Richtlinienzuweisungen an.

### Beispiel 15: Erhalten der neuesten Zusammenfassung der nicht kompatiblen Richtlinienzustände im aktuellen Abonnementbereich mit den Optionen "Von" und "Bis"
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die innerhalb des datumsbezogenen Bereichs generiert werden, der für alle Ressourcen im Abonnement im aktuellen Sitzungskontext angegeben ist.

### Beispiel 16: Holen Sie sich die neueste Zusammenfassung der nicht kompatiblen Richtlinienzustände im aktuellen Abonnementbereich mit der Option "Filterabfrage".
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Ruft die Zusammenfassungsansicht der neuesten Richtlinienkonformitätszustände ab, die am letzten Tag für alle Ressourcen im Abonnement im aktuellen Sitzungskontext generiert wurden.
Der Befehl beschränkt die von der Filterung zurückgegebenen Ergebnisse basierend auf einer Richtliniendefinitionsaktion (einschließlich Verweigern- oder Überwachungsaktionen) und dem Ressourcenspeicherort (schließt den Oststandort aus).

## PARAMETERS

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzPolicyState](./Get-AzPolicyState.md)
