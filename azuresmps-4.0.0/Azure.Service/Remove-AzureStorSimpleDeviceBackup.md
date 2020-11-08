---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006673"
---
# Remove-AzureStorSimpleDeviceBackup

## Synopsis
Löscht ein Sicherungsobjekt.

## Syntax

### IdentifyById (Standard)
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureStorSimpleDeviceBackup** löscht ein einzelnes Sicherungsobjekt.
Wenn Sie versuchen, eine bereits gelöschte Sicherung zu löschen, gibt dieses Cmdlet einen Fehler zurück.

## Beispiele

### Beispiel 1: Entfernen einer Sicherung für ein Gerät
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

Dieser Befehl entfernt die Sicherung mit der angegebenen ID für das Gerät mit dem Namen Contoso63-AppVm.
Der Befehl startet den Vorgang, der das **Sicherungs** Objekt entfernt, und gibt dann ein **TaskResponse** -Objekt zurück.
Verwenden Sie das Cmdlet **Get-AzureStorSimpleTask** , um den Status der Aufgabe anzuzeigen.

### Beispiel 2: Entfernen der ersten Sicherung für ein Gerät mithilfe der ID
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

Der erste Befehl ruft die Sicherungen für das Gerät mit dem Namen Contoso63-AppVm ab und speichert Sie dann in der $Backup Variablen.

Der zweite Befehl löscht eine Sicherung vom Gerät mit dem Namen Contoso63-AppVm.
Der Befehl verwendet die standardmäßige Punktnotation, um auf die **InstanceId** -Eigenschaft des ersten Elements des $Backup-Arrays zu verweisen.
Dieser Befehl gibt den *WaitForComplete* -Parameter an, und der Befehl wartet daher, bis der Vorgang abgeschlossen ist, und gibt dann ein **TaskStatusInfo** -Objekt zurück.

### Beispiel 3: Entfernen der ersten Sicherung für ein Gerät mithilfe der Pipeline
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

Der erste Befehl ruft die Sicherungen für das Gerät mit dem Namen Contoso63-AppVm ab und speichert Sie dann in der $Backup Variablen.

Der zweite Befehl übergibt das erste im $Backup-Array gespeicherte Objekt an das aktuelle Cmdlet.
Dieses Cmdlet löscht diese Sicherung vom Gerät mit dem Namen Contoso63-AppVm.
Dieser Befehl gibt den *WaitForComplete* -Parameter an, und der Befehl wartet daher, bis der Vorgang abgeschlossen ist, und gibt dann ein **TaskStatusInfo** -Objekt zurück.

## Parameter

### -Backup
Gibt das zu löschende **Sicherungs** Objekt an.
Wenn Sie ein **Sicherungs** Objekt abrufen möchten, verwenden Sie das Cmdlet **Get-AzureStorSimpleDeviceBackup** .

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Backup-Nr.
Gibt die Instanz-ID einer zu löschenden Sicherung an.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Gibt den Namen des StorSimple-Geräts an, auf dem eine Sicherung gelöscht werden soll.

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

### Backup

## Ausgaben

### TaskStatusInfo, TaskResponse
Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben, wenn Sie diesen Parameter nicht angeben, wird ein **TaskResponse** -Objekt zurückgegeben.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleDeviceBackup](./Get-AzureStorSimpleDeviceBackup.md)


