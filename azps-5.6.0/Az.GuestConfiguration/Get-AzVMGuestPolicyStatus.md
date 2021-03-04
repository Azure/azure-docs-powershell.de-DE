---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 3edb92ae8c46ab67e0e22ee808e38dad7101bfdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938136"
---
# Get-AzVMGuestPolicyStatus

## SYNOPSIS
Ruft gastkonfigurationsrichtlinienstatus (detailliert) für eine Initiative vom Typ "Gastkonfiguration" ab, die einer VM zugewiesen ist.
Eine Initiative ist eine Richtlinie des Definitionstyps "Initiative".

## SYNTAX

### VmScope (Standard)
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeNameScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ReportIdScope
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das Get-AzVMGuestPolicyStatus-Cmdlet ruft Gastkonfigurationsrichtlinienstatus für eine Initiative vom Typ "Gastkonfiguration" ab, die einer VM zugewiesen ist.
Eine Initiative ist eine Richtlinie des Definitionstyps "Initiative".
Dieses Cmdlet erhält den Compliancestatus der VM und die Gründe, warum es für die einzelnen Richtlinien in der Initiative nicht kompatibel ist.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Erhalten Sie alle aktuellen Status der Gastkonfigurationsrichtlinien für eine VM.
Der Status umfasst den Compliancestatus der VM für jede Richtlinie in allen Initiativen vom Typ "Gastkonfiguration", Compliancegründe, Uhrzeit der Complianceüberprüfung, Ressourceninformationen, die auf Compliance überprüft wurden.
Die Ergebnisse enthalten die neuesten Status und keine vorherigen historischen Status.

### Beispiel 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Holen Sie sich die neuesten Status der Gastkonfigurationsrichtlinien nach Initiative-ID. Der Status umfasst den Compliancestatus der VM für jede Richtlinie in der Initiative, Compliancegründe, Uhrzeit der Complianceüberprüfung, Ressourceninformationen, die auf Compliance überprüft wurden.
Die Ergebnisse enthalten keine zuvor generierten Status, sondern nur den neuesten Status für jede Richtlinie in der Initiative.

### Beispiel 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Holen Sie sich die neuesten Status der Gastkonfigurationsrichtlinien nach Dem Namen der Initiative.
Der Status umfasst den Compliancestatus der VM für jede Richtlinie in der Initiative, Compliancegründe, Uhrzeit der Complianceüberprüfung, Ressourceninformationen, die auf Compliance überprüft wurden.
Die Ergebnisse enthalten keine zuvor generierten Status, sondern nur den neuesten Status für jede Richtlinie in der Initiative.

### Beispiel 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

Holen Sie sich den Status der Gastkonfigurationsrichtlinie nach ReportId.
Die ReportId ist die ReportId-Eigenschaft, die in den Ergebnissen von Get-AzVMGuestPolicyStatus von initiativeId oder Initiative name zu finden ist (weitere Beispiele finden Sie hier).

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

Required: True
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

### -ReportId
Id eines Richtlinienstatus der Gastkonfiguration.
Eine Richtlinie, bei der der Definitionstyp "Initiative" und die Kategorie "Gastkonfiguration" ist, muss einem Bereich zugewiesen werden, um Status zu erhalten.

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
VM-Name.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
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

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed
## NOTIZEN

## VERWANDTE LINKS
