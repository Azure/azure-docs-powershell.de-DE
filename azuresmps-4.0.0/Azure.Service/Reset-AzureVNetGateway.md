---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B4102F33-979B-4649-99F4-96A295EAE43C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ddb0ac79f5164fb5c953dd1cf1efeff8391d30fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005671"
---
# Reset-AzureVNetGateway

## Synopsis
Setzt ein virtuelles Netzwerk-VPN-Gateway zurück.

## Syntax

```
Reset-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Reset-AzureVNetGateway** wird ein virtuelles privates Netzwerk (virtuelles privates Netzwerk)-virtuelles Netzwerk-Gateway zurückgesetzt und neu gestartet.

## Beispiele

### Beispiel 1: Zurücksetzen eines virtuellen Netzwerkgateways
```
PS C:\> Reset-AzureVNetGateway -VNetName "ContosoVN07"
```

Mit diesem Befehl wird das virtuelle Netzwerkgateway aus dem virtuellen Netzwerk mit dem Namen ContosoVN07 zurückgesetzt.

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
Gibt das virtuelle Netzwerk an, das das virtuelle Netzwerkgateway enthält, das von diesem Cmdlet zurückgesetzt wird.

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

[Größe ändern – AzureVNetGateway](./Resize-AzureVNetGateway.md)

[Satz-AzureVNetGatewayKey](./Set-AzureVNetGatewayKey.md)


