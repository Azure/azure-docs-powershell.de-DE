---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472261"
---
# Add-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Fügt eine ExpressRoute-Schaltkreisautorisierung hinzu.

## SYNTAX

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Add-AzExpressRouteCircuitAuthorization"** fügt einem "ExpressRoute"-Schaltkreis eine Autorisierung hinzu. ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem anstelle des öffentlichen Internets ein Konnektivitätsanbieter verwendet wird. Der Besitzer eines #A0 kann bis zu 10 Autorisierungen für jeden Schaltkreis erstellen. diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerkbesitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden (eine Autorisierung pro virtuellem Netzwerk). **Add-AzExpressRouteCircuitAuthorization** fügt einem Schaltkreis eine neue Autorisierung hinzu und generiert gleichzeitig den entsprechenden Autorisierungsschlüssel. Diese Schlüssel können jederzeit angezeigt werden, indem Sie das Cmdlet Get-AzExpressRouteCircuitAuthorization ausführen, und können dann nach Bedarf kopiert und an den entsprechenden Netzwerkbesitzer weitergeleitet werden.
Beachten Sie, dass Sie nach der Ausführung von **"Add-AzExpressRouteCircuitAuthorization"** das cmdlet Set-AzExpressRouteCircuit aufrufen müssen, um den Schlüssel zu aktivieren. Wenn Sie **Set-AzExpressRouteCircuit** nicht aufrufen, wird die Autorisierung dem Schaltkreis hinzugefügt, aber nicht für die Verwendung aktiviert.

## BEISPIELE

### Beispiel 1: Hinzufügen einer Autorisierung zum angegebenen "ExpressRoute"-Schaltkreis
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Mit den Befehlen in diesem Beispiel wird eine neue Autorisierung zu einem vorhandenen "ExpressRoute"-Schaltkreis hinzugefügt. Der erste Befehl verwendet **"Get-AzExpressRouteCircuit",** um einen Objektverweis auf einen Schaltkreis namens "ContosoCircuit" zu erstellen. Dieser Objektverweis wird in einer Variablen mit dem Namen $Circuit.
Im zweiten Befehl wird das **Cmdlet "Add-AzExpressRouteCircuitAuthorization"** verwendet, um dem "ExpressRoute"-Schaltkreis eine neue Autorisierung (ContosoCircuitAuthorization) hinzuzufügen. Dieser Befehl fügt die Autorisierung hinzu, aktiviert diese Autorisierung jedoch nicht. Zum Aktivieren einer Autorisierung ist das im endgültigen Befehl im Beispiel gezeigte **Set-AzExpressRouteCircuit** erforderlich.

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
Gibt den Namen der Schaltkreisautorisierung an, die hinzugefügt werden soll.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
