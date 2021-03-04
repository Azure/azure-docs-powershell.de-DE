---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
ms.openlocfilehash: 790c280d139f2770f08d5ecfed64acf42d0fc1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938336"
---
# Get-AzAutomationDscNode

## SYNOPSIS
Ruft DSC-Knoten aus der Automatisierung ab.

## SYNTAX

### ByAll (Standard)
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByNodeConfiguration
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConfiguration
```
Get-AzAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzAutomationDscNode-Cmdlet** ruft APS Desired State Configuration (DSC)-Knoten aus Azure Automation ab.

## BEISPIELE

### Beispiel 1: Alle DSC-Knoten erhalten
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

Dieser Befehl ruft Metadaten für alle DSC-Knoten im Automatisierungskonto namens Contoso17 ab.

### Beispiel 2: Alle DSC-Knoten für eine DSC-Konfiguration erhalten
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

Dieser Befehl ruft Metadaten für alle DSC-Knoten im Automatisierungskonto namens Contoso17 ab, die einer DSC-Knotenkonfiguration zugeordnet sind, die von der DSC-Konfiguration ContosoConfiguration generiert wurde.

### Beispiel 3: Erhalten eines DSC-Knotens nach ID
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Dieser Befehl ruft Metadaten für einen DSC-Knoten mit der angegebenen ID im Automatisierungskonto namens Contoso17 ab.

### Beispiel 4: Benennen eines DSC-Knotens
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

Dieser Befehl ruft Metadaten für einen DSC-Knoten mit dem Namen Computer14 im Automatisierungskonto namens Contoso17 ab.

### Beispiel 5: Erhalten aller DSC-Knoten, die einer KONFIGURATION eines DSC-Knotens zugeordnet sind
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

Dieser Befehl ruft Metadaten für alle DSC-Knoten im Automatisierungskonto namens Contoso17 ab, die einer KONFIGURATION des DSC-Knotens namens ContosoConfiguration.webserver zugeordnet sind.

## PARAMETER

### -AutomationAccountName
Gibt den Namen des Automatisierungskontos an, das die vom Cmdlet abgerufenen DSC-Knoten enthält.

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
Gibt den Namen einer DSC-Konfiguration an.
Dieses Cmdlet ruft DSC-Knoten ab, die den Knotenkonfigurationen entsprechen, die aus der von diesem Parameter angegebenen Konfiguration generiert werden.

```yaml
Type: System.String
Parameter Sets: ByConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -ID
Gibt die eindeutige ID des DSC-Knotens an, den dieses Cmdlet erhält.

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen eines DSC-Knotens an, den dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeConfigurationName
Gibt den Namen einer Knotenkonfiguration an, die dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: ByNodeConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet DSC-Knoten erhält.

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

### -Status
Gibt den Status der DSC-Knoten an, die von diesem Cmdlet abgerufen werden.
Gültige Werte sind: 
- Kompatibel 
- NotCompliant
- Fehlgeschlagen
- Ausstehend 
- Empfangen
- Nicht reagieren

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases:
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.Guid

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Automation.Model.Dscnode

## NOTIZEN

## VERWANDTE LINKS

[Register-AzAutomationDscNode](./Register-AzAutomationDscNode.md)

[Set-AzAutomationDscNode](./Set-AzAutomationDscNode.md)

[Aufheben der Registrierung-AzAutomationDscNode](./Unregister-AzAutomationDscNode.md)


