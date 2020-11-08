---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005695"
---
# Remove-AzureVNetGatewayDefaultSite

## Synopsis
Entfernt die Standardroute für erzwungenen Tunneling-Datenverkehr.

## Syntax

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureVNetGatewayDefaultSite** entfernt die Standardroute zur lokalen Website für erzwungenen Tunneling-Datenverkehr.
Dieses Cmdlet entfernt die Route von einem Azure Virtual Private Network (VPN)-Gateway für ein virtuelles Netzwerk.

## Beispiele

### Beispiel 1: Entfernen einer Route zur Standardwebsite
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

Dieser Befehl entfernt die Route zur Standardwebsite aus dem VPN des virtuellen Netzwerks mit dem Namen ContosoVNet01.

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
Gibt ein virtuelles Netzwerk an.
Dieses Cmdlet entfernt die Standardroute aus dem VPN-Gateway für das virtuelle Netzwerk, das dieser Parameter angibt.

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

[Satz-AzureVNetGatewayDefaultSite](./Set-AzureVNetGatewayDefaultSite.md)
