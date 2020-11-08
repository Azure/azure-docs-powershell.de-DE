---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006535"
---
# Get-AzureRemoteAppCollection

## Synopsis
Ruft Informationen zu einer Azure RemoteApp-Sammlung ab.

## Syntax

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRemoteAppCollection** " Ruft Informationen zu Azure RemoteApp-Auflistungen in Microsoft Azure ab.
Sie gibt ein Objekt zurück, das Informationen zu einer bestimmten Sammlung enthält, oder wenn für alle Auflistungen im aktuellen Abonnement keine Sammlung angegeben ist.

## Beispiele

### Beispiel 1: Abrufen einer Liste aller Auflistungen
```
PS C:\> Get-AzureRemoteAppCollection
```

Dieser Befehl gibt eine Liste aller Azure RemoteApp-Auflistungen im Abonnement zurück.

### Beispiel 2: Abrufen von Informationen zu einer angegebenen Sammlung
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

Dieser Befehl gibt Informationen zur Azure RemoteApp-Sammlung mit dem Namen "ContosoApps" zurück.

### Beispiel 3: Abrufen einer Liste von Auflistungen mit einem Platzhalter
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

Dieser Befehl gibt eine Liste aller Azure RemoteApp-Auflistungen zurück, die auf Finance * abgestimmt sind.

## Parameter

### -CollectionName
Gibt den Namen der Azure RemoteApp-Sammlung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
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

[Neu – AzureRemoteAppCollection](./New-AzureRemoteAppCollection.md)

[Remove-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Satz-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


