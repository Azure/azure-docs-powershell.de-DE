---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 76826524-480F-458E-A996-A9DBACB8BA9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa220334c75d3e6832698ec10fbad71896473d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006233"
---
# Start-AzureStorSimpleDeviceBackupJob

## Synopsis
Startet einen neuen Auftrag, mit dem eine Sicherung aus einer vorhandenen Sicherungsrichtlinie erstellt wird.

## Syntax

### Leer (Standard)
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BackupTypeGiven
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> -BackupType <String>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Start-AzureStorSimpleDeviceBackupJob** wird ein neuer Auftrag gestartet, der eine Sicherung aus einer vorhandenen Sicherungsrichtlinie auf einem StorSimple-Gerät erstellt.
Standardmäßig wird mit diesem Cmdlet eine lokale Snapshot-Sicherung erstellt.
Um eine Cloud-Sicherung zu erstellen, geben Sie einen Wert von CloudSnapshot für den *backuptype* -Parameter an.

## Beispiele

### Beispiel 1: Erstellen einer lokalen Snapshot-Sicherung
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f"
JobId                                                                StatusCode RequestId
-----                                                                ---------- ---------
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08                                 Accepted   456cf6bafd427103b71c07145e26d35c

VERBOSE: Your backup operation has been submitted for processing. Use commandlet "Get-AzureStorSimpleJob -JobId
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08" to track status.
```

Dieser Befehl erstellt eine lokale Snapshot-Sicherung für die angegebene Richtlinien-ID.
Mit diesem Befehl wird der Auftrag gestartet, und dann wird ein **TaskResponse** -Objekt zurückgegeben.
Verwenden Sie das Cmdlet " **Get-AzureStorSimpleTask** ", um den Status des Auftrags anzuzeigen.

### Beispiel 2: Erstellen einer Cloud-Snapshot-Sicherung und warten auf die Fertigstellung
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -BackupType CloudSnapshot -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f28ecf6cf75a7f128ca18e6ae14f9003
```

Mit diesem Befehl wird eine Cloud-Snapshot-Sicherung für die angegebene Richtlinien-ID erstellt.
Dieser Befehl gibt den *WaitForComplete* -Parameter an, sodass der Befehl die Aufgabe ausführt und dann ein **TaskStatusInfo** -Objekt für den Auftrag zurückgibt.

## Parameter

### -BackupPolicyId
Gibt die ID der Sicherungsrichtlinie an, die zum Erstellen der Sicherung verwendet werden soll.

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

### -Backuptype
Gibt den Sicherungstyp an.
Gültige Werte sind: LocalSnapshot und CloudSnapshot.

```yaml
Type: String
Parameter Sets: BackupTypeGiven
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Gibt den Namen des StorSimple-Geräts an, auf dem der Backup-Auftrag gestartet werden soll.

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

### Keine

## Ausgaben

### TaskStatusInfo, TaskResponse
Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.
Wenn Sie diesen Parameter nicht angeben, wird ein **TaskResponse** -Objekt zurückgegeben.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)

[Anfang-AzureStorSimpleDeviceBackupRestoreJob](./Start-AzureStorSimpleDeviceBackupRestoreJob.md)


