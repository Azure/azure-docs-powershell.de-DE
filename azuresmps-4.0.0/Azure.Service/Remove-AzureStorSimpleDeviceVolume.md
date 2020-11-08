---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A62D1A9D-C0EF-4305-B1F9-3AE68A79222D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a5023abffae6bbc2b70b7400e604ffabb1d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006666"
---
# Remove-AzureStorSimpleDeviceVolume

## Synopsis
Entfernt ein Volume von einem StorSimple-Gerät.

## Syntax

### IdentifyByName
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureStorSimpleDeviceVolume** entfernt ein Volume von einem StorSimple-Gerät.
Dieses Cmdlet fordert Sie zur Bestätigung auf, es sei denn, Sie geben den Parameter *Force* an.

## Beispiele

### Beispiel 1: Entfernen eines Volumes mithilfe der Pipeline
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" | Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: 2933e24d-9564-42b5-9053-5f0bc4f59ea8_PS
VERBOSE: ClientRequestId: 7c2d854b-537a-4253-bb0c-c15bc8aa2b49_PS
VERBOSE: ClientRequestId: 4bf749ac-517c-49e7-8027-a8f62e272014_PS
VERBOSE: ClientRequestId: 7d9ec87a-616d-4ca9-bfb8-158859174d59_PS

Confirm
Are you sure you want to remove the volume? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 67a38e28-a015-44b1-8159-c1a6604f4d81_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: 56101c10-07ca-40f4-8f19-c6fdd895e3a5_PS
32925451-4451-4478-89f7-d8930505d3fb
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
32925451-4451-4478-89f7-d8930505d3fb for tracking the task's status
VERBOSE: Volume with name: Volume18 is found.
```

Dieser Befehl ruft das Volume mit dem Namen Volume18 auf dem Gerät mit dem Namen Contoso63-AppVm ab und übergibt dann das Volume mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet startet die Aufgabe, die das Volume entfernt, und gibt dann ein **TaskResponse** -Objekt zurück.
Verwenden Sie das Cmdlet **Get-AzureStorSimpleTask** , um den Status der Aufgabe anzuzeigen.
Der Befehl gibt keinen *Force* -Parameter an, sodass Sie vom Cmdlet zur Bestätigung aufgefordert werden.

### Beispiel 2: Entfernen eines Volumes ohne Bestätigung
```
PS C:\>Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Force
VERBOSE: ClientRequestId: 72f13290-41eb-4ac4-9535-da1a42d0fa0b_PS
VERBOSE: ClientRequestId: ae0c1d99-1a66-4a69-9260-f2c8c12546bd_PS
VERBOSE: ClientRequestId: 9610744f-d031-488f-87e6-3ecddb305e13_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: d33525d8-7276-4d2a-942d-d10f8078f1f7_PS
483f8cb4-ebc3-46a9-a9e6-0989e25738a0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
483f8cb4-ebc3-46a9-a9e6-0989e25738a0 for tracking the task's status
```

Dieser Befehl entfernt das Volume mit dem Namen Volume18 aus dem Gerät namens Contoso63-AppVm.
Der Befehl gibt den Parameter *Force* an, sodass Sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.

## Parameter

### -DeviceName
Gibt den Namen des StorSimple-Geräts an, auf dem das zu entfernende Volume vorhanden ist.

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

### -Force
Gibt an, dass Sie von diesem Cmdlet nicht zur Bestätigung aufgefordert werden.

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

### -Profil
Gibt ein Azure-Profil an.

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

### -Lautstärke
Gibt das zu entfernende Volume als **VirtualDisk** -Objekt an.
Verwenden Sie das Cmdlet **Get-AzureStorSimpleDeviceVolume** , um ein **VirtualDisk** -Objekt abzurufen.

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Volumename
Gibt den Namen des zu entfernenden Volumes an.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### VirtualDisk
Dieses Cmdlet akzeptiert entweder das zu löschende **VirtualDisk** -Objekt oder den volumennamen des zu löschenden **VirtualDisk** .

## Ausgaben

### TaskStatusInfo
Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)

[Neu – AzureStorSimpleDeviceVolume](./New-AzureStorSimpleDeviceVolume.md)

[Satz-AzureStorSimpleDeviceVolume](./Set-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


