---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006758"
---
# Get-AzureStorSimpleAccessControlRecord

## Synopsis
Ruft Zugriffssteuerungseinträge in einer Dienstkonfiguration ab.

## Syntax

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorSimpleAccessControlRecord** " ruft Zugriffssteuerungseinträge in der StorSimple-Manager-Dienstkonfiguration ab.
Mit diesem Cmdlet werden alle Datensätze oder ein benannter Datensatz abgerufen.

Zugriffssteuerungseinträge sind Container mit iSCSI-initiatorparameter.
Diese Parameter geben an, welche Initiatoren auf ein Volume zugreifen können.
Wenn ein iSCSI-Initiator versucht, eine Verbindung mit einem Volume herzustellen, überprüft Ihre Appliance die Zugriffssteuerungseinträge, die diesem Volume zugewiesen sind.
Wenn die Parameter des iSCSI-Initiators mit einem der Einträge in einem Zugriffssteuerungseintrag übereinstimmen, der diesem Volume zugeordnet ist, kann der iSCSI-Initiator eine Verbindung herstellen.

## Beispiele

### Beispiel 1: Abrufen aller Zugriffssteuerungseinträge
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

Dieser Befehl ruft alle Zugriffssteuerungseinträge ab.

### Beispiel 2: Abrufen eines bestimmten Zugriffssteuerungseintrags
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

Dieser Befehl ruft den Zugriffssteuerungseintrag mit dem Namen Acr11 ab.

## Parameter

### -ACRName
Gibt den Namen eines Zugriffssteuerungseintrags an, der abgerufen werden soll.

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

### AccessControlRecord, IList\<AccessControlRecord\>
Dieses Cmdlet gibt ein **AccessControlRecord** -Objekt oder **ein \<AccessControlRecord\> IList** -Objekt zurück.
Ein **AccessControlRecord** -Objekt enthält die folgenden Felder: 

- **Global** -Nr ( **Zeichenfolge** ) 
- **Initiatorname** ( **Zeichenfolge** ) 
- **InstanceId** ( **Zeichenfolge** ) 
- **Name** ( **Zeichenfolge** ) 
- **OperationInProgress** ( **OperationInProgress** ) 
- **VolumeCount** ( **int** )

## Notizen

## Verwandte Links

[Neu – AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Remove-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Satz-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)


