---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995361"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## Synopsis
Legt die Standardwebsite für ein virtuelles Netzwerkgateway fest.

## Syntax

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **festlegen-AzVirtualNetworkGatewayDefaultSite** " weist einem virtuellen Netzwerkgateway eine erzwungene Tunneling-Standardwebsite zu.
Erzwungener Tunneling bietet Ihnen eine Möglichkeit, den Internet gebundenen Datenverkehr von Azure Virtual Machines zu Ihrem lokalen Netzwerk umzuleiten. auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.
Erzwungener Tunneling wird mithilfe eines VPN-Tunnels (virtuelles privates Netzwerk) durchgeführt. Dieser Tunnel erfordert eine Standardwebsite, ein lokales Gateway, in dem der gesamte Azure Internet gebundene Datenverkehr umgeleitet wird.
" **AzVirtualNetworkGatewayDefaultSite** " bietet eine Möglichkeit zum Ändern der Standardwebsite, die einem Gateway zugewiesen ist.

## Beispiele

### Beispiel 1: Zuweisen einer Standardwebsite zu einem virtuellen Netzwerkgateway
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

In diesem Beispiel wird einem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualGateway eine Standardwebsite zugewiesen.
Der erste Befehl erstellt einen Objektverweis auf ein lokales Gateway mit dem Namen ContosoLocalGateway.
Dieser Objektverweis, der in der Variablen mit dem Namen $LocalGateway gespeichert ist, stellt das Gateway dar, das als Standardwebsite konfiguriert werden soll.
Der zweite Befehl erstellt dann einen Objektverweis auf das virtuelle Netzwerkgateway und speichert das Ergebnis in der Variablen mit dem Namen $VirtualGateway.
Der dritte Befehl verwendet das Cmdlet " **Satz-AzVirtualNetworkGatewayDefaultSite** ", um die Standardwebsite ContosoVirtualGateway zuzuweisen.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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
Gibt einen Objektverweis auf das lokale Netzwerkgateway an, der als Standardwebsite für das angegebene virtuelle Netzwerk zugewiesen werden soll.
Sie können das Get-AzLocalNetworkGateway-Cmdlet verwenden, um einen Objektverweis auf ein lokales Gateway zu erstellen.

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
Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie den **Get-AzVirtualNetworkGateway** verwenden und den Namen des Gateways angeben.
Die Variable $VirtualGateway kann dann als Parameterwert für den *VirtualNetworkGateway* -Parameter verwendet werden:

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway

### Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway

## Notizen

## Verwandte Links

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


