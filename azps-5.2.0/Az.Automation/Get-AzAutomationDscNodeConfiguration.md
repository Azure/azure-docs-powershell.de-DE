---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 1114d0a78518c33126f28fb4b409a881a52a4ae7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370459"
---
# Get-AzAutomationDscNodeConfiguration

## SYNOPSIS
Ruft Metadaten für die Konfiguration von DSC-Knoten in der Automatisierung ab.

## SYNTAX

### ByAll (Standard)
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByNodeConfigurationName
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConfigurationName
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzAutomationDscNodeConfiguration"** ruft Metadaten für Die Konfiguration des Knotens "APS Desired State Configuration (DSC)" in der Azure Automation ab.
In der Automatisierung wird die KONFIGURATION von DSC-Knoten als Konfigurationsdokument für verwaltete Objektformate (Managed Object Format, MOF) gespeichert.

## BEISPIELE

### Beispiel 1: Alle KONFIGURATIONen des DSC-Knotens erhalten
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

Dieser Befehl ruft Metadaten für alle KONFIGURATIONen von DSC-Knoten im Automatisierungskonto namens "Contoso17" ab.

### Beispiel 2: Alle KONFIGURATIONen von DSC-Knoten für eine DSC-Konfiguration erhalten
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

Dieser Befehl ruft Metadaten für alle KONFIGURATIONen des DSC-Knotens im Automatisierungskonto namens "Contoso17" ab, das von der KONFIGURATION "ContosoConfiguration" generiert wurde.

### Beispiel 3: Erhalten einer KONFIGURATION eines DSC-Knotens nach Name
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

Dieser Befehl ruft Metadaten für eine Konfiguration eines DSC-Knotens mit dem Namen "ContosoConfiguration.webserver" im Automatisierungskonto namens "Contoso17" ab.

## PARAMETERS

### -AutomationAccountName
Gibt den Namen eines Automatisierungskontos an, das die DSC-Knotenkonfigurationen enthält, für die dieses Cmdlet Metadaten erhält.

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
Gibt den Namen der DSC-Konfiguration an, für die dieses Cmdlet Knotenkonfigurationsmetadaten erhält.

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
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

### -Name
Gibt den Namen der DSC-Knotenkonfiguration an, für die dieses Cmdlet Metadaten erhält.

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.
Dieses Cmdlet ruft Metadaten für DIE Konfiguration von DSC-Knoten in der Ressourcengruppe ab, die dieser Parameter angibt.

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

### -RollupStatus
Gibt den Rollupstatus von DSC-Knotenkonfigurationen an, die dieses Cmdlet erhält.
Gültige Werte sind: 
- Schlecht 
- Gut

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Automation.Model.CompilationJob

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Import-AzAutomationDscNodeConfiguration](./Import-AzAutomationDscNodeConfiguration.md)


