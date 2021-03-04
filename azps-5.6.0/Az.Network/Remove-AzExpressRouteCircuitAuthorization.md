---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2adb971d2e44f844fe52bb83a9ce834bbebe1897
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941683"
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
Das **Cmdlet Remove-AzExpressRouteCircuitAuthorization** entfernt eine Autorisierung, die einem ExpressRoute-Schaltkreis zugewiesen ist. ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit Azure mithilfe eines Konnektivitätsanbieters anstelle des öffentlichen Internets. Der Besitzer eines #A0 kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem Besitzer eines virtuellen Netzwerks verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden. Es kann nur eine Autorisierung pro virtuellem Netzwerk gibt. Der Besitzer des Schaltkreises kann jedoch **jederzeit Remove-AzExpressRouteCircuitAuthorization** verwenden, um die einem virtuellen Netzwerk zugewiesene Autorisierung zu entfernen. In diesem Fall kann das entsprechende virtuelle Netzwerk den ExpressRoute-Schaltkreis nicht mehr verwenden, um eine Verbindung mit Azure herzustellen.

## BEISPIELE

### Beispiel 1: Entfernen einer Schaltungsautorisierung von einem ExpressRoute-Schaltkreis
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

In diesem Beispiel wird eine Schaltungsautorisierung aus einem ExpressRoute-Schaltkreis entfernt. Der erste Befehl verwendet das **Get-AzExpressRouteCircuit-Cmdlet,** um einen Objektverweis auf einen ExpressRoute-Schaltkreis namens ContosoCircuit zu erstellen, und speichert das Ergebnis in der Variablen namens $Circuit.
Der zweite Befehl kennzeichnet die Schaltkreisautorisierung ContosoCircuitAuthorization zum Entfernen.
Der dritte Befehl verwendet das Set-AzExpressRouteCircuit-Cmdlet, um das Entfernen des in der Variablen $Circuit ExpressRoute-Schaltkreises zu bestätigen.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## NOTIZEN

## VERWANDTE LINKS

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
