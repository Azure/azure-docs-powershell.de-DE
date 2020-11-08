---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006785"
---
# Get-AzureRemoteAppTemplateImage

## Synopsis
Ruft Informationen zu Azure RemoteApp-Vorlagen Bildern ab.

## Syntax

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRemoteAppTemplateImage** " Ruft Informationen zu Azure RemoteApp-Vorlagen Bildern in Microsoft Azure ab.
Dieses Cmdlet gibt ein Objekt zurück, das Informationen zu einem angegebenen Vorlagenbild enthält.
Wenn kein Vorlagenbild angegeben ist, werden Informationen zu allen Vorlagen Bildern im aktuellen Abonnement abgerufen.

## Beispiele

### Beispiel 1: Abrufen einer Liste aller Vorlagen Bilder
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

Dieser Befehl gibt die Liste aller Vorlagen Bilder zurück.

### Beispiel 2: Abrufen von Informationen zu einem angegebenen Vorlagenbild
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

Dieser Befehl ruft Informationen zum Vorlagenbild mit dem Namen ContosoApps ab.

## Parameter

### -Bildname
Gibt den Namen eines Azure RemoteApp-Vorlagenbilds an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppStartMenuProgram](./Get-AzureRemoteAppStartMenuProgram.md)


