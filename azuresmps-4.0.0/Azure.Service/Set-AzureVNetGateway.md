---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006620"
---
# Set-AzureVNetGateway

## Synopsis
Aktiviert oder deaktiviert ein VPN-Gateway für ein Azure-virtuelles Netzwerk.

## Syntax

### Verbinden (Standard)
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Trennen
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureVNetGateway** " aktiviert oder deaktiviert ein VPN-Gateway (virtuelles privates Netzwerk) für ein Azure-virtuelles Netzwerk.
Ein virtuelles Netzwerkgateway ist ein VPN-Endpunkt zum Herstellen einer Verbindung mit einem virtuellen Netzwerk.
Geben Sie den Parameter *Connect* oder *Disconnect* an, um die VPN-Verbindung zwischen einer lokalen lokalen Netzwerk Website und einem virtuellen Netzwerk zu aktivieren oder zu deaktivieren.

## Beispiele

### Beispiel 1: Aktivieren eines virtuellen Netzwerkgateways für ein virtuelles Netzwerk
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Mit diesem Befehl wird das virtuelle Netzwerkgateway zwischen dem virtuellen Azure-Netzwerk mit dem Namen ContosoProdNet und dem VPN-Gerät für die lokale Netzwerk Website mit dem Namen ContosoBranchOffice aktiviert.

### Beispiel 2: Deaktivieren eines virtuellen Netzwerkgateways für ein virtuelles Netzwerk
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Mit diesem Befehl wird das virtuelle Netzwerkgateway zwischen dem virtuellen Azure-Netzwerk mit dem Namen ContosoProdNet und dem VPN-Gerät für die lokale Netzwerk Website mit dem Namen ContosoBranchOffice deaktiviert.

## Parameter

### -Connect
Gibt an, dass dieses Cmdlet die VPN-Verbindung zwischen einem virtuellen Netzwerk und einer lokalen Netzwerk Website aktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Trennen
Gibt an, dass dieses Cmdlet die VPN-Verbindung zwischen einem virtuellen Netzwerk und einer lokalen Netzwerk Website deaktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalNetworkSiteName
Gibt den Namen der lokalen lokalen Netzwerk Website an, für die dieses Cmdlet die VPN-Verbindung aktiviert oder deaktiviert.

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
Gibt das virtuelle Netzwerk an, für das dieses Cmdlet die VPN-Verbindung aktiviert oder deaktiviert.

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

[Größe ändern – AzureVNetGateway](./Resize-AzureVNetGateway.md)


