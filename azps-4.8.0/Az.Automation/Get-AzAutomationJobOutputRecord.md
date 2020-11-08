---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008164"
---
# Get-AzAutomationJobOutputRecord

## Synopsis
Ruft die vollständige Ausgabe eines Automatisierungs Auftrags-Ausgabe Eintrags ab.

## Syntax

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzAutomationJobOutputRecord** " Ruft die vollständige Ausgabe eines Automatisierungs Auftrags-Ausgabe Eintrags ab.
Obwohl das Cmdlet " **Get-AzAutomationJobOutput** " einen oder mehrere Auftragsausgabe Datensätze aufführt, gibt es nur eine Zusammenfassung als Zeichenfolge des Werts eines beliebigen Ausgabedatensatzes zurück.
Er gibt nicht den vollständigen Wert des ausgegebenen Werts eines Ausgabedatensatzes in seinem ursprünglichen Typ zurück.
Darüber hinaus hat die Zusammenfassung eine maximale Länge, wobei der vollständige Wert, den dieses Cmdlet ausgibt, möglicherweise überschritten wird.

## Beispiele

### Beispiel 1: Abrufen der vollständigen Ausgabe eines Automatisierungs Auftrags
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

Dieser Befehl ruft die vollständige Ausgabe des Auftrags ab, die die angegebene Auftrags-ID aufweist.

## Parameter

### -AutomationAccountName
Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet einen Auftragsausgabe Daten Satz erhält.

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

### -ID
Gibt die ID eines Auftragsausgabe Datensatzes an, der für dieses Cmdlet abgerufen werden soll.

```yaml
Type: System.String
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
Type: System.Guid
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. GUID

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. JobStreamRecord

## Notizen

## Verwandte Links

[Get-AzAutomationJobOutput](./Get-AzAutomationJobOutput.md)


