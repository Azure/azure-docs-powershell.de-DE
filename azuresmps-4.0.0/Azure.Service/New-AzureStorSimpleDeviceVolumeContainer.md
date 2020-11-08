---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5605F11E-EEA0-4C32-8445-2E001D56BC47
online version: ''
schema: 2.0.0
ms.openlocfilehash: e364692858cf190b48b61f4d38fbf483d229ffb7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005726"
---
# New-AzureStorSimpleDeviceVolumeContainer

## Synopsis
Erstellt einen Volumen Container.

## Syntax

```
New-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainerName <String>
 -PrimaryStorageAccountCredential <StorageAccountCredentialResponse> -BandWidthRateInMbps <Int32>
 [-EncryptionEnabled <Boolean>] [-EncryptionKey <String>] [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureStorSimpleDeviceVolumeContainer** erstellt einen Volumen Container.
Sie müssen dem neuen Volumen Container eine Speicherkonto Anmeldeinformationen zuordnen.
Verwenden Sie das Cmdlet **Get-AzureStorSimpleStorageAccountCredential** , um die Anmeldeinformationen eines speicherkontos zu erhalten.

## Beispiele

### Beispiel 1: Erstellen eines Containers
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount" | New-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" -BandWidthRateInMbps 256
VERBOSE: ClientRequestId: 96a4ccd4-f2a9-4820-8bc8-e6b7b56dce0d_PS
VERBOSE: ClientRequestId: 90be20db-098a-4f2b-a6da-9da6f533a846_PS
VERBOSE: ClientRequestId: 410fd33a-8fa3-4ae5-a1bf-1b6da9b34ffc_PS
VERBOSE: Storage Access Credential with name ContosoAccount found! 
VERBOSE: ClientRequestId: 0a6d1008-ba1f-43b2-a424-9c86be2fb83b_PS
VERBOSE: ClientRequestId: 08f0d657-a130-4a25-8090-270c58b479dc_PS
VERBOSE: ClientRequestId: 0f3e894a-b031-467c-a258-41b74c89cf18_PS
5b192120-9df0-40ed-b75e-b4e728bd37ef
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
5b192120-9df0-40ed-b75e-b4e728bd37ef for tracking the task's status
```

Dieser Befehl ruft die Speicherkonto Anmeldeinformationen für das Konto mit dem Namen ContosoAccount mit dem Cmdlet **Get-AzureStorSimpleStorageAccountCredential** ab.
Der Befehl übergibt die Anmeldeinformationen mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Dieses Cmdlet verwendet die Anmeldeinformationen dieses Cmdlets, um den Container mit dem Namen Container08 auf dem Gerät mit dem Namen Contoso63-AppVm zu erstellen.
Mit diesem Befehl wird der Auftrag gestartet, und dann wird ein **TaskResponse** -Objekt zurückgegeben.
Verwenden Sie das Cmdlet " **Get-AzureStorSimpleTask** ", um den Status des Auftrags anzuzeigen.

## Parameter

### -BandWidthRateInMbps
Gibt die Bandbreiten Rate in Megabit pro Sekunde (Mbit/s) an.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CloudBandwidthInMbps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Gibt den Namen des StorSimple-Geräts an, auf dem der Volumen Container erstellt werden soll.

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

### -EncryptionEnabled
Gibt an, ob die Verschlüsselung aktiviert werden soll.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKey
Gibt den Verschlüsselungsschlüssel an.

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

### -PrimaryStorageAccountCredential
Gibt die Anmeldeinformationen als **StorageAccountCredential** -Objekt an, das dem neuen Volumen Container zugeordnet werden soll.
Verwenden Sie das Cmdlet **Get-AzureStorSimpleStorageAccountCredential** , um ein **StorageAccountCredential** -Objekt abzurufen.

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: (All)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -VolumeContainerName
Gibt den Namen des zu erstellende Volumen Containers an.

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
Dieses Cmdlet akzeptiert ein **PrimaryStorageAccountCredential** -Objekt, das dem Volumen Container zugeordnet werden soll.

## Ausgaben

### TaskStatusInfo
Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[Remove-AzureStorSimpleDeviceVolumeContainer](./Remove-AzureStorSimpleDeviceVolumeContainer.md)

[Get-AzureStorSimpleStorageAccountCredential](./Get-AzureStorSimpleStorageAccountCredential.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


