---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006257"
---
# Set-AzureRemoteAppWorkspace

## Synopsis
Legt die Eigenschaften eines Azure RemoteApp-Arbeitsbereichs fest.

## Syntax

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureRemoteAppWorkspace** " legt die Eigenschaften eines Azure RemoteApp-Arbeitsbereichs fest.

## Beispiele

### Beispiel 1: Einrichten des Arbeitsbereichs namens
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

Mit diesem Befehl wird der Azure RemoteApp-Arbeitsbereichsname auf contoso-Arbeitsanwendungen festgelegt.

## Parameter

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

### -WorkspaceName
Gibt den Namen des Azure RemoteApp-Arbeitsbereichs an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen
* Alle Azure RemoteApp-Auflistungen für ein angegebenes Abonnement sind in einem freigegebenen Arbeitsbereich vorhanden.

## Verwandte Links

[Get-AzureRemoteAppWorkspace](./Get-AzureRemoteAppWorkspace.md)


