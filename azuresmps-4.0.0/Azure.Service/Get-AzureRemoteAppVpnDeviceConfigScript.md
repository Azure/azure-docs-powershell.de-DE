---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D0E8B2BD-D68F-477A-9D66-C27AB737960D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59423aa3de5ae91abe82090054fac61f3901363c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005831"
---
# Get-AzureRemoteAppVpnDeviceConfigScript

## Synopsis
Ruft das Konfigurationsskript für ein Azure RemoteApp-VPN-Gerät ab.

## Syntax

```
Get-AzureRemoteAppVpnDeviceConfigScript [-VNetName] <String> [-Vendor] <String> [-Platform] <String>
 [-OSFamily] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRemoteAppVpnDeviceConfigScript** " Ruft das Konfigurationsskript für ein Azure RemoteApp-VPN-Gerät (virtuelles privates Netzwerk) ab.

## Beispiele

### Beispiel 1: Abrufen eines Konfigurationsskripts für ein VPN-Gerät
```
PS C:\> Get-AzureRemoteAppVpnDeviceConfigScript -VNetName "ContosoVNet" -Vendor "Microsoft Corporation" -OSFamily "Windows Server 2012 R2"
```

Dieser Befehl gibt das Skript oder die Konfigurationsdatei zurück, das zum Konfigurieren des VPN-Geräts für das virtuelle Netzwerk mit dem Namen ContosoVNet verwendet wird.
Diese Skript-oder Konfigurationsdatei sollte auf das VPN-Gerät auf die übliche Weise für dieses Gerät ausgeführt oder geladen werden.
Erkundigen Sie sich beim Hersteller des VPN-Geräts nach den eindeutigen Anforderungen für die einzelnen Geräte.

## Parameter

### -Einstellung osfamily
Gibt die Betriebssystemfamilie an, die auf der Geräteplattform ausgeführt wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Plattform
Gibt die Geräteplattform an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
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

### -Vendor
Gibt den Anbieter des VPN-Geräts an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VNetName
Gibt den Namen eines virtuellen Azure RemoteApp-Netzwerks an.

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

## Verwandte Links

[Get-AzureRemoteAppVpnDevice](./Get-AzureRemoteAppVpnDevice.md)


