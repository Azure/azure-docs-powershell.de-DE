---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360756"
---
# Remove-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Entfernt eine vorhandene ExpressRoute-Konfigurationsautorisierung.

## SYNTAX

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Mit **dem Cmdlet "Remove-AzExpressRouteCircuitAuthorization"** wird eine einem "ExpressRoute"-Schaltkreis zugewiesene Autorisierung entfernt. ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit Azure, indem ein Konnektivitätsanbieter anstelle des öffentlichen Internets verwendet wird. Der Besitzer eines #A0 kann bis zu 10 Autorisierungen für jeden Schaltkreis erstellen. diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerkbesitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden. Pro virtuellem Netzwerk kann es nur eine Autorisierung gibt. Der Besitzer des Schaltkreises kann jedoch **jederzeit "Remove-AzExpressRouteCircuitAuthorization"** verwenden, um die einem virtuellen Netzwerk zugewiesene Autorisierung zu entfernen. In diesem Fall kann das entsprechende virtuelle Netzwerk den "ExpressRoute"-Schaltkreis nicht mehr zum Herstellen einer Verbindung mit Azure verwenden.

## BEISPIELE

### Beispiel 1: Entfernen einer Schaltkreisautorisierung von einem ExpressRoute-Schaltkreis
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

In diesem Beispiel wird eine Schaltkreisautorisierung von einem "ExpressRoute"-Schaltkreis entfernt. Der erste Befehl verwendet das **Cmdlet "Get-AzExpressRouteCircuit",** um einen Objektverweis auf einen "ContosoCircuit"-Schaltkreis zu erstellen, und speichert das Ergebnis in der Variablen namens $Circuit.
Der zweite Befehl kennzeichnet die Schaltkreisautorisierung "ContosoCircuitAuthorization" zum Entfernen.
Der dritte Befehl verwendet das Set-AzExpressRouteCircuit Cmdlet, um das Entfernen des in der Variablen gespeicherten $Circuit zu bestätigen.

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
Gibt das ExpressRouteCircuit-Objekt an, das von diesem Cmdlet entfernt wird.

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
Gibt den Namen der Schaltkreisautorisierung an, die von diesem Cmdlet entfernt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
