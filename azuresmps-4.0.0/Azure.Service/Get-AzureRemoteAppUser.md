---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6F2CC9F-8C95-484D-8676-7DAA5E0AA617
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf2a5cc1390db2a6ae5eb49894a47d1ccf0aca4c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006522"
---
# Get-AzureRemoteAppUser

## Synopsis
Listet die Benutzer in einer Azure RemoteApp-Sammlung auf.

## Syntax

```
Get-AzureRemoteAppUser [-CollectionName] <String> [[-UserUpn] <String>] [-Alias <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRemoteAppUser** " listet die Benutzer in einer Azure RemoteApp-Sammlung auf.

## Beispiele

### Beispiel 1: Auflisten der Benutzer einer Sammlung
```
PS C:\> Get-AzureRemoteAppUser -CollectionName "Contoso"
```

Dieser Befehl listet die Benutzer auf, die Zugriff auf die Azure RemoteApp-Sammlung mit dem Namen "Contoso" haben.

## Parameter

### -Alias
Gibt einen veröffentlichten Programm-Alias an.
Sie können diesen Parameter nur im pro-App-Veröffentlichungsmodus verwenden.

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

### -CollectionName
Gibt den Namen der Azure RemoteApp-Sammlung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
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

### -UserUpn
Gibt den Benutzerprinzipalnamen (User Principal Name, UPN) eines Benutzers an, für den Informationen aufgelistet werden sollen.
Beispiel: PattiFuller@contoso.com .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Add-AzureRemoteAppUser](./Add-AzureRemoteAppUser.md)

[Get-AzureRemoteAppSession](./Get-AzureRemoteAppSession.md)

[Remove-AzureRemoteAppUser](./Remove-AzureRemoteAppUser.md)


