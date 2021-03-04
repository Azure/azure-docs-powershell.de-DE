---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: ceae5a9e7dec9913d90aae836784c6bfe66b680f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947616"
---
# Register-AzAutomationDscNode

## SYNOPSIS
Registriert einen virtuellen Azure-Computer mit Windows OS als DSC-Knoten für ein Automatisierungskonto.

## SYNTAX

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Register-AzAutomationDscNode** registriert einen virtuellen Azure-Computer als APS Desired State Configuration (DSC)-Knoten in einem Azure Automation-Konto. Dieses Cmdlet registriert nur VMs mit Windows OS als Automatisierungs-DSC-Knoten für ein Konto.

Wenn Sie einen Knoten bei einem Automatisierungskonto in einem anderen Abonnement registrieren müssen, müssen Sie anstelle von Cmdlets eine ARM verwenden. Weitere Details finden Sie in [der](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) Dokumentation zur Azure-Automatisierung.

## BEISPIELE

### Beispiel 1: Registrieren eines virtuellen Azure-Computers als Azure DSC-Knoten
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

Mit diesem Befehl wird der virtuelle Azure-Computer mit dem Namen VirtualMachine01 als DSC-Knoten im Automatisierungskonto namens Contoso17 registriert.

## PARAMETER

### -ActionAfterReboot
Gibt die Aktion an, die der virtuelle Computer nach dem Neustart ausgeführt hat.
Gültige Werte sind: 
- ContinueConfiguration 
- StopConfiguration

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AllowModuleOverwrite
Gibt an, ob neue Konfigurationen, die dieser DSC-Knoten vom Azure Automation DSC-Pullserver herunterlädet, die vorhandenen Module ersetzen, die sich bereits auf dem Zielknoten befinden.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutomationAccountName
Gibt den Namen eines Automatisierungskontos an, in dem dieses Cmdlet einen virtuellen Computer registriert.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMLocation
Der Azure VM-Speicherort.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMName
Der Name des virtuellen Azure-Computers, der für die Verwaltung bei Azure Automation DSC registriert werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMResourceGroup
Der Name der Azure VM-Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationMode
Gibt den DSC-Konfigurationsmodus an.
Gültige Werte sind: 
- ApplyAndMonitor 
- ApplyAndAutocorrect 
- ApplyOnly

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationModeFrequencyMins
Gibt die Häufigkeit in Minuten an, mit der die Hintergrundanwendung von DSC versucht, die aktuelle Konfiguration auf dem Zielknoten zu implementieren.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -NodeConfigurationName
Gibt den Namen der Knotenkonfiguration an, die von diesem Cmdlet so konfiguriert wird, dass der virtuelle Computer von Azure Automation DSC abgerufen wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RebootNodeIfNeeded
Gibt an, ob der virtuelle Computer bei Bedarf neu gestartet werden soll.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RefreshFrequencyMins
Gibt die Häufigkeit in Minuten an, mit der sich der lokale Configuration Manager an den Azure Automation DSC-Pullserver wendet, um die neueste Knotenkonfiguration herunterzuladen.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.
Das Automatisierungskonto, mit dem dieses Cmdlet einen virtuellen Computer registriert, gehört zu der Ressourcengruppe, die dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### System.Int32

### System.Boolean

## AUSGABEN

### System.Void

## NOTIZEN

## VERWANDTE LINKS

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Set-AzAutomationDscNode](./Set-AzAutomationDscNode.md)

[Aufheben der Registrierung-AzAutomationDscNode](./Unregister-AzAutomationDscNode.md)


