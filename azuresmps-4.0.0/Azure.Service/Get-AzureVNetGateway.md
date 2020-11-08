---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4024D20D-46DF-4ED8-A091-E6E17F840E40
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c6ba8827906fbfc51b121e4500dea3ec4555d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006485"
---
# Get-AzureVNetGateway

## Synopsis
Ruft den Status eines virtuellen Netzwerkgateways ab.

## Syntax

```
Get-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureVNetGateway** " Ruft den Status eines vorhandenen virtuellen Netzwerkgateways ab.

## Beispiele

### Beispiel 1: Abrufen des Status eines virtuellen Netzwerkgateways
```
PS C:\> Get-AzureVNetGateway -VNetName "ContosoVN07"
```

Dieser Befehl ruft diesen Status des virtuellen Netzwerkgateways für das virtuelle Netzwerk mit dem Namen ContosoVN07 ab.

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
Gibt das virtuelle Netzwerk an, das das virtuelle Netzwerkgateway enthält, für das dieses Cmdlet den Status erhält.

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

[Neu – AzureVNetGateway](./New-AzureVNetGateway.md)

[Remove-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Größe ändern – AzureVNetGateway](./Resize-AzureVNetGateway.md)

[Satz-AzureVNetGatewayKey](./Set-AzureVNetGatewayKey.md)


