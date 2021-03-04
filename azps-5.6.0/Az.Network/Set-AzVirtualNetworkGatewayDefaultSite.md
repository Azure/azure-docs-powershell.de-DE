---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 8e35347813849badfa50100cc4cac418e2d66332
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932336"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Legt die Standardwebsite für ein Virtuelles Netzwerkgateway fest.

## SYNTAX

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzVirtualNetworkGatewayDefaultSite** weist einem Gateway des virtuellen Netzwerks eine Standardwebsite für erzwungenes Tunneln zu.
Erzwungenes Tunneln bietet Ihnen die Möglichkeit, internetgebundenen Datenverkehr von virtuellen #A0 an Ihr lokales Netzwerk umzuleiten. Auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.
Erzwungenes Tunneln wird mithilfe eines VPN-Tunnels (Virtual Private Network) ausgeführt. Für diesen Tunnel ist eine Standardwebsite erforderlich, ein lokales Gateway, auf dem der internetgebundene Azure-Datenverkehr umgeleitet wird.
**Set-AzVirtualNetworkGatewayDefaultSite** bietet eine Möglichkeit zum Ändern der Standardwebsite, die einem Gateway zugewiesen ist.

## BEISPIELE

### Beispiel 1: Zuweisen einer Standardwebsite zu einem Gateway für virtuelle Netzwerke
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

In diesem Beispiel wird einem Virtuellen Netzwerkgateway namens ContosoVirtualGateway eine Standardwebsite zugewiesen.
Mit dem ersten Befehl wird ein Objektverweis auf ein lokales Gateway namens ContosoLocalGateway erstellt.
Dieser Objektverweis, der in der Variablen namens $LocalGateway ist, stellt das Gateway dar, das als Standardwebsite konfiguriert werden soll.
Der zweite Befehl erstellt dann einen Objektverweis auf das Virtuelle Netzwerkgateway und speichert das Ergebnis in der Variablen namens $VirtualGateway.
Der dritte Befehl verwendet das **Cmdlet Set-AzVirtualNetworkGatewayDefaultSite,** um contosoVirtualGateway die Standardwebsite zuzuordnen.

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

### -GatewayDefaultSite
Gibt einen Objektverweis auf das lokale Netzwerkgateway an, das als Standardwebsite für das angegebene virtuelle Netzwerk zugewiesen werden soll.
Sie können das cmdlet Get-AzLocalNetworkGateway verwenden, um einen Objektverweis auf ein lokales Gateway zu erstellen.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Gibt einen Objektverweis auf das Virtuelle Netzwerkgateway an, dem die Standardwebsite zugewiesen wird.
Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie **das Get-AzVirtualNetworkGateway** verwenden und den Namen des Gateways angeben.
Die Variable $VirtualGateway kann dann als Parameterwert für den *VirtualNetworkGateway-Parameter verwendet* werden:

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

### Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## NOTIZEN

## VERWANDTE LINKS

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


