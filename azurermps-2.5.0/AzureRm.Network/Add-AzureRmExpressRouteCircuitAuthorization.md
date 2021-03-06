---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 9b41eb0c95c2b1693e56c8b11fee86b6e49a4609
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849259"
---
# Add-AzureRmExpressRouteCircuitAuthorization

## Synopsis
Fügt eine Express Route-Schaltkreis Autorisierung hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** wird eine Autorisierung zu einem Express Route-Schaltkreis hinzugefügt. Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden. Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis (eine Autorisierung pro virtuelles Netzwerk) zu verbinden. **Add-AzureRmExpressRouteCircuitAuthorization** fügt eine neue Autorisierung zu einem Schaltkreis hinzu und generiert gleichzeitig den entsprechenden Autorisierungsschlüssel. Diese Schlüssel können jederzeit angezeigt werden, indem Sie das Get-AzureRmExpressRouteCircuitAuthorization-Cmdlet ausführen und es nach Bedarf dann kopieren und an den entsprechenden Netzwerk Besitzer weiterleiten.

Beachten Sie, dass Sie nach dem Ausführen von **Add-AzureRmExpressRouteCircuitAuthorization** das Set-AzureRmExpressRouteCircuit-Cmdlet aufrufen müssen, um den Schlüssel zu aktivieren. Wenn Sie " **Satz-AzureRmExpressRouteCircuit** " nicht aufrufen, wird die Autorisierung dem Schaltkreis hinzugefügt, aber nicht für die Verwendung aktiviert.

## Beispiele

### Beispiel 1: Hinzufügen einer Autorisierung zum angegebenen Express Route-Schaltkreis
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Mit den Befehlen in diesem Beispiel wird eine neue Autorisierung zu einem vorhandenen Express Route-Schaltkreis hinzugefügt. Der erste Befehl verwendet **Get-AzureRmExpressRouteCircuit** , um einen Objektverweis auf einen Schaltkreis mit dem Namen ContosoCircuit zu erstellen. Dieser Objektverweis wird in einer Variablen mit dem Namen $Circuit gespeichert.

Im zweiten Befehl wird das Cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** verwendet, um dem Express Route-Schaltkreis eine neue Autorisierung (ContosoCircuitAuthorization) hinzuzufügen. Mit diesem Befehl wird die Autorisierung hinzugefügt, diese Autorisierung wird jedoch nicht aktiviert. Für das Aktivieren einer Autorisierung ist die im letzten Befehl im Beispiel angezeigte **Satz-AzureRmExpressRouteCircuit** erforderlich.

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

### -ExpressRouteCircuit
Gibt den Express Route-Schaltkreis an, dem dieses Cmdlet die Autorisierung hinzufügt.

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Schaltkreis Autorisierung an, die hinzugefügt werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### PSExpressRouteCircuit
**Add-AzureRmExpressRouteCircuitAuthorization** akzeptiert Pipelineinstanzen des **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** -Objekts.

## Ausgaben

### PSExpressRouteCircuit
**Add-AzureRmExpressRouteCircuitAuthorization** ändert Instanzen des **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** -Objekts.

## Notizen

## Verwandte Links

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Neu – AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[Satz-AzureRmExpressRouteCircuit](./Set-AzureRmExpressRouteCircuit.md)
