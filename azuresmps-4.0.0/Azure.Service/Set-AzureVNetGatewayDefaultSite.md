---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006619"
---
# Set-AzureVNetGatewayDefaultSite

## Synopsis
Legt die Standardwebsite für erzwungenen Tunneling-Datenverkehr fest.

## Syntax

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureVNetGatewayDefaultSite** " legt die Standardroute zur lokalen Website für erzwungenen Tunneling-Datenverkehr fest.
Dieser Befehl legt die Route auf einem Azure Virtual Private Network (VPN)-Gateway für ein virtuelles Netzwerk fest.

## Beispiele

## Parameter

### -DefaultSite
Gibt den Namen der lokalen lokalen Netzwerk Website für erzwungenen Tunneling-Datenverkehr an.

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
Gibt ein virtuelles Netzwerk an.
Mit diesem Cmdlet wird die Standardroute des VPN-Gateways für erzwungenen Tunneling-Datenverkehr für das virtuelle Netzwerk festgelegt, das dieser Parameter angibt.

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

[Remove-AzureVNetGatewayDefaultSite](./Remove-AzureVNetGatewayDefaultSite.md)
