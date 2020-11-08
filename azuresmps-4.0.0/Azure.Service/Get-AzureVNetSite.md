---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CFAA371E-F320-4FC3-80E0-5C857E5C0998
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fbb80550acb0c743a3134a315f790bc25fb793a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006733"
---
# Get-AzureVNetSite

## Synopsis
Ruft ein Listenobjekt mit Informationen zu Azure Virtual Networks ab.

## Syntax

```
Get-AzureVNetSite [[-VNetName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureVNetSite** " Ruft ein Listenobjekt mit Informationen zu Azure Virtual Networks für das aktuelle Abonnement ab.
Wenn Sie einen virtuellen Netzwerknamen angeben, werden nur Informationen für dieses virtuelle Netzwerk zurückgegeben.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu allen virtuellen Netzwerken im aktuellen Abonnement
```
PS C:\> Get-AzureVNetSite
```

Dieser Befehl ruft Informationen zu allen virtuellen Netzwerken im aktuellen Abonnement ab.

### Beispiel 2: Abrufen von Informationen zu einem bestimmten virtuellen Netzwerk im aktuellen Abonnement
```
PS C:\> Get-AzureVNetSite -VNetName "MyProductionNetwork"
```

Dieser Befehl ruft nur Informationen im virtuellen MyProductionNetwork-Netzwerk ab.

## Parameter

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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
Gibt einen virtuellen Netzwerknamen an, zu dem Informationen zurückgegeben werden sollen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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

[Get-AzureVNetConfig](./Get-AzureVNetConfig.md)

[Remove-AzureVNetConfig](./Remove-AzureVNetConfig.md)

[Satz-AzureVNetConfig](./Set-AzureVNetConfig.md)


