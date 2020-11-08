---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5AB916CB-A141-4662-8220-6C1FBB58FC69
online version: ''
schema: 2.0.0
ms.openlocfilehash: aab5e0f3ef432333eeb4aff68673c0d5c2219521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006670"
---
# Remove-AzureStorSimpleDeviceBackupPolicy

## Synopsis
Entfernt eine vorhandene Sicherungsrichtlinie.

## Syntax

### IdentifyById (Standard)
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureStorSimpleDeviceBackupPolicy** entfernt ein vorhandenes **BackupPolicy** -Objekt.
Nachdem Sie eine Sicherungsrichtlinie entfernt haben, erfolgen keine weiteren Sicherungen auf Grundlage dieser Richtlinie.
Mit diesem Cmdlet werden auch alle Zeitpläne gelöscht, die der gelöschten Richtlinie zugeordnet sind.

## Beispiele

### Beispiel 1: Entfernen einer Sicherungsrichtlinie
```
PS C:\>Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "03710b4c-82c1-40ca-be5c-40289dc49642" -Force
VERBOSE: ClientRequestId: b3e4d485-eae4-4cf4-a43b-815f3abcd2dd_PS
VERBOSE: ClientRequestId: a260ee98-46aa-49e0-91ac-31d4155f4cae_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: 92a9c264-90df-4345-a495-92767dd266f2_PS
695be190-ac81-4cf2-b1c5-03ef6b08d005
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
695be190-ac81-4cf2-b1c5-03ef6b08d005 for tracking the task's status
```

Mit diesem Befehl wird der **BackupPolicy** mit der Instanz-ID 03710b4c-82c1-40ca-be5c-40289dc49642 entfernt, sodass keine weiteren Sicherungen auf Grundlage dieser Richtlinie durchgeführt werden.
Der Befehl löscht auch alle Zeitpläne, die dieser Richtlinie zugeordnet sind.
Der Befehl startet den Vorgang, der das **BackupPolicy** -Objekt entfernt, und gibt dann ein **TaskResponse** -Objekt zurück.
Verwenden Sie das Cmdlet **Get-AzureStorSimpleTask** , um den Status der Aufgabe anzuzeigen.

### Beispiel 2: Entfernen der ersten Sicherungsrichtlinien für ein Gerät
```
PS C:\>$Policies = Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId $Policies[0].InstanceId -Force -WaitForComplete
VERBOSE: ClientRequestId: db3b49fa-cffa-446d-ba52-daa6802e00f7_PS
VERBOSE: ClientRequestId: 70e2b56f-c2df-40d0-a1e5-d7a4d7e25962_PS
VERBOSE: About to run a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: f8eb3d4d-2c57-4fc9-9f40-79d0f2ea1b6a_PS


JobId        : 820a246e-54b6-41a9-bdd5-15d5daea9b0a
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your remove operation has completed successfully.
```

Der erste Befehl ruft die Sicherungsrichtlinien für das Gerät mit dem Namen Contoso63-AppVm ab und speichert Sie dann in der $Policies Variablen.

Der zweite Befehl entfernt die erste Sicherungsrichtlinie aus Contoso63-AppVm.
Der Befehl verwendet die standardmäßige Punktsyntax, um die **InstanceId** -Eigenschaft des ersten Elements in $Policies zu identifizieren.
Dieser Befehl gibt den *WaitForComplete* -Parameter an, sodass der Befehl die Aufgabe ausführt und dann ein **TaskStatusInfo** -Objekt für die Aufgabe zurückgibt.

### Beispiel 3: Entfernen einer Sicherungsrichtlinie mithilfe der Pipeline
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQAVolume01_Default" | Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -Force -WaitForComplete
VERBOSE: ClientRequestId: 60080fb1-2f88-4c17-bfd7-21aa73440a9c_PS
VERBOSE: ClientRequestId: 04c91121-50d7-4796-9af6-fc6a7d6b6a0e_PS
VERBOSE: ClientRequestId: 47ceb37c-672f-42e8-bd19-1190925c46cd_PS
VERBOSE: ClientRequestId: cbc39757-f2cc-4cc5-93ea-4ec0fbfb0ca8_PS
VERBOSE: ClientRequestId: 3614d47a-51fc-4500-a5f1-5401301ca4e3_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: dbd7166e-1888-4b11-9af9-8d49712a8c8b_PS
702ad240-5730-4015-b051-56055bd2c2d3
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
702ad240-5730-4015-b051-56055bd2c2d3 for tracking the task's status
VERBOSE: BackupPolicy with id bfe0bf8a-2d09-4690-93da-38a4f24e9f4f found!
```

Dieser Befehl ruft mithilfe von **Get-AzureStorSimpleDeviceBackupPolicy** ein **BackupPolicyDetails** -Objekt ab und übergibt es dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet entfernt die Sicherungsrichtlinie mit dem Namen TSQAVolume01_Default.

## Parameter

### -BackupPolicy
Gibt das **BackupPolicyDetails** -Objekt an, das gelöscht werden soll.
Verwenden Sie das Cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** , um ein **BackupPolicyDetails** -Objekt abzurufen.

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupPolicyId
Gibt die Instanz-ID des zu löschenden **BackupPolicy** -Objekts an.

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
Gibt den Namen des StorSimple-Geräts an, auf dem die Sicherungsrichtlinie gelöscht werden soll.

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

### BackupPolicyDetails
Dieses Cmdlet akzeptiert ein zu löschendes **BackupPolicyDetails** -Objekt.

## Ausgaben

### TaskStatusInfo, TaskResponse
Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.
Wenn Sie diesen Parameter nicht angeben, wird ein **TaskResponse** -Objekt zurückgegeben.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Neu – AzureStorSimpleDeviceBackupPolicy](./New-AzureStorSimpleDeviceBackupPolicy.md)

[Satz-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


