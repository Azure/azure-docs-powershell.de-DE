---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006293"
---
# Resize-AzureVNetGateway

## Synopsis
Ändert die Größe eines VPN-Gateways.

## Syntax

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **size-AzureVNetGateway** wird die Größe eines virtuellen VPN-Gateways (virtuelles privates Netzwerk) auf eine andere SKU geändert.
Gültige SKUs für ein virtuelles Netzwerkgateway sind Standard, Standard und leistungsfähige.

## Beispiele

### Beispiel 1: Ändern der SKU für ein virtuelles Netzwerkgateway
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

Mit diesem Befehl wird die SKU des virtuellen Netzwerkgateways für das virtuelle Netzwerk mit dem Namen ContosoVN07 in leistungsfähige geändert.

## Parameter

### -GatewaySKU
Gibt die SKU an, für die dieses Cmdlet die Größe des virtuellen Netzwerkgateways ändert.
Gültige Werte sind: 

- Standard 
- Standard 
- Hochleistungs

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

### -VNetName
Gibt das virtuelle Netzwerk an, in dem dieses Cmdlet die Größe eines virtuellen Netzwerkgateways ändert.

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

[Remove-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Satz-AzureVNetGatewayKey](./Set-AzureVNetGatewayKey.md)


