---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-help.xml
ms.assetid: 02F429EA-FE9A-427F-86B5-C9C4275FD3EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 289cc21b6edd2a841b8121672d838aaa056db4f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005904"
---
# Copy-AzureRemoteAppUserDisk

## Synopsis
Kopiert den Benutzerdatenträger eines Benutzers aus einer Azure RemoteApp-Sammlung in einen anderen.

## Syntax

```
Copy-AzureRemoteAppUserDisk [-SourceCollectionName] <String> [-DestinationCollectionName] <String>
 [-UserUpn] <String> [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Copy-AzureRemoteAppUserDisk** kopiert den Benutzerdatenträger eines Benutzers aus einer Azure RemoteApp-Sammlung in einen anderen.

## Beispiele

### Beispiel 1: Kopieren eines Benutzer Datenträgers
```
PS C:\> Copy-AzureRemoteAppUserDisk -DestinationCollectionName "Contoso02" -SourceCollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com" -OverwriteExistingUserDisk
```

Mit diesem Befehl wird der Benutzerdatenträger eines Azure Active Directory-Benutzers kopiert, der über den UPN PattiFuller@contoso.com aus der Auflistungs-contoso01 zum Contoso02 der Sammlung verfügt.
Wenn bereits ein Benutzerdatenträger für PattiFuller@contoso.com Contoso02 vorhanden ist, wird dieser durch diesen Befehl überschrieben.

## Parameter

### -DestinationCollectionName
Gibt den Namen der Ziel Azure RemoteApp-Sammlung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OverwriteExistingUserDisk
Gibt an, dass mit diesem Cmdlet ein vorhandener Benutzerdatenträger überschrieben wird.

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

### -SourceCollectionName
Gibt den Namen der Quell Azure RemoteApp-Sammlung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserUpn
Gibt den Benutzerprinzipalnamen (User Principal Name, UPN) des Benutzers an, für den das Cmdlet den Datenträger kopiert.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Remove-AzureRemoteAppUserDisk](./Remove-AzureRemoteAppUserDisk.md)


