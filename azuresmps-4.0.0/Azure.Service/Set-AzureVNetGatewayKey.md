---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006016"
---
# Set-AzureVNetGatewayKey

## Synopsis
Legt den vor-freigegebenen Schlüssel für die Verbindung zwischen einem Azure VPN-Gateway und einer lokalen Netzwerk Website fest.

## Syntax

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Set-AzureVNetGatewayKey** wird der vorinstallierte Schlüssel für die Verbindung zwischen einem Azure Virtual Private Network (VPN)-Gateway und einer lokalen lokalen Netzwerk Website festgelegt.
Der Schlüssel muss mit dem auf dem Gateway der lokalen Netzwerk Website konfigurierten Schlüssel identisch sein.
Wenn die Schlüssel nicht übereinstimmen, kann eine Verbindung nicht hergestellt werden.

## Beispiele

## Parameter

### -LocalNetworkSiteName
Gibt den Namen der lokalen Netzwerk Website an, die eine Verbindung mit dem virtuellen Netzwerkgateway herstellt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest. Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

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

### -SharedKey
Gibt den freigegebenen Schlüssel an, der dem VPN-Gateway zugewiesen werden soll.
Der Wert muss eine alphanumerische Zeichenfolge nicht mehr als 128 Zeichen sein.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Gibt das virtuelle Netzwerk an, für das dieses Cmdlet den freigegebenen Schlüssel für die Verbindung festlegt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

[Get-AzureVNetGatewayKey](./Get-AzureVNetGatewayKey.md)


