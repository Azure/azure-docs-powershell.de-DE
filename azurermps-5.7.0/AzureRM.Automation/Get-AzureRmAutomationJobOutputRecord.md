---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
ms.openlocfilehash: 18551d6d839991cf0eb9e020c62fa0a24207d1e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497766"
---
# Get-AzureRmAutomationJobOutputRecord

## Synopsis
Ruft die vollständige Ausgabe eines Automatisierungs Auftrags-Ausgabe Eintrags ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmAutomationJobOutputRecord** " Ruft die vollständige Ausgabe eines Automatisierungs Auftrags-Ausgabe Eintrags ab.

Obwohl das Cmdlet " **Get-AzureRmAutomationJobOutput** " einen oder mehrere Auftragsausgabe Datensätze aufführt, gibt es nur eine Zusammenfassung als Zeichenfolge des Werts eines beliebigen Ausgabedatensatzes zurück.
Er gibt nicht den vollständigen Wert des ausgegebenen Werts eines Ausgabedatensatzes in seinem ursprünglichen Typ zurück.
Darüber hinaus hat die Zusammenfassung eine maximale Länge, wobei der vollständige Wert, den dieses Cmdlet ausgibt, möglicherweise überschritten wird.
Im Gegensatz zu " **Get-AzureRmAutomationJobOutput** " gibt dieses Cmdlet den vollständigen Wert in seinem ursprünglich ausgegebenen Typ für den ausgegebenen Wert eines Ausgabedatensatzes zurück.

## Beispiele

### Beispiel 1: Abrufen der vollständigen Ausgabe eines Automatisierungs Auftrags
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzureRmAutomationJobOutputRecord
```

Dieser Befehl ruft die vollständige Ausgabe des Auftrags ab, die die angegebene Auftrags-ID aufweist.

## Parameter

### -AutomationAccountName
Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet einen Auftragsausgabe Daten Satz erhält.

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

### -ID
Gibt die ID eines Auftragsausgabe Datensatzes an, der für dieses Cmdlet abgerufen werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobId
Gibt die ID eines Auftrags an, für den dieses Cmdlet einen Ausgabe Eintrag erhält.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Auftragsausgabe Daten Satz erhält.

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

### Microsoft. Azure. Commands. Automation. Model. JobStreamRecord

## Notizen

## Verwandte Links

[Get-AzureRmAutomationJobOutput](./Get-AzureRMAutomationJobOutput.md)


