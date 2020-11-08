---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005696"
---
# Remove-AzureVNetGateway

## Synopsis
Löscht ein VPN-Gateway.

## Syntax

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureVNetGateway** löscht ein vorhandenes virtuelles privates Netzwerk (VPN)-Gateway für ein virtuelles Netzwerk.

## Beispiele

### Beispiel 1: Entfernen eines virtuellen Netzwerkgateways
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

Dieser Befehl entfernt das virtuelle Netzwerkgateway aus dem virtuellen Netzwerk mit dem Namen ContosoVN07.

## Parameter

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

### -VNetName
Gibt das virtuelle Netzwerk an, in dem dieses Cmdlet das VPN-Gateway löscht.

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

[Get-AzureVNetGateway](./Get-AzureVNetGateway.md)

[Neu – AzureVNetGateway](./New-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Größe ändern – AzureVNetGateway](./Resize-AzureVNetGateway.md)

[Satz-AzureVNetGatewayKey](./Set-AzureVNetGatewayKey.md)


