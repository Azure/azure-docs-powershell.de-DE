---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 1BD296FB-8BFC-473F-951D-D2BF265E50AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 048be9276957ee865aa3204392b1dd847b0d6acf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006655"
---
# Remove-AzureStorSimpleStorageAccountCredential

## Synopsis
Löscht eine vorhandene Speicherkonto Anmeldeinformationen.

## Syntax

### IdentifyByName
```
Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleStorageAccountCredential -SAC <StorageAccountCredentialResponse> [-WaitForComplete]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureStorSimpleStorageAccountCredential** löscht eine vorhandene Speicherkonto Anmeldeinformationen.
Geben Sie ein Konto nach Namen an, oder verwenden Sie das Cmdlet " **Get-AzureStorSimpleStorageAccountCredential** ", um ein **StorageAccountCredential** -Objekt zum Löschen abzurufen.

## Beispiele

### Beispiel 1: Entfernen der Anmeldeinformationen eines speicherkontos
```
PS C:\>Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" -Force
VERBOSE: ClientRequestId: 8e10d56b-ddb1-459b-b26e-a185f5a303de_PS
VERBOSE: About to create a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: 55cb6296-0156-4266-8591-d9e9bf8cc584_PS
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72 for tracking the task's status
```

Dieser Befehl entfernt die Kontoanmeldeinformationen für das Speicherkonto mit dem Namen ContosoStorage07.
Mit diesem Befehl wird der *Force* -Parameter angegeben.
Das Cmdlet entfernt die Anmeldeinformationen, ohne dass Sie zur Bestätigung aufgefordert werden.

### Beispiel 2: Entfernen der Anmeldeinformationen eines speicherkontos mithilfe des Pipelineoperators
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" | Remove-AzureStorSimpleStorageAccountCredential -Force -WaitForComplete
VERBOSE: ClientRequestId: f1b46216-bf4c-4c19-8e92-1dfe3894e258_PS
VERBOSE: ClientRequestId: 0d946f8f-c771-4ade-8a83-7c08dad86c52_PS
VERBOSE: ClientRequestId: 2000bab6-8311-4192-ad12-c67e35fc2697_PS
VERBOSE: Storage Access Credential with name ContosoStorage07 found! 
VERBOSE: About to run a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: b803b165-bef8-4a8f-9509-4b515ea8bdec_PS
VERBOSE: Your delete operation completed successfully!
```

Dieser Befehl ruft das Speicherkonto mit dem Namen ContosoStorage07 mit dem Cmdlet **Get-AzureStorSimpleStorageAccountCredential** ab und übergibt dieses Objekt dann an das aktuelle Cmdlet.
Das aktuelle Cmdlet entfernt die Anmeldeinformationen für dieses Speicherkonto.
Mit diesem Befehl wird der *WaitForComplete* -Parameter angegeben.
Das Cmdlet gibt erst dann die Steuerung an die Konsole zurück, wenn der Löschvorgang abgeschlossen ist.

## Parameter

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

### -SAC
Gibt Anmeldeinformationen als **StorageAccountCredential** -Objekt an, um Sie zu entfernen.
Verwenden Sie das Cmdlet **Get-AzureStorSimpleStorageAccountCredential** , um ein **StorageAccountCredential** -Objekt abzurufen.

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Gibt den Namen der zu löschenden Speicherkonto Anmeldeinformationen an.

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

### StorageAccountCredential
Dieses Cmdlet akzeptiert ein **StorageAccountCredential** -Objekt mithilfe der Pipeline.

## Ausgaben

### TaskStatusInfo
Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleStorageAccountCredential](./Get-AzureStorSimpleStorageAccountCredential.md)

[Neu – AzureStorSimpleStorageAccountCredential](./New-AzureStorSimpleStorageAccountCredential.md)

[Satz-AzureStorSimpleStorageAccountCredential](./Set-AzureStorSimpleStorageAccountCredential.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


