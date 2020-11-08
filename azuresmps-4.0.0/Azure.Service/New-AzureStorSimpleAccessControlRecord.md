---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006416"
---
# New-AzureStorSimpleAccessControlRecord

## Synopsis
Erstellt einen Zugriffssteuerungseintrag.

## Syntax

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureStorSimpleAccessControlRecord** erstellt einen Zugriffssteuerungseintrag.
Sie können ein **AccessControlRecord** -Objekt verwenden, um Volumes zu konfigurieren.

## Beispiele

### Beispiel 1: Erstellen eines Zugriffs Controlaccess-Steuerelement Eintrags und warten auf das resultaccess-Steuerelement
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

Dieser Befehl erstellt einen Zugriffssteuerungseintrag mit dem Namen Acr10 für den iSCSI-Initiator mit dem Namen Iqn10.
Dieser Befehl gibt den *WaitForComplete* -Parameter an, und der Befehl wartet daher, bis der Vorgang abgeschlossen ist, und gibt dann ein **TaskStatusInfo** -Objekt zurück.

### Beispiel 2: Erstellen eines Access Controlaccess Control recordaccess-Steuerelements
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

Dieser Befehl erstellt einen Zugriffssteuerungseintrag mit dem Namen Acr11 für den iSCSI-Initiator mit dem Namen Iqn11.
Mit diesem Befehl wird der *WaitForComplete* -Parameter nicht angegeben, und daher wird der Befehl von der Aufgabe gestartet und dann ein **TaskResponse** -Objekt zurückgegeben.
Verwenden Sie das Cmdlet **Get-AzureStorSimpleTask** , um den Status der Aufgabe anzuzeigen.

## Parameter

### -ACRName
Gibt einen Namen für den Zugriffssteuerungseintrag an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IQNInitiatorName
Gibt den iSCSI Qualified Name (IQN) des iSCSI-Initiators an, dem dieses Cmdlet Zugriff auf das Volume gewährt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

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

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)

[Remove-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Satz-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


