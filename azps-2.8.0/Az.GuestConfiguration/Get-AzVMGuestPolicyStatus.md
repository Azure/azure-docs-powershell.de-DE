---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: c1bf608c76c547360d9d7a48f4ba74c1713ee049
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651090"
---
# Get-AzVMGuestPolicyStatus

## Synopsis
Ruft den Status der gastkonfigurations Richtlinien (detailliert) für eine Initiative des Typs "Gast Konfiguration" ab, die einem virtuellen Computer zugewiesen ist.
Eine Initiative ist eine Richtlinie des Definitions Typs "Initiative".

## Syntax

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

## Beschreibung
Das Get-AzVMGuestPolicyStatus-Cmdlet ruft den Status der gastkonfigurations Richtlinie für eine Initiative des Typs "Gast Konfiguration" ab, die einem virtuellen Computer zugewiesen ist.
Eine Initiative ist eine Richtlinie des Definitions Typs "Initiative".
Dieses Cmdlet ruft den Konformitätsstatus der VM ab und begründet, warum Sie für die einzelnen Richtlinien in der Initiative nicht kompatibel ist.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Abrufen allerneuesten Einstellungen für die Gast Konfiguration für einen virtuellen Computer
Der Status umfasst den Kompatibilitätsstatus des virtuellen Computers für jede Richtlinie in allen Initiativen des Typs "Gast Konfiguration", Konformitäts Gründe, Zeitpunkt der Konformitätsprüfung, Ressourceninformationen, die auf die Compliance überprüft wurden.
Die Ergebnisse umfassen die neuesten Status, beinhalten keine vorherigen Verlaufsstatus.

### Beispiel 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Besorgen Sie sich die neuesten Einstellungen für Gast Konfigurationsrichtlinien nach initiativ-ID. Der Status umfasst den Kompatibilitätsstatus des virtuellen Computers für jede Richtlinie in der Initiative, Compliance-Gründen, Zeitpunkt der Konformitätsprüfung, Ressourceninformationen, die auf Compliance überprüft wurden.
Die Ergebnisse beinhalten keine generierten vorherigen Status, sondern enthalten nur den neuesten Status für jede Richtlinie in der Initiative.

### Beispiel 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Besorgen Sie sich die neuesten Einstellungen für Gast Konfigurationsrichtlinien nach initiativ Namen.
Der Status umfasst den Kompatibilitätsstatus des virtuellen Computers für jede Richtlinie in der Initiative, Compliance-Gründen, Zeitpunkt der Konformitätsprüfung, Ressourceninformationen, die auf Compliance überprüft wurden.
Die Ergebnisse beinhalten keine generierten vorherigen Status, sondern enthalten nur den neuesten Status für jede Richtlinie in der Initiative.

### Beispiel 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

Abrufen des Gast Konfigurationsrichtlinien Status nach Berichts-Nr.
Die Berichts-Nr ist die Eigenschaft "Reporter", die in den Ergebnissen von Get-AzVMGuestPolicyStatus nach initiativ-oder initiativ Name zu finden ist (Weitere Beispiele finden Sie hier)

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

Required: True
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

### -Berichts-Nr
Die ID eines Gast Konfigurationsrichtlinien Status.
Eine Richtlinie, bei der der Definitions Initiative und Kategorie ist, muss einem Bereich zugewiesen werden, um Status zu erhalten.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
## Ausgaben

### Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatusDetailed
## Notizen

## Verwandte Links
