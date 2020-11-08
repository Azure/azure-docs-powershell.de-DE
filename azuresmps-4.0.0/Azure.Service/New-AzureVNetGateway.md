---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006393"
---
# New-AzureVNetGateway

## Synopsis
Erstellt ein VPN-Gateway in einem virtuellen Netzwerk.

## Syntax

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzureVNetGateway** wird ein VPN-Gateway (virtuelles privates Netzwerk) in einem virtuellen Netzwerk erstellt.
Sie können auch die SKU des Gateways angeben, entweder Standard, Standard oder leistungsfähige.
Sie können den Typ angeben, entweder StaticRouting oder DynamicRouting.

## Beispiele

### Beispiel 1: Erstellen eines virtuellen Netzwerkgateways
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

Dieser Befehl erstellt ein virtuelles Netzwerkgateway für das virtuelle Netzwerk mit dem Namen ContosoVN07.
Das Gateway ist die Standard-SKU und verwendet dynamisches Routing.

## Parameter

### -GatewaySKU
Gibt die SKU des vom Cmdlet erstellten virtuellen Netzwerkgateways an.
Gültige Werte sind: 

- Standard 
- Standard 
- Hochleistungs

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

### -Gatewaytype
Gibt den Typ des Gateways an, das von diesem Cmdlet erstellt wird.
Gültige Werte sind: 

- StaticRouting 
- DynamicRouting

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
Gibt das virtuelle Netzwerk an, in dem mit diesem Cmdlet ein virtuelles Netzwerkgateway hinzugefügt wird.

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

[Remove-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Größe ändern – AzureVNetGateway](./Resize-AzureVNetGateway.md)

[Satz-AzureVNetGatewayKey](./Set-AzureVNetGatewayKey.md)


