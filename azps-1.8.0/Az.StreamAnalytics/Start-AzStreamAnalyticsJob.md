---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: bdbd590f2c6c158759d439e473274c8b4508863d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658643"
---
# Start-AzStreamAnalyticsJob

## Synopsis
Startet einen Datenstrom Analyse Auftrag.

## Syntax

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Start-AzStreamAnalyticsJob** " wird ein Datenstrom Analyse Auftrag in Azure asynchron bereitgestellt und gestartet.

## Beispiele

### Beispiel 1: Starten eines Datenstrom Analyse Auftrags
```
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

Dieser Befehl startet den Job-StreamingJob und gibt an, dass der ausgabeereignis Datenstrom bei Timestamp 2014-07-03T01:00Z beginnen soll.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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
 - LastOutputEventTime – dieser Wert gibt an, dass der Ausgangspunkt des ausgabeereignis Datenstroms ab dem letzten Ereignisausgabe Zeitpunkt beginnen soll.
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links

[Get-AzStreamAnalyticsJob](./Get-AzStreamAnalyticsJob.md)

[Neu – AzStreamAnalyticsJob](./New-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[Stopp-AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)


