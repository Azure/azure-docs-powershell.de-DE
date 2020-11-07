---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 2e2474b784d66c3c3c34bc9ea9abc2b0959ea500
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819983"
---
# Get-AzVMGuestPolicyStatusHistory

## Synopsis
Ruft den Kompatibilitätsstatus des Gast Konfigurationsrichtlinien für eine Initiative des Typs "Gast Konfiguration" ab, die einem virtuellen Computer zugewiesen ist.
Eine Initiative ist eine Richtlinie des Definitions Typs "Initiative".

## Syntax

### InitiativeNameScope (Standard)
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Get-AzVMGuestPolicyStatusHistory-Cmdlet ruft den Kompatibilitätsstatus Verlauf von Gast Konfigurationsrichtlinien für eine Initiative des Typs "Gast Konfiguration" ab, die einem virtuellen Computer zugewiesen ist.
Eine Initiative ist eine Richtlinie des Definitions Typs "Initiative".
Verwenden Sie Get-AzVMGuestPolicyStatus-Cmdlet, um Details zu einem einzelnen Kompatibilitätsstatus mithilfe der Berichts-Nr abzurufen, die in der Ausgabe des Get-AzVMGuestPolicyStatusHistory-Cmdlets zu finden ist.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

Ruft den Konformitätsstatus Verlauf nach initiativ-ID ab. ShowOnlyChange-Schalter zeigt nur Verlaufsstatus Änderungen an.
Überspringt Status, die sich zwischen zwei Kompatibilitätsprüfungen nicht geändert haben.

### Beispiel 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

Ruft den Konformitätsstatus Verlauf nach initiativ Name ab.
ShowOnlyChange-Schalter zeigt nur Änderungen des Verlaufsstatus an.
Überspringt Status, die sich zwischen zwei Kompatibilitätsprüfungen nicht geändert haben.

### Beispiel 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

Ruft den Kompatibilitätsstatus Verlauf für alle Guest-Konfigurationsrichtlinien ab, die dem virtuellen Computer zugewiesen sind.
ShowOnlyChange-Schalter zeigt nur Änderungen des Verlaufsstatus an.
Überspringt Status, die sich zwischen zwei Kompatibilitätsprüfungen nicht geändert haben.

### Beispiel 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Ruft den Konformitätsstatus Verlauf nach initiativ-ID ab.

### Beispiel 5
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Ruft den Konformitätsstatus Verlauf nach initiativ Name ab.

### Beispiel 6
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
Ruft den Kompatibilitätsstatus Verlauf für alle Guest-Konfigurationsrichtlinien ab, die dem virtuellen Computer zugewiesen sind.

### Beispiel 7
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

Abrufen des Gast Konfigurationsrichtlinien Status nach Berichts-Nr.
Die Berichts-Nr ist die Eigenschaft "Reporter", die in den Ergebnissen von Get-AzVMGuestPolicyStatusHistory zu finden ist. (Weitere Beispiele finden Sie hier)

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

### -Initiativ-Nr.
Definitions-ID einer Richtlinie, bei der der Definitions Initiative und Kategorie ist Gast Konfiguration ist

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Initiativname
Name einer Richtlinie, bei der der Definitions "Initiative" und "Kategorie" Gast Konfiguration ist

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowOnlyChange
Zeigt Änderungen des Verlaufsstatus nur für Gast Konfigurationsrichtlinien an.
Überspringt Status, die sich zwischen zwei Kompatibilitätsstatus-Überwachungs Läufen nicht geändert haben.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
VM-Name.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
## Ausgaben

### Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatus
## Notizen

## Verwandte Links
