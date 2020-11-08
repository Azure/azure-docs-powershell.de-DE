---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006334"
---
# Remove-AzureSchedulerJobCollection

## Synopsis
Löscht eine Scheduler-Auftrags Sammlung.

## Syntax

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das Cmdlet **Remove-AzureSchedulerJobCollection** löscht eine Scheduler-Auftrags Sammlung und alle Aufträge unter dieser Auflistung.

## Beispiele

### Beispiel 1: Löschen einer Auftrags Sammlung für einen Speicherort
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

Dieser Befehl löscht die Scheduler-Auftrags Sammlung mit dem Namen JobCollection01 im Nord zentralen US-Standort.
Der Befehl löscht auch die Aufträge unter JobCollection01.

### Beispiel 2: Löschen eines Auftragsspeicher Orts
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

Dieser Befehl löscht die Scheduler-Auftrags Sammlung mit dem Namen JobCollection02.
Der Befehl löscht auch die Aufträge unter JobCollection02.

## Parameter

### -Force
Gibt an, dass dieses Cmdlet die Scheduler-Auftrags Sammlung entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.

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

### -JobCollectionName
Gibt den Namen der zu löschenden Scheduler-Auftrags Sammlung an.

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

[Satz-AzureSchedulerJobCollection](./Set-AzureSchedulerJobCollection.md)


