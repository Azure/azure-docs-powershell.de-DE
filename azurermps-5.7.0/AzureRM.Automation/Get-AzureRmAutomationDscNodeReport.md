---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: f71aef989a26ec5998ee8fd059446a2b05c2e4b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665319"
---
# Get-AzureRmAutomationDscNodeReport

## Synopsis
Ruft Berichte ab, die von einem DSC-Knoten an die Automatisierung gesendet werden.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Seitensaller (Standard)
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByLatest
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmAutomationDscNodeReport** " ruft Berichte ab, die von einem APS-Knoten (Desired State Configuration, DSC) an Azure Automation gesendet werden.

## Beispiele

### Beispiel 1: Abrufen aller Berichte für einen DSC-Knoten
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

Der erste Befehl ruft den DSC-Knoten für den Computer mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.
Der Befehl speichert dieses Objekt in der $Node-Variablen.

Der zweite Befehl ruft Metadaten für alle Berichte ab, die vom DSC-Knoten mit dem Namen Computer14 an das Automatisierungs Konto mit dem Namen Contoso17 gesendet wurden.
Der Befehl gibt den Knoten mithilfe der **ID** -Eigenschaft des $Node-Objekts an.

### Beispiel 2: Abrufen eines Berichts für einen DSC-Knoten nach Berichts-ID
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Der erste Befehl ruft den DSC-Knoten für den Computer mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.
Der Befehl speichert dieses Objekt in der $Node-Variablen.

Der zweite Befehl ruft Metadaten für den Bericht ab, der durch die angegebene ID identifiziert wird, die vom DSC-Knoten mit dem Namen Computer14 an das Automatisierungs Konto mit dem Namen Contoso17 gesendet wurde.

### Beispiel 3: Abrufen des neuesten Berichts für einen DSC-Knoten
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

Der erste Befehl ruft den DSC-Knoten für den Computer mit dem Namen Computer14 im Automatisierungs Konto mit dem Namen Contoso17 ab.
Der Befehl speichert dieses Objekt in der $Node-Variablen.

Der zweite Befehl ruft Metadaten für den neuesten Bericht ab, der vom DSC-Knoten mit dem Namen Computer14 an das Automatisierungs Konto mit dem Namen Contoso17 gesendet wird.

## Parameter

### -AutomationAccountName
Gibt den Namen eines Automatisierungs Kontos an.
Dieses Cmdlet exportiert Berichte für einen DSC-Knoten, der zu dem Konto gehört, das dieser Parameter angibt.

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

### -EndTime
Gibt eine Endzeit an.
Dieses Cmdlet ruft Berichte ab, die von der Automatisierung vor diesem Zeitpunkt empfangen wurden.

```yaml
Type: DateTimeOffset
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
Type: Guid
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
Type: SwitchParameter
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
Type: Guid
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
Type: String
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
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
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

### Microsoft. Azure. Commands. Automation. Model. DscNode

## Notizen

## Verwandte Links

[Get-AzureRmAutomationDscNode](./Get-AzureRmAutomationDscNode.md)

[Export-AzureRmAutomationDscNodeReportContent](./Export-AzureRmAutomationDscNodeReportContent.md)


