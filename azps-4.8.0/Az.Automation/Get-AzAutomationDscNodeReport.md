---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: 81a50a8c805d05b47b934b899eff708031ac6beb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165342"
---
# Get-AzAutomationDscNodeReport

## Synopsis
Ruft Berichte ab, die von einem DSC-Knoten an die Automatisierung gesendet werden.

## Syntax

### Seitensaller (Standard)
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByLatest
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzAutomationDscNodeReport** " ruft Berichte ab, die von einem APS-Knoten (Desired State Configuration, DSC) an Azure Automation gesendet werden.

## Beispiele

### Beispiel 1: Abrufen aller Berichte für einen DSC-Knoten
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

Der erste Befehl ruft den DSC-Knoten für den Computer mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.
Der Befehl speichert dieses Objekt in der $Node-Variablen.
Der zweite Befehl ruft Metadaten für alle Berichte ab, die vom DSC-Knoten mit dem Namen Computer14 an das Automatisierungs Konto mit dem Namen Contoso17 gesendet wurden.
Der Befehl gibt den Knoten mithilfe der **ID** -Eigenschaft des $Node-Objekts an.

### Beispiel 2: Abrufen eines Berichts für einen DSC-Knoten nach Berichts-ID
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Der erste Befehl ruft den DSC-Knoten für den Computer mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.
Der Befehl speichert dieses Objekt in der $Node-Variablen.
Der zweite Befehl ruft Metadaten für den Bericht ab, der durch die angegebene ID identifiziert wird, die vom DSC-Knoten mit dem Namen Computer14 an das Automatisierungs Konto mit dem Namen Contoso17 gesendet wurde.

### Beispiel 3: Abrufen des neuesten Berichts für einen DSC-Knoten
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

Der erste Befehl ruft den DSC-Knoten für den Computer mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.
Der Befehl speichert dieses Objekt in der $Node-Variablen.
Der zweite Befehl ruft Metadaten für den neuesten Bericht ab, der vom DSC-Knoten mit dem Namen Computer14 an das Automatisierungs Konto mit dem Namen Contoso17 gesendet wird.

## Parameter

### -AutomationAccountName
Gibt den Namen eines Automatisierungs Kontos an.
Dieses Cmdlet exportiert Berichte für einen DSC-Knoten, der zu dem Konto gehört, das dieser Parameter angibt.

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

### -EndTime
Gibt eine Endzeit an.
Dieses Cmdlet ruft Berichte ab, die von der Automatisierung vor diesem Zeitpunkt empfangen wurden.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Gibt die eindeutige ID des DSC-Knoten Berichts an, der für dieses Cmdlet abgerufen werden soll.

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Neueste
Gibt an, dass dieses Cmdlet nur den neuesten DSC-Bericht für den angegebenen Knoten abruft.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Knoten-Nr
Gibt die eindeutige ID des DSC-Knotens an, für den dieses Cmdlet Berichte abruft.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, die den DSC-Knoten enthält, für den dieses Cmdlet Berichte abruft.

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

### -Startzeit
Gibt eine Startzeit an.
Dieses Cmdlet ruft Berichte ab, die von der Automatisierung nach diesem Zeitpunkt empfangen wurden.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. GUID

### System. Nullable ' 1 [[System. DateTimeOffset, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. DscNode

## Notizen

## Verwandte Links

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Export-AzAutomationDscNodeReportContent](./Export-AzAutomationDscNodeReportContent.md)


