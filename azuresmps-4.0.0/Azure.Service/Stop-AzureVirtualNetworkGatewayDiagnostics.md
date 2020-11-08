---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9E7A170D-512A-4117-85C3-3AA4D6341C6B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97fe847fd183caa7de281b358da579e8df4d5831
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005946"
---
# Stop-AzureVirtualNetworkGatewayDiagnostics

## Synopsis
Unterbricht die Ausführung einer virtuellen Netzwerkgateway-Diagnosesitzung.

## Syntax

```
Stop-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Stop-AzureVirtualNetworkGatewayDiagnostics** beendet die Ausführung einer virtuellen Netzwerk-Gateway-Diagnosesitzung.
Dieser Befehl speichert die Ergebnisse der Diagnosesitzung in dem Speicherkonto, das vom Start-AzureVirtualNetworkGatewayDiagnostics-Cmdlet angegeben wird.

## Beispiele

## Parameter

### -Gatewayserver
Gibt die ID eines Gateways an.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureVirtualNetworkGatewayDiagnostics](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[Anfang-AzureVirtualNetworkGatewayDiagnostics](./Start-AzureVirtualNetworkGatewayDiagnostics.md)


