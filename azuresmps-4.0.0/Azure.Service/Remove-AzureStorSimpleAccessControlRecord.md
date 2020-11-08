---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006302"
---
# Remove-AzureStorSimpleAccessControlRecord

## Synopsis
Löscht einen Zugriffssteuerungseintrag aus der Dienstkonfiguration.

## Syntax

### IdentifyByName
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureStorSimpleAccessControlRecord** löscht einen Zugriffssteuerungseintrag aus der Dienstkonfiguration.

## Beispiele

### Beispiel 1: Entfernen eines Access Controlaccess Control recordaccess-Steuerelements
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

Dieser Befehl löscht den Zugriffssteuerungseintrag mit dem Namen Acr10.
Dieser Befehl gibt den *WaitForComplete* -Parameter an, und der Befehl wartet daher, bis der Vorgang abgeschlossen ist, und gibt dann ein **TaskStatusInfo** -Objekt zurück.

### Beispiel 2: Entfernen eines Access-Controlaccess-Steuerelement Eintrags mithilfe des pipelineAccess Controlaccess Controlaccess-Steuerelements
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

Dieser Befehl verwendet die **Get-AzureStorSimpleAccessControlRecord-** Funktion, um die **AccessControlRecord** mit dem Namen Acr10 abzurufen, und übergibt dieses Objekt dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Der Befehl startet den Vorgang, der das **AccessControlRecord** -Objekt entfernt, und gibt dann ein **TaskResponse** -Objekt zurück.
Verwenden Sie das Cmdlet **Get-AzureStorSimpleTask** , um den Status der Aufgabe anzuzeigen.

## Parameter

### -ACR
Gibt ein **AccessControlRecord** -Objekt an, das gelöscht werden soll.
Verwenden Sie das Cmdlet **Get-AzureStorSimpleAccessControlRecord** , um ein **AccessControlRecord** -Objekt abzurufen.

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ACRName
Gibt den Namen des zu löschenden Zugriffssteuerungseintrags an.

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

### AccessControlRecord
Dieses Cmdlet akzeptiert ein **AccessControlRecord** -Objekt.
Ein **AccessControlRecord** -Objekt enthält die folgenden Felder: 

- **Global** -Nr ( **Zeichenfolge** ) 
- **Initiatorname** ( **Zeichenfolge** ) 
- **InstanceId** ( **Zeichenfolge** ) 
- **Name** ( **Zeichenfolge** ) 
- **OperationInProgress** ( **OperationInProgress** ) 
- **VolumeCount** ( **int** )

## Ausgaben

### TaskStatusInfo, TaskResponse
Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.
Wenn Sie diesen Parameter nicht angeben, wird ein **TaskResponse** -Objekt zurückgegeben.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)

[Neu – AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Satz-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


