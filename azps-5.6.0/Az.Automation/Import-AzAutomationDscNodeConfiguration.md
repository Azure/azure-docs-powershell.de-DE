---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3680d277addba29444f3f2955d7cca28505435a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949635"
---
# Import-AzAutomationDscNodeConfiguration

## SYNOPSIS
Importiert ein MOF-Dokument als DSC-Knotenkonfiguration in automation.

## SYNTAX

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Import-AzAutomationDscConfiguration** importiert ein MoF-Konfigurationsdokument (Managed Object Format) als Dsc-Knotenkonfiguration (Desired State Configuration).
Geben Sie den Pfad einer MOF-Datei an.

## BEISPIELE

### Beispiel 1: Importieren einer KONFIGURATION eines DSC-Knotens in die Automatisierung
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

Mit diesem Befehl wird eine KONFIGURATION des DSC-Knotens aus der Datei "webserver.mof" in das Automatisierungskonto namens Contoso17 unter der DSC-Konfiguration ContosoConfiguration importiert.
Der Befehl gibt den Parameter *"Erzwingen"* an.
Wenn die Konfiguration eines DSC-Knotens mit dem Namen ContosoConfiguration.webserver vorhanden ist, ersetzt ihn dieser Befehl.

### Beispiel 2: Importieren Sie eine KONFIGURATION eines DSC-Knotens in die Automatisierung, erstellen Sie eine neue Buildversion, und überschreiben Sie die vorhandene NodeConfiguration nicht.
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

Mit diesem Befehl wird eine KONFIGURATION des DSC-Knotens aus der Datei "webserver.mof" in das Automatisierungskonto namens Contoso17 unter der DSC-Konfiguration ContosoConfiguration importiert.
Der Befehl gibt den Parameter *"Erzwingen"* an.
Wenn eine #A0 mit dem Namen ContosoConfiguration.webserver vorhanden ist, fügt dieser Befehl eine neue Buildversion mit dem Namen ContosoConfiguration[2].webserver hinzu.

## PARAMETER

### -AutomationAccountName
Gibt den Namen des Automatisierungskontos an, in das dieses Cmdlet eine DSC-Knotenkonfiguration importiert.

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
Gibt den Namen einer DSC-Konfiguration in automation an, die als Namespace und Container für die zu importierende Knotenkonfiguration verwendet werden soll.

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

### -Erzwingen
Gibt an, dass dieses Cmdlet eine vorhandene KONFIGURATION des DSC-Knotens in der Automatisierung ersetzt.

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
Erstellt eine neue Buildversion der Knotenkonfiguration.

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
Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet eine DSC-Knotenkonfiguration importiert.

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
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
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

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Automation.Model.NodeConfiguration

## NOTIZEN

## VERWANDTE LINKS

[Export-AzAutomationDscConfiguration](./Export-AzAutomationDscConfiguration.md)

[Get-AzAutomationDscConfiguration](./Get-AzAutomationDscConfiguration.md)


