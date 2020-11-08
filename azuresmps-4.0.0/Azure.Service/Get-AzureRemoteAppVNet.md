---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006776"
---
# Get-AzureRemoteAppVNet

## Synopsis
Ruft Informationen zu Azure RemoteApp-virtuellen Netzwerken in Azure ab.

## Syntax

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRemoteAppVNet** " Ruft Informationen zu virtuellen Azure RemoteApp-Netzwerken in Microsoft Azure ab.
Dieses Cmdlet gibt ein Objekt zurück, das Informationen zu einem angegebenen virtuellen Netzwerk enthält.
Wenn kein virtuelles Netzwerk angegeben ist, gibt dieses Cmdlet Informationen zu allen virtuellen Netzwerken im aktuellen Abonnement zurück.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu einem virtuellen Netzwerk
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

Dieser Befehl ruft Informationen über das virtuelle Netzwerk mit dem Namen ContosoVNet ab.

## Parameter

### -IncludeSharedKey
Gibt an, dass dieses Cmdlet den Wert des freigegebenen Schlüssels in den Informationen enthält, die er über das virtuelle Netzwerk abruft.

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

### -VNetName
Gibt den Namen des virtuellen Azure RemoteApp-Netzwerks an.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Satz-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


