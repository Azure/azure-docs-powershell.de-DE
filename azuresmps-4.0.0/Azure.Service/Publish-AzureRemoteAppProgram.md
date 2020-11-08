---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F101382E-B015-4913-B4A0-8827EC423319
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37c4bf3ad2c2aaf74f268b18d17b6af71f4f2fc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006090"
---
# Publish-AzureRemoteAppProgram

## Synopsis
Veröffentlicht ein Azure RemoteApp-Programm.

## Syntax

### APP-ID (Standard)
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-StartMenuAppId] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### App-Pfad
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-FileVirtualPath] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Publish-AzureRemoteAppProgram** veröffentlicht ein Azure RemoteApp-Programm, das für Benutzer der Azure RemoteApp-Sammlung verfügbar ist.

## Beispiele

### Beispiel 1: Veröffentlichen eines Programms in einer Sammlung
```
PS C:\> Publish-AzureRemoteAppProgram -CollectionName "ContosoApps" -StartMenuAppId "a3732322-89a5-4cbc-9844-9634c74d337f" -DisplayName "Finance App"
```

Dieser Befehl veröffentlicht das Programm in der ContosoApps-Sammlung mit dem angegebenen *StartMenuAppId* , um das Programm zum Startmenü hinzuzufügen.
Die veröffentlichte APP hat den Anzeigenamen "Finance-App".

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

### -CommandLine
Gibt Befehlszeilenargumente für das Programm an, das dieses Cmdlet veröffentlicht.

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

### -DisplayName
Gibt den benutzerfreundlichen Anzeigenamen des Azure RemoteApp-Programms an.
Benutzer sehen dies als den Namen der Anwendung.

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

### -Filevirtualpath
Gibt den Pfad des Programms innerhalb des Vorlagenbilds des Programms an.

```yaml
Type: String
Parameter Sets: App Path
Aliases: 

Required: True
Position: 2
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

### -StartMenuAppId
Gibt eine GUID an, die dieses Cmdlet verwendet, um das Programm dem Startmenü hinzuzufügen.

```yaml
Type: String
Parameter Sets: App Id
Aliases: 

Required: True
Position: 2
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

[Get-AzureRemoteAppProgram](./Get-AzureRemoteAppProgram.md)

[Veröffentlichung aufheben – AzureRemoteAppProgram](./Unpublish-AzureRemoteAppProgram.md)


