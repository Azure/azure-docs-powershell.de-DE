---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b012704eebfa9d2c2a868679450cd0231667f585
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665343"
---
# Start-AzureRmStreamAnalyticsJob

## Synopsis
Startet einen Datenstrom Analyse Auftrag.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Start-AzureRmStreamAnalyticsJob** " wird ein Datenstrom Analyse Auftrag in Azure asynchron bereitgestellt und gestartet.

## Beispiele

### Beispiel 1: Starten eines Datenstrom Analyse Auftrags
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

Dieser Befehl startet den Job-StreamingJob und gibt an, dass der ausgabeereignis Datenstrom bei Timestamp 2014-07-03T01:00Z beginnen soll.

## Parameter

### -Name
Gibt den Namen des zu startenden Azure Stream Analytics-Auftrags an.

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

### -OutputStartMode
Gibt den Startmodus für den Auftrag an.
Gültige Werte sind: 

- JobStartTime – dieser Wert gibt an, dass der Ausgangspunkt des ausgabeereignis Datenstroms beginnen soll, wenn der Auftrag gestartet wird.
- Benutzerdefiniertes Zeit-dieser Wert gibt an, dass der Ausgangspunkt des ausgabeereignis Datenstroms zu einem im *OutputStartTime* -Parameter angegebenen benutzerdefinierten Zeitpunkt beginnen soll. 
 --LastOutputEventTime – dieser Wert gibt an, dass der Ausgangspunkt des ausgabeereignis Datenstroms ab dem letzten Ereignisausgabe Zeitpunkt beginnen soll.

Wenn die Eigenschaft nicht vorhanden ist, lautet der Standardwert JobStartTime.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputStartTime
Gibt die Startzeit der Ausgabe an.
Dieser Wert ist entweder ein ISO-8601-formatierter Zeitstempel, der den Anfangspunkt des ausgabeereignis Datenstroms angibt, oder $NULL, um anzugeben, dass der ausgabeereignis Datenstrom beim Starten des Streaming-Auftrags gestartet wird.
Diese Eigenschaft muss einen Wert haben, wenn *OutputStartMode* auf "Benutzerdefiniert" eingestellt ist.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehört.

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

### System. Object

## Notizen

## Verwandte Links

[Get-AzureRmStreamAnalyticsJob](./Get-AzureRmStreamAnalyticsJob.md)

[Neu – AzureRmStreamAnalyticsJob](./New-AzureRmStreamAnalyticsJob.md)

[Remove-AzureRmStreamAnalyticsJob](./Remove-AzureRmStreamAnalyticsJob.md)

[Stopp-AzureRmStreamAnalyticsJob](./Stop-AzureRmStreamAnalyticsJob.md)


