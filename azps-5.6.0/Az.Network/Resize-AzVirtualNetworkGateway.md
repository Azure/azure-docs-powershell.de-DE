---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: 4b2963d77d2182821bb4950907ef278950e410f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921691"
---
# Resize-AzVirtualNetworkGateway

## SYNOPSIS
Ändert die Größe eines vorhandenen Gateways für virtuelle Netzwerke.

## SYNTAX

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Mit **dem Cmdlet Resize-AzVirtualNetworkGateway** können Sie die SKU (Stock-Keeping Unit) für ein Gateway für virtuelle Netzwerke ändern.
SKUs bestimmen die Funktionen eines Gateways, z. B. den Durchsatz und die maximale Anzahl zulässiger IP-Tunnel.
Azure unterstützt Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (manchmal auch als kleine, mittlere und große SKUs bezeichnet).
Ausführliche Informationen zu den Funktionen der einzelnen SKU-Typen finden Sie unter https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .
Beachten Sie, dass SKUs sich in der Preisgestaltung sowie in den Funktionen unterscheiden.
Weitere Informationen finden Sie unter https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## BEISPIELE

### Beispiel 1: Ändern der Größe eines Gateways für virtuelle Netzwerke
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

In diesem Beispiel wird die Größe eines Virtuellen Netzwerkgateways namens ContosoVirtualGateway geändert.
Mit dem ersten Befehl wird ein Objektverweis auf ContosoVirtualGateway erstellt. Dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway.
Der zweite Befehl verwendet dann **das Cmdlet Resize-AzVirtualNetworkGateway,** um die *GatewaySku-Eigenschaft* auf Basic zu setzen.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewaySku
Gibt den neuen Typ der Gateway-SKU an.
Die zulässigen Werte für diesen Parameter sind:
- Basic
- Standard
- Hohe Leistung
- VpnGw1
- VpnGw2
- VpnGw3
- VpnGw1AZ 
- VpnGw2AZ 
- VpnGw3AZ 
- ErGw1AZ 
- ErGw2AZ 
- ErGw3AZ 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, dessen Größe geändert werden soll.
Sie können diesen Objektverweis erstellen, indem Sie Get-AzVirtualNetworkGateway und den Namen des Gateways angeben.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## NOTIZEN
Sie können die Größe nicht von Basic/Standard/HighPerformance SKUs auf die neuen VPNGw1/VpnGw2/VpnGw3-SKUs ändern. Eine weitere Größenänderung ist von/zu VpnGw1AZ/VpnGw2AZ/VpnGw3AZ oder ErGw1AZ/ErGw2AZ/ErGw3AZ nicht zulässig. Die Größe der Größe ist nur innerhalb der SKU-Serie zulässig, z. B. kann vpnGw1AZ in/von VpnGw2AZ/VpnGw3AZ geändert werden, und ErGw1AZ kann die Größe in/von ErGw2AZ/ErGw3AZ geändert werden. Anweisungen https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways finden Sie unter.

## VERWANDTE LINKS

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[New-AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[Reset-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
