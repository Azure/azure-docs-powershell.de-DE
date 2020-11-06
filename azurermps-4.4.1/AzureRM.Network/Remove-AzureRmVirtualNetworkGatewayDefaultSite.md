---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 5a2490e25d42e6285183d1f78182ce0d7c92f02f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499949"
---
# Remove-AzureRmVirtualNetworkGatewayDefaultSite

## Synopsis
Entfernt die Standardwebsite aus einem virtuellen Netzwerkgateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmVirtualNetworkGatewayDefaultSite** entfernt die erzwungene Tunneling-Standardwebsite von einem virtuellen Netzwerkgateway.
Erzwungener Tunneling bietet Ihnen eine Möglichkeit, den Internet gebundenen Datenverkehr von Azure Virtual Machines zu Ihrem lokalen Netzwerk umzuleiten. auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.
Erzwungener Tunneling wird mithilfe eines VPN-Tunnels (virtuelles privates Netzwerk) durchgeführt. Dieser Tunnel erfordert eine Standardwebsite, ein lokales Gateway, in dem der gesamte Azure Internet gebundene Datenverkehr umgeleitet wird.

**Remove-AzureRmVirtualNetworkGatewayDefaultSite** entfernt die Standardwebsite, die einem Gateway zugewiesen ist.
In diesem Fall müssen Sie Set-AzureRmVirtualNetworkGatewayDefaultSite verwenden, um eine neue Standardwebsite zuzuweisen, bevor das Gateway für erzwungenen Tunneln verwendet werden kann.

## Beispiele

### Beispiel 1: Entfernen der Standardwebsite, die einem virtuellen Netzwerkgateway zugewiesen ist
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

In diesem Beispiel wird die Standardwebsite entfernt, die derzeit einem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualGateway zugewiesen ist.

Der erste Befehl verwendet " **Get-AzureRmVirtualNetworkGateway** ", um einen Objektverweis auf das Gateway zu erstellen. dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway gespeichert.

Der zweite Befehl verwendet dann **Remove-AzureRmVirtualNetworkGatewayDefaultSite** , um die dem Gateway zugewiesene Standardwebsite zu entfernen.

## Parameter

### -VirtualNetworkGateway
Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, das die zu entfernende Standardwebsite enthält.
Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie den Get-AzureRmVirtualNetworkGateway verwenden und den Namen des Gateways angeben.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

###  
Dieses Cmdlet akzeptiert Pipelineinstanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.

## Ausgaben

###  
Dieses Cmdlet ändert vorhandene Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.

## Notizen

## Verwandte Links

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Satz-AzureRmVirtualNetworkGatewayDefaultSite](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


