---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 947D1C09-7CFA-4E97-A6B3-2DA9D7507F0C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0260b452c96b5f6dd60599b5da15cc323b5423d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006469"
---
# Get-WAPackVNet

## Synopsis
Ruft virtuelle Netzwerke ab.

## Syntax

### Leer (Standard)
```
Get-WAPackVNet [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromId
```
Get-WAPackVNet -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVNet -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-WAPackVNet** " ruft virtuelle Netzwerke ab.

## Beispiele

### Beispiel 1: Abrufen aller virtuellen Netzwerke
```
PS C:\> Get-WAPackVNet
```

Dieser Befehl ruft alle virtuellen Netzwerke ab.

### Beispiel 2: Abrufen eines virtuellen Netzwerks mithilfe einer ID
```
PS C:\> Get-WAPackVNet -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

Dieser Befehl ruft das virtuelle Netzwerk ab, das die angegebene ID hat.

### Beispiel 3: Abrufen eines virtuellen Netzwerks mithilfe eines Namens
```
PS C:\> Get-WAPackVNet -Name "ContosoVNet08"
```

Dieser Befehl ruft das virtuelle Netzwerk mit dem Namen ContosoVNet08 ab.

## Parameter

### -ID
Gibt die eindeutige ID eines virtuellen Netzwerks an.

```yaml
Type: Guid
Parameter Sets: FromId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen eines virtuellen Netzwerks an.

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: True
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

