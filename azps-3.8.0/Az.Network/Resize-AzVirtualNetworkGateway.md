---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: 31ec0453b0ce64c27d1bb37d4bf6c0f100a8c760
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411754"
---
# Resize-AzVirtualNetworkGateway

## SYNOPSIS
Ändert die Größe eines vorhandenen virtuellen Netzwerkgateways.

## SYNTAX

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Mit **dem Cmdlet Resize-AzVirtualNetworkGateway** können Sie die SKU (Stock-Keeping Unit) für ein virtuelles Netzwerkgateway ändern.
SKUs bestimmen die Funktionen eines Gateways, z. B. Durchsatz und die maximale Anzahl zulässiger IP-Tunnel.
Azure unterstützt Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (manchmal auch als kleine, mittlere und große SKUs bezeichnet).
Ausführliche Informationen zu den Funktionen der einzelnen SKU-Typen finden Sie unter https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .
Bedenken Sie, dass skUs in der Preisgestaltung sowie in den Funktionen unterschiedlich sind.
Weitere Informationen finden Sie unter https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## BEISPIELE

### Beispiel 1: Ändern der Größe eines virtuellen Netzwerkgateways
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

In diesem Beispiel wird die Größe eines virtuellen Netzwerkgateways namens "ContosoVirtualGateway" geändert.
Der erste Befehl erstellt einen Objektverweis auf ContosoVirtualGateway. objektverweis wird in einer Variablen mit dem Namen $Gateway.
Der zweite Befehl verwendet dann das **Cmdlet Resize-AzVirtualNetworkGateway,** um die *Eigenschaft "GatewaySku"* auf "Basic" zu setzen.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -GatewaySKU
Gibt den neuen Typ der Gateway-SKU an.
Die zulässigen Werte für diesen Parameter sind:
- Standard
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## HINWEISE
Sie können die Größe nicht von Basic/Standard/HighPerformance-SKUs auf die neuen VPNGw1/VpnGw2/VpnGw3-SKUs ändern. Eine weitere Größenänderung ist von/zu VpnGw1AZ/VpnGw2AZ/VpnGw3AZ oder ErGw1AZ/ErGw2AZ/ErGw3AZ nicht zulässig. Die Größenänderung ist nur in der SKU-Serie zulässig, z. B. kann die Größe von VpnGw1AZ in VpnGw2AZ/VpnGw3AZ und von ErGw1AZ in/von ErGw2AZ/ErGw3AZ geändert werden. Anweisungen https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways finden Sie hier.

## LINKS ZU VERWANDTEN THEMEN

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[New-AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[Reset-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

