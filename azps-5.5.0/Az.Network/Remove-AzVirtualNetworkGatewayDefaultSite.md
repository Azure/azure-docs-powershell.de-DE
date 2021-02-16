---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146705"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Entfernt die Standardwebsite aus einem virtuellen Netzwerkgateway.

## SYNTAX

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Remove-AzVirtualNetworkGatewayDefaultSite"** entfernt die Standardwebsite mit erzwungenen Tunneln von einem virtuellen Netzwerkgateway.
Erzwungenes Tunneln bietet Ihnen die Möglichkeit, internetgebundenen Datenverkehr von virtuellen #A0 an Ihr lokales Netzwerk umzuleiten. auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.
Erzwungenes Tunneln wird mithilfe eines VPN (Virtual Private Network)-Tunnels durchgeführt. dieser Tunnel erfordert eine Standardwebsite, also ein lokales Gateway, an das der internetgebundene Azure-Datenverkehr umgeleitet wird.
**Remove-AzVirtualNetworkGatewayDefaultSite** entfernt die einem Gateway zugewiesene Standardwebsite.
Wenn Sie dies tun, müssen Sie Set-AzVirtualNetworkGatewayDefaultSite verwenden, um eine neue Standardwebsite zuzuordnen, bevor das Gateway für erzwungenes Tunneln verwendet werden kann.

## BEISPIELE

### Beispiel 1: Entfernen der einem virtuellen Netzwerkgateway zugewiesenen Standardwebsite
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

In diesem Beispiel wird die Standardwebsite entfernt, die derzeit einem virtuellen Netzwerkgateway namens "ContosoVirtualGateway" zugewiesen ist.
Der erste Befehl verwendet **"Get-AzVirtualNetworkGateway",** um einen Objektverweis auf das Gateway zu erstellen. objektverweis wird in einer Variablen mit dem Namen $Gateway.
Der zweite Befehl verwendet dann **"Remove-AzVirtualNetworkGatewayDefaultSite",** um die diesem Gateway zugewiesene Standardwebsite zu entfernen.

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

### -VirtualNetworkGateway
Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, das die zu entfernende Standardwebsite enthält.
Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie Get-AzVirtualNetworkGateway und den Namen des Gateways angeben.

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

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


