---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005818"
---
# Get-AzureSchedulerJobCollection

## Synopsis
Ruft Scheduler-Auftrags Auflistungen ab.

## Syntax

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das Cmdlet " **Get-AzureSchedulerJobCollection** " Ruft eine oder mehrere Scheduler-Auftrags Auflistungen ab.

## Beispiele

### Beispiel 1: Abrufen aller Auflistungen
```
PS C:\> Get-AzureSchedulerJobCollection
```

Dieser Befehl ruft alle Scheduler-Auftrags Auflistungen über alle Speicherorte des aktuellen Abonnements ab.

### Beispiel 2: Abrufen aller Auflistungen für einen Speicherort
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

Dieser Befehl ruft alle Scheduler-Auftrags Auflistungen an dem Speicherort mit dem Namen North Central US ab.

### Beispiel 3: Abrufen einer Sammlung mithilfe eines Namens
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

Dieser Befehl ruft die Scheduler-Auftrags Sammlung mit dem Namen JobCollection01 ab.

## Parameter

### -JobCollectionName
Gibt den Namen der abzurufenden Scheduler-Auftrags Sammlung an.

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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

[Neu – AzureSchedulerJobCollection](./New-AzureSchedulerJobCollection.md)

[Remove-AzureSchedulerJobCollection](./Remove-AzureSchedulerJobCollection.md)

[Satz-AzureSchedulerJobCollection](./Set-AzureSchedulerJobCollection.md)


