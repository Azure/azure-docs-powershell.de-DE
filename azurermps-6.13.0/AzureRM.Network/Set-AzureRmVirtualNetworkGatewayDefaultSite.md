---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 9c0eec0f38929efe188d8ab0ba8e30d31a16b717
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482194"
---
# Set-AzureRmVirtualNetworkGatewayDefaultSite

## Synopsis
Legt die Standardwebsite für ein virtuelles Netzwerkgateway fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **festlegen-AzureRmVirtualNetworkGatewayDefaultSite** " weist einem virtuellen Netzwerkgateway eine erzwungene Tunneling-Standardwebsite zu.
Erzwungener Tunneling bietet Ihnen eine Möglichkeit, den Internet gebundenen Datenverkehr von Azure Virtual Machines zu Ihrem lokalen Netzwerk umzuleiten. auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.
Erzwungener Tunneling wird mithilfe eines VPN-Tunnels (virtuelles privates Netzwerk) durchgeführt. Dieser Tunnel erfordert eine Standardwebsite, ein lokales Gateway, in dem der gesamte Azure Internet gebundene Datenverkehr umgeleitet wird.
" **AzureRmVirtualNetworkGatewayDefaultSite** " bietet eine Möglichkeit zum Ändern der Standardwebsite, die einem Gateway zugewiesen ist.

## Beispiele

### Beispiel 1: Zuweisen einer Standardwebsite zu einem virtuellen Netzwerkgateway
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

In diesem Beispiel wird einem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualGateway eine Standardwebsite zugewiesen.
Der erste Befehl erstellt einen Objektverweis auf ein lokales Gateway mit dem Namen ContosoLocalGateway.
Dieser Objektverweis, der in der Variablen mit dem Namen $LocalGateway gespeichert ist, stellt das Gateway dar, das als Standardwebsite konfiguriert werden soll.
Der zweite Befehl erstellt dann einen Objektverweis auf das virtuelle Netzwerkgateway und speichert das Ergebnis in der Variablen mit dem Namen $VirtualGateway.
Der dritte Befehl verwendet das Cmdlet " **Satz-AzureRmVirtualNetworkGatewayDefaultSite** ", um die Standardwebsite ContosoVirtualGateway zuzuweisen.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewayDefaultSite
Gibt einen Objektverweis auf das lokale Netzwerkgateway an, der als Standardwebsite für das angegebene virtuelle Netzwerk zugewiesen werden soll.
Sie können das Get-AzureRmLocalNetworkGateway-Cmdlet verwenden, um einen Objektverweis auf ein lokales Gateway zu erstellen.

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
Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie den **Get-AzureRmVirtualNetworkGateway** verwenden und den Namen des Gateways angeben.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway
Parameter: VirtualNetworkGateway (ByValue)

### Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway

## Notizen

## Verwandte Links

[Get-AzureRmLocalNetworkGateway](./Get-AzureRmLocalNetworkGateway.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Remove-AzureRmVirtualNetworkGatewayDefaultSite](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


