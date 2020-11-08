---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006497"
---
# Get-AzureStorSimpleDeviceConnectedInitiator

## Synopsis
Ruft die iSCSI-Verbindungen ab, die für ein StorSimple-Gerät verfügbar sind.

## Syntax

### IdentifyById
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorSimpleDeviceConnectedInitiator** " Ruft eine Liste der iSCSI-Verbindungen ab, die für ein StorSimple-Gerät verfügbar sind.
Die von diesem Cmdlet zurückgegebenen iSCSI-Verbindungsobjekte enthalten die folgenden Eigenschaften:

- **AcrInstanceId**
- **AcrName**
- **AllowedVolumeNames**
- **InitiatorAddress**
- **Schnittstellen**
- **IQN**
- **IscsiConnectionId**

Dieses Cmdlet ruft nur dann Connection-Objekt ab, wenn iSCSI-Verbindungen für das Gerät aktiviert sind.
Standardmäßig sind Verbindungen deaktiviert.

## Beispiele

### Beispiel 1: Abrufen aller Verbindungen für ein Gerät
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

Dieser Befehl ruft alle iSCSI-Verbindungen für das Gerät mit dem Namen Contoso63-AppVm.
Dieser Befehl gibt nur dann Verbindungen zurück, wenn Verbindungen für das Gerät aktiviert sind.

## Parameter

### -Geräte-Nr
Gibt die Instanz-ID des StorSimple-Geräts an, aus dem iSCSI-Initiatoren abgerufen werden sollen.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Gibt den Namen des StorSimple-Geräts an, aus dem iSCSI-Initiatoren abgerufen werden sollen.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Liste\<IscsiConnection\>
Dieses Cmdlet gibt ein iSCSI-Verbindungsobjekt zurück, das die folgenden Eigenschaften enthält: 

- **AcrInstanceId**
- **AcrName**
- **AllowedVolumeNames**
- **InitiatorAddress**
- **Schnittstellen**
- **IQN**
- **IscsiConnectionId**

## Notizen

## Verwandte Links

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)


