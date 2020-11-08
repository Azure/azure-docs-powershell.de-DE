---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005764"
---
# Get-AzureStorSimpleJob

## Synopsis
Ruft StorSimple-Aufträge ab.

## Syntax

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorSimpleJob** " ruft Azure StorSimple-Aufträge ab.
Geben Sie eine Instanz-ID an, um einen bestimmten Job zu erhalten.
Geben Sie andere Parameter an, um die von diesem Cmdlet abgerufenen Aufträge zu begrenzen.

Dieses Cmdlet gibt maximal 200-Aufträge zurück.
Wenn mehr als 200-Aufträge vorhanden sind, rufen Sie die verbleibenden Aufträge mithilfe des *First* -und *Skip* -Parameters ab.
Wenn Sie einen Wert von 100 für *Skip* und 50 für *First* angeben, gibt dieses Cmdlet nicht die ersten 100 Ergebnisse zurück.
Nach dem 100 werden die nächsten 50-Ergebnisse zurückgegeben, die übersprungen werden.

## Beispiele

### Beispiel 1: Abrufen eines Auftrags mithilfe einer ID
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

Dieser Befehl ruft Informationen für den Auftrag ab, der die angegebene ID aufweist.

### Beispiel 2: Abrufen von Aufträgen mit einem Gerätenamen
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

Dieser Befehl ruft Informationen zu den Aufträgen für das Gerät mit dem Namen 8600-Bravo 001 ab.
Der Befehl ruft die ersten beiden Aufträge für das Gerät ab.

### Beispiel 3: Abrufen von abgeschlossenen Aufträgen
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

Dieser Befehl ruft abgeschlossene Aufträge ab.
Der Befehl ruft nur die ersten beiden Aufträge ab, nachdem er die ersten zehn Aufträge übersprungen hat.

### Beispiel 4: Abrufen manueller Backup-Aufträge
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

Dieser Befehl ruft Aufträge des manuellen Sicherungstyps ab.

### Beispiel 5: Abrufen von Aufträgen zwischen angegebenen Zeiten
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

Die ersten beiden Befehle erstellen **DateTime** -Objekte mithilfe des Get-Date-Cmdlets.
Die Befehle speichern die neuen Uhrzeiten in den $StartTime-und $EndTime Variablen.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .

Der endgültige Befehl ruft Aufträge für das Gerät mit dem Namen Device07 zwischen den in $StartTime und $EndTime gespeicherten Zeiten ab.

## Parameter

### -DeviceName
Gibt den Namen eines StorSimple-Geräts an.

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

### -First
Ruft nur die angegebene Anzahl von Objekten ab.
Geben Sie die Anzahl der abzurufenden Objekte ein.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ab
Gibt das Startdatum und die Startzeit für die Aufträge an, die dieses Cmdlet erhält.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Gibt die ID des abzurufenden Auftrags an.

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

### -Skip
Ignoriert die angegebene Anzahl von Objekten und ruft dann die restlichen Objekte ab.
Geben Sie die Anzahl der zu überspringenden Objekte ein.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Gibt den Status an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Ausgeführt
- Abgeschlossen
- Storniert
- Fehlgeschlagen
- Cancelling
- CompletedWithErrors

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

### -To
Gibt das Enddatum und die Endzeit für die Aufträge an, die dieses Cmdlet erhält.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Typ
Gibt den Auftragstyp an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Backup
- ManualBackup
- Wiederherstellungs
- CloneWorkflow
- DeviceRestore
- Aktualisieren
- SupportPackage
- VirtualApplianceProvisioning

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Sie können keine Eingabe an dieses Cmdlet übergeben.

## Ausgaben

### IList \<DeviceJobDetails\> , DeviceJobDetails
Dieses Cmdlet gibt eine Liste von Auftragsdetail Objekten zurück, oder wenn Sie den *InstanceId* -Parameter angeben, wird ein einzelnes Auftragsdetail Objekt zurückgegeben.

## Notizen

## Verwandte Links

[Stopp-AzureStorSimpleJob](./Stop-AzureStorSimpleJob.md)


