---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DBB3DD-B02D-4288-89CB-550EBECC2E79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4373e4eed8524db1dd5311778b3e297e766c74dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005649"
---
# Set-AzureSchedulerJobCollection

## Synopsis
Aktualisiert eine Scheduler-Auftrags Sammlung.

## Syntax

```
Set-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das Cmdlet " **Satz-AzureSchedulerJobCollection** " aktualisiert eine Scheduler-Auftrags Sammlung.

## Beispiele

### Beispiel 1: Ändern der maximalen Anzahl von Aufträgen für eine Sammlung
```
PS C:\> Set-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -MaxJobCount 30
```

Mit diesem Befehl wird die maximale Anzahl von Aufträgen für die vorhandene Scheduler-Auftrags Sammlung mit dem Namen JobCollection01 in 30 geändert.

## Parameter

### -Häufigkeit
Gibt die maximale Häufigkeit an, die für einen beliebigen Job in dieser Scheduler-Auftrags Sammlung angegeben werden kann.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Minuten
- Stunde
- Tag
- Woche
- Monat
- Jahr

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Intervall
Gibt das Intervall der Serie mit der Häufigkeit an, die mithilfe des *Frequency* -Parameters angegeben wird.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobCollectionName
Gibt den Namen der Scheduler-Auftrags Sammlung an, die aktualisiert werden soll.

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
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxJobCount
Gibt die maximale Anzahl von Aufträgen an, die in der Scheduler-Auftrags Sammlung erstellt werden können.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt an, dass dieses Cmdlet ein Objekt zurückgibt, das das Element darstellt, auf dem es ausgeführt wird.
Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plan
Gibt den Plan des Scheduler-Auftrags Sammlungs Plans an.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureSchedulerJobCollection](./Get-AzureSchedulerJobCollection.md)

[Neu – AzureSchedulerJobCollection](./New-AzureSchedulerJobCollection.md)

[Remove-AzureSchedulerJobCollection](./Remove-AzureSchedulerJobCollection.md)


