---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006714"
---
# Get-WAPackCloudVMRoleSizeProfile

## Synopsis
Ruft Cloud VM-Rollengröße-Profilobjekte ab.

## Syntax

### Leer (Standard)
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-WAPackCloudVMRoleSizeProfile** " ruft Cloud VM-Rollengröße-Profilobjekte für virtuelle Computer ab.

## Beispiele

### Beispiel 1: Abrufen eines VM-Rollen Formats für eine Cloud mit einem Namen
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

Dieser Befehl ruft das Größen Profil mit dem Namen klein ab.

### Beispiel 2: Abrufen aller Rollenformat Profile für die VM-Cloud
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

Dieser Befehl ruft alle Größen Profile ab.

## Parameter

### -Name
Gibt den Namen eines VM-Rollengrößen Profils für die Cloud an.

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

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

## Ausgaben

## Notizen

## Verwandte Links

[Get-WAPackVM](./Get-WAPackVM.md)


