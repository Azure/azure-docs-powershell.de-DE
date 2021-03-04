---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: ddf0f6687550e544aa22efbce772c0751a7b810e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945838"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Entfernt die Standardwebsite aus einem Gateway für virtuelle Netzwerke.

## SYNTAX

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Remove-AzVirtualNetworkGatewayDefaultSite** entfernt die Standardwebsite für erzwungenes Tunneln aus einem Gateway für virtuelle Netzwerke.
Erzwungenes Tunneln bietet Ihnen die Möglichkeit, internetgebundenen Datenverkehr von virtuellen #A0 an Ihr lokales Netzwerk umzuleiten. Auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.
Erzwungenes Tunneln wird mithilfe eines VPN-Tunnels (Virtual Private Network) ausgeführt. Für diesen Tunnel ist eine Standardwebsite erforderlich, ein lokales Gateway, auf dem der internetgebundene Azure-Datenverkehr umgeleitet wird.
**Remove-AzVirtualNetworkGatewayDefaultSite** entfernt die Standardwebsite, die einem Gateway zugewiesen ist.
Wenn Sie dies tun, müssen Sie Set-AzVirtualNetworkGatewayDefaultSite verwenden, um eine neue Standardwebsite zuzuordnen, bevor das Gateway für erzwungenes Tunneln verwendet werden kann.

## BEISPIELE

### Beispiel 1: Entfernen der Standardwebsite, die einem Gateway für virtuelle Netzwerke zugewiesen ist
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

In diesem Beispiel wird die Standardwebsite entfernt, die derzeit einem Virtuellen Netzwerkgateway namens ContosoVirtualGateway zugewiesen ist.
Der erste Befehl verwendet **Get-AzVirtualNetworkGateway,** um einen Objektverweis auf das Gateway zu erstellen. Dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway.
Der zweite Befehl verwendet dann **Remove-AzVirtualNetworkGatewayDefaultSite,** um die diesem Gateway zugewiesene Standardwebsite zu entfernen.

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

### -VirtualNetworkGateway
Gibt einen Objektverweis auf das Gateway für virtuelle Netzwerke an, das die zu entfernende Standardwebsite enthält.
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## NOTIZEN

## VERWANDTE LINKS

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


