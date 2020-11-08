---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 895F9A5F-D48F-403D-BD8F-72D72D420690
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97bb3e07f5c6df25e7c03c167cc4cb49c25f9414
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005993"
---
# Set-AzureVNetConfig

## Synopsis
Aktualisiert die Einstellungen für das virtuelle Netzwerk für einen Azure Cloud-Dienst.

## Syntax

```
Set-AzureVNetConfig [-ConfigurationPath] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureVNetConfig** " aktualisiert die Netzwerkkonfiguration für das aktuelle Azure-Abonnement, indem Sie einen Pfad zu einer Netzwerk Konfigurationsdatei (. netcfg) angeben.
Die Netzwerk Konfigurationsdatei definiert DNS-Server und-Subnetze für Cloud-Dienste in einem Abonnement.

## Beispiele

### Beispiel 1: Aktualisieren der Netzwerkkonfiguration des Azure-Abonnements auf eine lokale Datei
```
PS C:\> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

Mit diesem Befehl wird die Netzwerkkonfiguration des aktuellen Microsoft Azure-Abonnements in der lokalen Datei "c:\temp\MyAzNets.netcfg" aktualisiert.

### Beispiel 2: Einrichten des Azure-Abonnements und anschließendes Aktualisieren der Netzwerkkonfiguration
```
PS C:\> $SubsId = "5bea2bc2-88a5-44b8-abe1-3e76733b6783"
C:\PS> $Cert = Get-Item cert:\LocalMachine\MY\82F105B2DA81149204A6257A9A91EC452B8C52C3
C:\PS> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

In diesem Beispiel wird das Microsoft Azure-Abonnement festgelegt, und dann wird die Netzwerkkonfiguration dieses Abonnements unter Verwendung der Konfiguration aktualisiert, die in der lokalen Datei "c:\temp\MyAzNets.netcfg" definiert ist.

## Parameter

### -ConfigurationPath
Gibt den Pfad und den Dateinamen einer Netzwerk Konfigurationsdatei an (netcfg).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

[Get-AzureVNetConfig](./Get-AzureVNetConfig.md)

[Get-AzureVNetSite](./Get-AzureVNetSite.md)

[Remove-AzureVNetConfig](./Remove-AzureVNetConfig.md)


