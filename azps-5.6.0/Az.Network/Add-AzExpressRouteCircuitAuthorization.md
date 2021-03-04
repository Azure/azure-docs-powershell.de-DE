---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9812316b20db927dea9bfe999cad54fe002bfc93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918768"
---
# Add-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Fügt eine ExpressRoute-Schaltungsautorisierung hinzu.

## SYNTAX

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Add-AzExpressRouteCircuitAuthorization-Cmdlet** fügt einer ExpressRoute-Schaltung eine Autorisierung hinzu. ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem sie einen Konnektivitätsanbieter anstelle des öffentlichen Internets verwenden. Der Besitzer eines #A0 kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem Besitzer des virtuellen Netzwerks verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden (eine Autorisierung pro virtuellem Netzwerk). **Add-AzExpressRouteCircuitAuthorization** fügt einem Schaltkreis eine neue Autorisierung hinzu und generiert gleichzeitig den entsprechenden Autorisierungsschlüssel. Diese Schlüssel können jederzeit angezeigt werden, indem sie das Get-AzExpressRouteCircuitAuthorization-Cmdlet ausführen und dann nach Bedarf kopiert und an den entsprechenden Netzwerkbesitzer weitergeleitet werden.
Beachten Sie, dass Sie nach dem Ausführen von **Add-AzExpressRouteCircuitAuthorization** das cmdlet Set-AzExpressRouteCircuit aufrufen müssen, um den Schlüssel zu aktivieren. Wenn Sie **Set-AzExpressRouteCircuit** nicht aufrufen, wird die Autorisierung dem Schaltkreis hinzugefügt, aber nicht für die Verwendung aktiviert.

## BEISPIELE

### Beispiel 1: Hinzufügen einer Autorisierung zum angegebenen ExpressRoute-Schaltkreis
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Die Befehle in diesem Beispiel fügen einer vorhandenen ExpressRoute-Schaltung eine neue Autorisierung hinzu. Der erste Befehl verwendet **Get-AzExpressRouteCircuit,** um einen Objektverweis auf einen Schaltkreis namens ContosoCircuit zu erstellen. Dieser Objektverweis wird in einer Variablen mit dem Namen $Circuit.
Im zweiten Befehl wird das **Add-AzExpressRouteCircuitAuthorization-Cmdlet** verwendet, um dem ExpressRoute-Schaltkreis eine neue Autorisierung (ContosoCircuitAuthorization) hinzuzufügen. Dieser Befehl fügt die Autorisierung hinzu, aktiviert diese Autorisierung aber nicht. Zum Aktivieren einer Autorisierung ist **das Set-AzExpressRouteCircuit** erforderlich, das im letzten Befehl im Beispiel angezeigt wird.

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

### -ExpressRouteCircuit
Gibt den ExpressRoute-Schaltkreis an, dem dieses Cmdlet die Autorisierung hinzufügt.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der zu hinzufügenden Schaltkreisautorisierung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## NOTIZEN

## VERWANDTE LINKS

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
