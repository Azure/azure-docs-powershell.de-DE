---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006517"
---
# Get-AzureSchedulerJob

## Synopsis
Ruft eine Liste der Scheduler-Aufträge oder eines bestimmten Scheduler-Auftrags ab.

## Syntax

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das Cmdlet " **Get-AzureSchedulerJobCollection** " Ruft eine Liste der Scheduler-Aufträge oder eines bestimmten Scheduler-Auftrags ab.

## Beispiele

### Beispiel 1: Abrufen aller Aufträge in einer Sammlung
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

Dieser Befehl ruft Scheduler-Aufträge ab, die Teil der Auftrags Sammlung mit dem Namen JobCollection01 sind.

### Beispiel 2: Abrufen eines benannten Auftrags
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

Dieser Befehl ruft den Auftrag mit dem Namen Job01 aus der Sammlung mit dem Namen JobCollection01 an der angegebenen Position ab.

### Beispiel 3: Abrufen von deaktivierten Aufträgen in einer Sammlung
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

Dieser Befehl ruft alle deaktivierten Scheduler-Aufträge ab, die Teil von JobCollection01 an der angegebenen Position sind.

## Parameter

### -JobCollectionName
Gibt den Namen der Sammlung an, die den abzurufenden Scheduler-Auftrag enthält.

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
Gibt den Namen des abzurufenden Scheduler-Auftrags an.

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

### -JobState
Gibt den Zustand der abzurufenden Scheduler-Aufträge an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Aktiviert
- Deaktiviert
- Faulted
- Abgeschlossen

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
Die zulässigen Werte für diesen Parameter lauten wie folgt:

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Remove-AzureSchedulerJob](./Remove-AzureSchedulerJob.md)


