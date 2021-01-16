---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293621"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Legt die Standardwebsite für ein virtuelles Netzwerkgateway fest.

## SYNTAX

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzVirtualNetworkGatewayDefaultSite"** weist einem virtuellen Netzwerkgateway eine Standardwebsite für erzwungenes Tunneln zu.
Erzwungenes Tunneln bietet Ihnen die Möglichkeit, internetgebundenen Datenverkehr von virtuellen #A0 an Ihr lokales Netzwerk umzuleiten. auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.
Erzwungenes Tunneln wird mithilfe eines VPN (Virtual Private Network)-Tunnels durchgeführt. dieser Tunnel erfordert eine Standardwebsite, also ein lokales Gateway, an das der internetgebundene Azure-Datenverkehr umgeleitet wird.
**Set-AzVirtualNetworkGatewayDefaultSite** bietet eine Möglichkeit, die einem Gateway zugewiesene Standardwebsite zu ändern.

## BEISPIELE

### Beispiel 1: Zuweisen einer Standardwebsite zu einem virtuellen Netzwerkgateway
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

In diesem Beispiel wird eine Standardwebsite einem virtuellen Netzwerkgateway namens "ContosoVirtualGateway" zugewiesen.
Der erste Befehl erstellt einen Objektverweis auf ein lokales Gateway namens "ContosoLocalGateway".
Dieser Objektverweis, der in der Variablen namens $LocalGateway gespeichert wird, stellt das Gateway dar, das als Standardwebsite konfiguriert werden soll.
Der zweite Befehl erstellt dann einen Objektverweis auf das virtuelle Netzwerkgateway und speichert das Ergebnis in der Variablen namens $VirtualGateway.
Der dritte Befehl verwendet das **Cmdlet "Set-AzVirtualNetworkGatewayDefaultSite",** um "ContosoVirtualGateway" die Standardwebsite zuzuordnen.

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

### -GatewayDefaultSite
Gibt einen Objektverweis auf das lokale Netzwerkgateway an, das als Standardwebsite für das angegebene virtuelle Netzwerk zugewiesen werden soll.
Sie können das cmdlet Get-AzLocalNetworkGateway erstellen, um einen Objektverweis auf ein lokales Gateway zu erstellen.

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
Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, dem die Standardwebsite zugewiesen wird.
Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie **das Get-AzVirtualNetworkGateway verwenden** und den Namen des Gateways angeben.
Die variable $VirtualGateway kann dann als Parameterwert für den *Parameter VirtualNetworkGateway verwendet* werden:

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

### Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


