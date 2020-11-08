---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006516"
---
# Get-AzureSchedulerJobHistory

## Synopsis
Ruft den Verlauf eines Scheduler-Auftrags ab.

## Syntax

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das Cmdlet " **Get-AzureSchedulerJobHistory** " Ruft das Protokoll für einen Scheduler-Auftrag ab.

## Beispiele

### Beispiel 1: Abrufen des Verlaufs für einen Auftrag mithilfe des Namens
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

Mit diesem Befehl wird der Verlauf des Auftrags mit dem Namen Job01 abgerufen.
Dieser Auftrag gehört zur Auftrags Sammlung mit dem Namen JobCollection01 an der angegebenen Position.

### Beispiel 2: Abrufen des Verlaufs für einen fehlerhaften Auftrag mithilfe des Namens
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

Dieser Befehl ruft den Verlauf des Auftrags mit dem Namen Job12 ab, der den Status Fehler aufweist.
Dieser Auftrag gehört zur Auftrags Sammlung mit dem Namen JobCollection01 an der angegebenen Position.

## Parameter

### -First
Ruft nur die angegebene Anzahl von Objekten ab.
Geben Sie die Anzahl der abzurufenden Objekte ein.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
Gibt die Gesamtzahl der Objekte in der Datengruppe (einer ganzen Zahl) an, gefolgt von den ausgewählten Objekten.
Wenn das Cmdlet die Gesamtanzahl nicht ermitteln kann, wird "unbekannte Gesamtanzahl" angezeigt. Die ganze Zahl verfügt über eine Genauigkeits Eigenschaft, die die Zuverlässigkeit des Gesamtanzahl Werts angibt.
Der Wert der Genauigkeit reicht von 0,0 bis 1,0, wobei 0,0 bedeutet, dass das Cmdlet die Objekte nicht zählen konnte, 1,0 bedeutet, dass die Anzahl exakt ist, und ein Wert zwischen 0,0 und 1,0 eine zunehmend zuverlässige Schätzung angibt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobCollectionName
Gibt den Namen einer Scheduler-Auftrags Sammlung an.
Dieses Cmdlet ruft das Protokoll für einen Auftrag ab, der zu der Sammlung gehört, die dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Jobname
Gibt den Namen eines Scheduler-Auftrags an, für den der Verlauf abgerufen werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Jobstatus
Gibt den Status des Scheduler-Auftrags an, für den der Verlauf abgerufen werden soll.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Abgeschlossen
- Fehlgeschlagen

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Standort
Gibt den Namen des Speicherorts an, der den clouddienst hostet.
Gültige Werte sind: 

- Überall in Asien
- Überall in Europa
- Überall in den USA
- Ostasien
- East US
- Nord-Zentral-USA
- Nordeuropa
- Süd-Mittelamerika
- Südostasien
- West Europa
- West-US

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skip
Ignoriert die angegebene Anzahl von Objekten und ruft dann die restlichen Objekte ab.
Geben Sie die Anzahl der zu überspringenden Objekte ein.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureSchedulerJob](./Get-AzureSchedulerJob.md)

[Get-AzureSchedulerJobCollection](./Get-AzureSchedulerJobCollection.md)


