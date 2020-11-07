---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 0a3dea2b706f7efcdc76b48175df225e2974728c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850596"
---
# Resize-AzureRmVirtualNetworkGateway

## Synopsis
Ändert die Größe eines vorhandenen virtuellen Netzwerkgateways.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **size-AzureRmVirtualNetworkGateway** können Sie die Lagerhaltungs Einheit (SKU) für ein virtuelles Netzwerkgateway ändern.
SKUs ermitteln die Funktionen eines Gateways, beispielsweise den Durchsatz und die maximal zulässige Anzahl von IP-Tunneln.
Azure unterstützt Basis-, Standard-, Hochleistungs-, VpnGw1-, VpnGw2-und VpnGw3-SKUs (manchmal auch als kleine, mittlere und große SKUs bezeichnet).
Ausführliche Informationen zu den Funktionen der einzelnen SKU-Typen finden Sie unter https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .

Beachten Sie, dass sich die SKUs in der Preis-und Leistungsfähigkeit unterscheiden.
Weitere Informationen finden Sie unter https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## Beispiele

### Beispiel 1: Ändern der Größe eines virtuellen Netzwerkgateways
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

In diesem Beispiel wird die Größe eines virtuellen Netzwerkgateways mit dem Namen ContosoVirtualGateway geändert.

Der erste Befehl erstellt einen Objektverweis auf ContosoVirtualGateway; dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway gespeichert.

Der zweite Befehl verwendet dann das Cmdlet **size-AzureRmVirtualNetworkGateway** , um die *GatewaySku* -Eigenschaft auf Basic zu setzen.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewaySku
Gibt den neuen Typ der Gateway-SKU an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Grundlegende
- Standard
- Höchstleistung
- VpnGw1
- VpnGw2
- VpnGw3

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, dessen Größe geändert werden soll.
Sie können diesen Objektverweis mithilfe der Get-AzureRmVirtualNetworkGateway erstellen und den Namen des Gateways angeben.

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

###  
Dieses Cmdlet akzeptiert Pipelineinstanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.

## Ausgaben

###  
Dieses Cmdlet ändert vorhandene Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.

## Notizen
Sie können die Größe nicht von Basic/Standard/Performance-SKUs auf die neue VpnGw1/VpnGw2/VpnGw3-SKUs ändern. Anweisungen hierzu finden Sie unter https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways .

## Verwandte Links

[Get-AzureRmVpnClientPackage](./Get-AzureRmVpnClientPackage.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Satz-AzureRmVirtualNetworkGatewayVpnClientConfig](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


