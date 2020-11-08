---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BF054CA4-B0A4-4BFC-A657-92A0D3ABBCB5
online version: ''
schema: 2.0.0
ms.openlocfilehash: f82db6a826a6ed612e1d98c7cef6ab642bf15858
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005757"
---
# Get-AzureStorSimpleStorageAccountCredential

## Synopsis
Ruft Anmeldeinformationen für Speicherkonten ab.

## Syntax

```
Get-AzureStorSimpleStorageAccountCredential [-StorageAccountName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorSimpleStorageAccountCredential** " ruft Anmeldeinformationen für Speicherkonten ab.
Dieses Cmdlet ruft alle **StorageAccountCredential** -Objekte ab, die im Dienst konfiguriert sind, oder ein benanntes **StorageAccountCredential**.

## Beispiele

### Beispiel 1: Abrufen aller Anmeldeinformationen für eine Ressource
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential
InstanceId                           Login           Name            UseSSL VolumeCount     CloudType    Location
----------                           -----           ----            ------ -----------     ---------    --------
b5e0857f-82ef-4426-883b-a612889ebee4 qwertyuiopa     AdminAccount    True   24              Azure
```

Dieser Befehl ruft alle verfügbaren Anmeldeinformationen für Speicherkonten für die aktuelle Ressource ab.

### Beispiel 2: Abrufen der Anmeldeinformationen für ein bestimmtes Speicherkonto
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoCloudStorage"
VERBOSE: ClientRequestId: 16551af6-3398-4d30-a389-1b8eb01ce92c_PS
VERBOSE: ClientRequestId: 5041277d-4044-4b6c-ae19-4ea9e7ae135a_PS
VERBOSE: Storage Access Credential with name ContosoCloudStorage found! 


CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoCloudStorage
Name                             : ContosoCloudStorage
OperationInProgress              : None
Password                         : 
PasswordEncryptionCertThumbprint : 
UseSSL                           : True
VolumeCount                      : 0
```

Dieser Befehl ruft die Speicherkonto Anmeldeinformationen für das Speicherkonto mit dem Namen ContosoCloudStorage ab.

## Parameter

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

### -StorageAccountName
Gibt den Namen des speicherkontos an, für das Anmeldeinformationen abgerufen werden sollen.

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

### StorageAccountCredential, IList\<StorageAccountCredential\>
Dieses Cmdlet gibt ein **StorageAccountCredential** -Objekt zurück, wenn Sie den *StorageAccountName* -Parameter angeben, oder wenn Sie diesen Parameter nicht angeben, wird **ein \<StorageAccountCredential\> IList** -Objekt zurückgegeben.

## Notizen

## Verwandte Links

[Neu – AzureStorSimpleStorageAccountCredential](./New-AzureStorSimpleStorageAccountCredential.md)

[Remove-AzureStorSimpleStorageAccountCredential](./Remove-AzureStorSimpleStorageAccountCredential.md)

[Satz-AzureStorSimpleStorageAccountCredential](./Set-AzureStorSimpleStorageAccountCredential.md)


