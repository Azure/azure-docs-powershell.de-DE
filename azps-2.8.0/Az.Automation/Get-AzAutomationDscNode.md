---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
ms.openlocfilehash: 9d4efbccffeae2654b5be6d6db8635e588fd87f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658067"
---
# Get-AzAutomationDscNode

## Synopsis
Ruft DSC-Knoten aus der Automatisierung ab.

## Syntax

### Seitensaller (Standard)
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

## Beschreibung
Das Cmdlet " **Get-AzAutomationDscNode** " ruft APS-Knoten (Desired State Configuration, DSC) aus Azure Automation ab.

## Beispiele

### Beispiel 1: Abrufen aller DSC-Knoten
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

Dieser Befehl ruft Metadaten für alle DSC-Knoten im Automatisierungs Konto mit dem Namen Contoso17 ab.

### Beispiel 2: Abrufen aller DSC-Knoten für eine DSC-Konfiguration
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

Dieser Befehl ruft Metadaten für alle DSC-Knoten im Automatisierungs Konto mit dem Namen Contoso17 ab, die einer DSC-Knoten Konfiguration zugeordnet sind, die durch DSC-Konfigurations ContosoConfiguration generiert wurde.

### Beispiel 3: Abrufen eines DSC-Knotens anhand der ID
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Dieser Befehl ruft Metadaten auf einem DSC-Knoten mit der angegebenen ID im Automatisierungs Konto mit dem Namen Contoso17 ab.

### Beispiel 4: Abrufen eines DSC-Knotens anhand des Namens
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

Dieser Befehl ruft Metadaten auf einem DSC-Knoten mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.

### Beispiel 5: Abrufen aller DSC-Knoten, die einer DSC-Knoten Konfiguration zugeordnet sind
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

Dieser Befehl ruft Metadaten für alle DSC-Knoten im Automatisierungs Konto mit dem Namen Contoso17 ab, die einer DSC-Knoten Konfiguration mit dem Namen ContosoConfiguration. Webserver zugeordnet sind.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos an, das die DSC-Knoten enthält, die dieses Cmdlet erhält.

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
Dieses Cmdlet ruft DSC-Knoten ab, die den Knoten Konfigurationen entsprechen, die aus der von diesem Parameter festgelegten Konfiguration generiert wurden.

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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
Gibt den Namen einer Knoten Konfiguration an, die dieses Cmdlet erhält.

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
Gibt den Status der DSC-Knoten an, die dieses Cmdlet erhält.
Gültige Werte sind: 
- Kompatibel 
- NotCompliant
- Fehlgeschlagen
- Ausstehend 
- Empfangen
- Reagiert

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. GUID

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. DscNode

## Notizen

## Verwandte Links

[Registrieren-AzAutomationDscNode](./Register-AzAutomationDscNode.md)

[Satz-AzAutomationDscNode](./Set-AzAutomationDscNode.md)

[Registrierung aufheben-AzAutomationDscNode](./Unregister-AzAutomationDscNode.md)


