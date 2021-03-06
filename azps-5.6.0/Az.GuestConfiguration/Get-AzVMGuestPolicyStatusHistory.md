---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 9161b3c9c55c1014b64419a3644bf7ec80af8648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938131"
---
# Get-AzVMGuestPolicyStatusHistory

## SYNOPSIS
Ruft den Compliancestatus der Gastkonfigurationsrichtlinie für eine Initiative vom Typ "Gastkonfiguration" ab, die einer VM zugewiesen ist.
Eine Initiative ist eine Richtlinie des Definitionstyps "Initiative".

## SYNTAX

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

## BESCHREIBUNG
Das Get-AzVMGuestPolicyStatusHistory-Cmdlet ruft den Compliancestatusverlauf von Gastkonfigurationsrichtlinien für eine Initiative vom Typ "Gastkonfiguration" ab, die einer VM zugewiesen ist.
Eine Initiative ist eine Richtlinie des Definitionstyps "Initiative".
Verwenden Get-AzVMGuestPolicyStatus cmdlet, um Details zu einem einzelnen Compliancestatus mithilfe von ReportId zu erhalten, die in der Ausgabe des cmdlets Get-AzVMGuestPolicyStatusHistory finden.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

Ruft den Compliancestatusverlauf nach Initiative-ID ab. Der ShowOnlyChange-Schalter zeigt nur historische Statusänderungen an.
Überspringt Status, die sich nicht zwischen zwei Complianceüberprüfungen geändert haben.

### Beispiel 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

Ruft den Compliancestatusverlauf nach Dem Namen der Initiative ab.
Der ShowOnlyChange-Schalter zeigt nur historische Statusänderungen an.
Überspringt Status, die sich nicht zwischen zwei Complianceüberprüfungen geändert haben.

### Beispiel 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

Ruft den Compliancestatusverlauf für alle der VM zugewiesenen Gastkonfigurationsrichtlinien ab.
Der ShowOnlyChange-Schalter zeigt nur historische Statusänderungen an.
Überspringt Status, die sich nicht zwischen zwei Complianceüberprüfungen geändert haben.

### Beispiel 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Ruft den Compliancestatusverlauf nach Initiative-ID ab.

### Beispiel 5
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Ruft den Compliancestatusverlauf nach Dem Namen der Initiative ab.

### Beispiel 6
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
Ruft den Compliancestatusverlauf für alle der VM zugewiesenen Gastkonfigurationsrichtlinien ab.

### Beispiel 7
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

Holen Sie sich den Status der Gastkonfigurationsrichtlinie nach ReportId.
Die ReportId ist die ReportId-Eigenschaft, die in den Ergebnissen von Get-AzVMGuestPolicyStatusHistory zu finden ist. (weitere Beispiele finden Sie hier.

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

### -InitiativeId
Definitions-ID einer Richtlinie, bei der der Definitionstyp "Initiative" und "Kategorie" "Gastkonfiguration" ist

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

### -InitiativeName
Name einer Richtlinie, deren Definitionstyp "Initiative" und "Kategorie" "Gastkonfiguration" ist

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
Zeigt Änderungen des verlaufshistorischen Status nur für Gastkonfigurationsrichtlinien an.
Überspringt Status, die sich nicht zwischen zwei Compliancestatusprüfungsläufen geändert haben.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine
## AUSGABEN

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus
## NOTIZEN

## VERWANDTE LINKS
