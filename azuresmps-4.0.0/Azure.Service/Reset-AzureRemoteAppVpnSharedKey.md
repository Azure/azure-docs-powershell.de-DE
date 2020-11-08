---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4522E93F-6AC9-4A37-88B8-CCCCE15A5879
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcfc41e06f6847612c275817560e8593b76f6bac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005677"
---
# Reset-AzureRemoteAppVpnSharedKey

## Synopsis
Der freigegebene Azure RemoteApp-VPN-Schlüssel wird zurückgesetzt.

## Syntax

```
Reset-AzureRemoteAppVpnSharedKey [-VNetName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Reset-AzureRemoteAppVpnSharedKey** wird der freigegebene Schlüssel Azure RemoteApp-VPN (virtuelles privates Netzwerk) zurückgesetzt.

## Beispiele

### Beispiel 1: Zurücksetzen des freigegebenen Schlüssels in einem virtuellen Netzwerk
```
PS C:\> Reset-AzureRemoteAppVpnSharedKey -VNetName "ContosoVNet"
```

Mit diesem Befehl wird der freigegebene Schlüssel im virtuellen Netzwerk mit dem Namen ContosoVNet zurückgesetzt.
Die VPN-Verbindung mit dem lokalen Netzwerk bleibt offline, bis der neue freigegebene Schlüssel auf dem VPN-Gerät konfiguriert ist.
Verwenden Sie zum Konfigurieren des VPN-Geräts das Cmdlet " **Get-AzureRemoteAppVpnDeviceConfigScript** ", um das richtige Skript oder die richtige Konfigurationsdatei für Ihr VPN-Gerät abzurufen, und laden Sie dann das Skript oder die Konfigurationsdatei auf das VPN-Gerät.

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

### -VNetName
Gibt den Namen des virtuellen Azure RemoteApp-Netzwerks an.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### System. String

## Notizen

## Verwandte Links

[Get-AzureRemoteAppVNet](./Get-AzureRemoteAppVNet.md)

[Get-AzureRemoteAppVpnDeviceConfigScript](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


