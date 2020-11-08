---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005769"
---
# Get-AzureStorSimpleDeviceVolumeContainer

## Synopsis
Ruft Volumen Container auf einem Gerät ab.

## Syntax

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorSimpleDeviceVolumeContainer** " Ruft eine Liste mit Volumen Containern auf einem Gerät oder einem Volumen Container mit dem angegebenen Namen ab.
Das zurückgegebene Objekt enthält die folgenden Eigenschaften: 

- **BandwidthRate**
- **EncryptionKey**
- **InstanceId**
- **IsDefault**
- **IsEncryptionEnabled**
- **Namen**
- **OperationInProgress**
- **Eigentum**
- **PrimaryStorageAccountCredential**
- **SecretsEncryptionThumbprint**
- **VolumeCount**

## Beispiele

### Beispiel 1: Abrufen aller Container auf einem Gerät
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

Dieser Befehl ruft eine Liste der Volumen Container auf dem Gerät mit dem Namen 8600-Bravo 001 ab.

### Beispiel 2: Abrufen eines Containers mit dem Namen
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

Dieser Befehl ruft den Volumen Container mit dem Namen Container08 auf dem Gerät mit dem Namen Contoso63-AppVm ab.

## Parameter

### -DeviceName
Gibt den Namen eines StorSimple-Geräts an.
Dieses Cmdlet ruft Volumen Container vom Gerät ab, das dieser Parameter angibt.

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

### -VolumeContainerName
Gibt den Namen des abzurufenden Volumen Containers an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### DataContainer, IList\<DataContainer\>
Wenn Sie den *VolumeContainerName* -Parameter angeben, gibt dieses Cmdlet ein **DataContainer** -Objekt zurück.
Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet ein **IList \<DataContainer\>** -Objekt zurück.

## Notizen

## Verwandte Links

[Neu – AzureStorSimpleDeviceVolumeContainer](./New-AzureStorSimpleDeviceVolumeContainer.md)

[Remove-AzureStorSimpleDeviceVolumeContainer](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


