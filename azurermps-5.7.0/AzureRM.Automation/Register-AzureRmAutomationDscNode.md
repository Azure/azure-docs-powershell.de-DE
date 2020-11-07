---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
ms.openlocfilehash: 614e954f4e8ec37d24495e766a139eb8a961c743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664936"
---
# Register-AzureRmAutomationDscNode

## Synopsis
Registriert einen virtuellen Azure-Computer als DSC-Knoten für ein Automatisierungs Konto.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Register-AzureRmAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Register-AzureRmAutomationDscNode** " wird ein Azure Virtual Machine als APS-Knoten (Desired State Configuration, DSC) in einem Azure Automation-Konto registriert.

## Beispiele

### Beispiel 1: Registrieren eines Azure Virtual Machine als Azure DSC-Knoten
```
PS C:\>Register-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

Dieser Befehl registriert den Azure Virtual Machine mit dem Namen VirtualMachine01 als DSC-Knoten im Automatisierungs Konto mit dem Namen Contoso17.

## Parameter

### -ActionAfterReboot
Gibt die Aktion an, die der virtuelle Computer ausführt, nachdem er neu gestartet wurde.
Gültige Werte sind: 

- ContinueConfiguration 
- StopConfiguration

```yaml
Type: String
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
Gibt an, ob neue Konfigurationen, die dieser DSC-Knoten vom Azure Automation DSC-Pull-Server herunterlädt, die vorhandenen Module ersetzen, die bereits auf dem Zielknoten vorhanden sind.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutomationAccountName
Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet einen virtuellen Computer registriert.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMLocation
Gibt den Speicherort an, an dem dieses Cmdlet einen virtuellen Computer registriert.
Verwenden Sie das Get-AzureRMLocation-Cmdlet, um gültige Speicherorte zu erhalten.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMName
Gibt den Namen des Azure Virtual Machine an, den dieses Cmdlet für die Verwaltung registriert.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMResourceGroup
Gibt den Namen der Ressourcengruppe des Azure Virtual Machine an, die dieses Cmdlet registriert.

```yaml
Type: String
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
Type: String
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
Gibt die Häufigkeit in Minuten an, bei der die Hintergrundanwendung von DSC versucht, die aktuelle Konfiguration auf dem Zielknoten zu implementieren.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeConfigurationName
Gibt den Namen der Knoten Konfiguration an, die von diesem Cmdlet für den virtuellen Computer konfiguriert wird, um von Azure Automation DSC zu ziehen.

```yaml
Type: String
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
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RefreshFrequencyMins
Gibt die Häufigkeit in Minuten an, mit der der lokale Konfigurations-Manager den Azure Automation DSC-Pull-Server kontaktiert, um die neueste Knoten Konfiguration herunterzuladen.

```yaml
Type: Int32
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
Das Automatisierungs Konto, mit dem dieses Cmdlet einen virtuellen Computer registriert, gehört zur Ressourcengruppe, die dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmAutomationDscNode](./Get-AzureRmAutomationDscNode.md)

[Satz-AzureRmAutomationDscNode](./Set-AzureRmAutomationDscNode.md)

[Registrierung aufheben-AzureRmAutomationDscNode](./Unregister-AzureRmAutomationDscNode.md)


