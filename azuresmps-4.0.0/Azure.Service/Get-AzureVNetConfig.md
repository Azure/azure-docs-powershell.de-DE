---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F34910FA-B024-4C1C-B040-671C8962C49D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 558d714c432efd1dbd8f11feb09b0bbde035e2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006494"
---
# Get-AzureVNetConfig

## Synopsis
Ruft die Azure Virtual Network-Konfiguration aus dem aktuellen Abonnement ab.

## Syntax

```
Get-AzureVNetConfig [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureVNetConfig** " Ruft die virtuelle Netzwerkkonfiguration des aktuellen Azure-Abonnements ab.
Wenn der Parameter *ExportToFile* angegeben wird, wird eine Netzwerk Konfigurationsdatei erstellt.

## Beispiele

### Beispiel 1: Abrufen der virtuellen Netzwerkkonfiguration eines aktuellen Azure-Abonnements
```
PS C:\> Get-AzureVNetConfig
```

Mit diesem Befehl wird die virtuelle Netzwerkkonfiguration des aktuellen Azure-Abonnements abgerufen und angezeigt.

### Beispiel 2: Abrufen der virtuellen Netzwerkkonfiguration des aktuellen Azure-Abonnements und speichern in einer lokalen Datei
```
PS C:\> Get-AzureVNetConfig -ExportToFile "c:\temp\MyAzNets.netcfg"
```

Mit diesem Befehl wird die virtuelle Netzwerkkonfiguration des aktuellen Azure-Abonnements abgerufen und dann in einer lokalen Datei gespeichert.

## Parameter

### -ExportToFile
Gibt den Pfad und den Dateinamen einer Netzwerk Konfigurationsdatei an, die aus den Einstellungen erstellt werden soll.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureVNetSite](./Get-AzureVNetSite.md)

[Remove-AzureVNetConfig](./Remove-AzureVNetConfig.md)

[Satz-AzureVNetConfig](./Set-AzureVNetConfig.md)


