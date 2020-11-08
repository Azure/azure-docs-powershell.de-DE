---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006783"
---
# Get-AzureRemoteAppSession

## Synopsis
Listet alle aktiven und getrennten Azure RemoteApp-Sitzungen für eine Sammlung auf.

## Syntax

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRemoteAppSession** " listet alle aktiven und getrennten Azure RemoteApp-Sitzungen für eine Azure RemoteApp-Sammlung auf.

## Beispiele

### Beispiel 1: Auflisten aller Sitzungen in einer Sammlung
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

Dieser Befehl listet alle Sitzungen in der Azure RemoteApp-Sammlung mit dem Namen "ContosoApps" auf.

## Parameter

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
Gibt den Benutzerprinzipalnamen (User Principal Name, UPN) eines Benutzers an, für den Azure RemoteApp-Sitzungen abgerufen werden sollen.
Der UPN kann Beispiels PattiFuller@contoso.com Weise folgendes Format aufweisen:

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Trennen-AzureRemoteAppSession](./Disconnect-AzureRemoteAppSession.md)

[Invoke-AzureRemoteAppSessionLogoff](./Invoke-AzureRemoteAppSessionLogoff.md)

[Senden-AzureRemoteAppSessionMessage](./Send-AzureRemoteAppSessionMessage.md)


