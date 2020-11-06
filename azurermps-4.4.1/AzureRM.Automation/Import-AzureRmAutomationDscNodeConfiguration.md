---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 9c3fd17454381cf17604eb430588255b4889b3cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497969"
---
# Import-AzureRmAutomationDscNodeConfiguration

## Synopsis
Importiert ein MOF-Dokument als DSC-Knoten Konfiguration in der Automatisierung.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Import-AzureRmAutomationDscConfiguration** " wird ein MOF-Konfigurationsdokument (Managed Object Format) in die Azure-Automatisierung als Konfiguration für eine gewünschte Statuskonfiguration (DSC) importiert.
Geben Sie den Pfad einer MOF-Datei an.

## Beispiele

### Beispiel 1: Importieren einer DSC-Knoten Konfiguration in die Automatisierung
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

Dieser Befehl importiert eine DSC-Knoten Konfiguration aus der Datei "Webserver. mof" in das Automatisierungs Konto mit dem Namen Contoso17 unter dem DSC-Konfigurations ContosoConfiguration.
Der Befehl gibt den Parameter *Force* an.
Wenn eine vorhandene DSC-Knoten Konfiguration mit dem Namen ContosoConfiguration. Webserver vorhanden ist, wird Sie durch diesen Befehl ersetzt.

### Beispiel 2: Importieren Sie eine DSC-Knoten Konfiguration in die Automatisierung, und erstellen Sie eine neue Buildversion, und überschreiben Sie keine vorhandenen NodeConfiguration.
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

Dieser Befehl importiert eine DSC-Knoten Konfiguration aus der Datei "Webserver. mof" in das Automatisierungs Konto mit dem Namen Contoso17 unter dem DSC-Konfigurations ContosoConfiguration.
Der Befehl gibt den Parameter *Force* an.
Wenn eine vorhandene DSC-Knoten Konfiguration mit dem Namen ContosoConfiguration. Webserver vorhanden ist, wird mit diesem Befehl eine neue Buildversion mit dem Namen ContosoConfiguration [2]. Webserver hinzugefügt.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos an, in das dieses Cmdlet eine DSC-Knoten Konfiguration importiert.

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

### -ConfigurationName
Gibt den Namen einer DSC-Konfiguration in Automatisierung an, die als Namespace und Container für die zu importierende Knoten Konfiguration verwendet werden soll.

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

### -Force
Gibt an, dass dieses Cmdlet eine vorhandene DSC-Knoten Konfiguration in der Automatisierung ersetzt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncrementNodeConfigurationBuild
Erstellt eine neue Buildversion für die Knoten Konfiguration.

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

### -Path
Gibt den Pfad des MOF-Konfigurationsdokuments an, das von diesem Cmdlet importiert wird.

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

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet eine DSC-Knoten Konfiguration importiert.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. NodeConfiguration

## Notizen

## Verwandte Links

[Export-AzureRmAutomationDscConfiguration](./Export-AzureRmAutomationDscConfiguration.md)

[Get-AzureRmAutomationDscConfiguration](./Get-AzureRmAutomationDscConfiguration.md)


