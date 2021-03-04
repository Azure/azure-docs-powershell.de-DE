---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2c58549ee79cd24d29c1e3549d729995313c5748
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926539"
---
# Get-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Ruft Informationen zu ExpressRoute-Schaltkreisautorisierungen ab.

## SYNTAX

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzExpressRouteCircuitAuthorization-Cmdlet** ruft Informationen zu den Berechtigungen ab, die einem ExpressRoute-Schaltkreis zugewiesen sind. ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem sie einen Konnektivitätsanbieter anstelle des öffentlichen Internets verwenden. Der Besitzer eines #A0 kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem Besitzer des virtuellen Netzwerks verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden (eine Autorisierung pro virtuellem Netzwerk). Autorisierungsschlüssel sowie andere Informationen zur Autorisierung können jederzeit angezeigt werden, indem **Get-AzExpressRouteCircuitAuthorization ausgeführt wird.**

## BEISPIELE

### Beispiel 1: Alle ExpressRoute-Berechtigungen erhalten
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

Diese Befehle geben Informationen zu allen ExpressRoute-Berechtigungen zurück, die einem ExpressRoute-Schaltkreis zugeordnet sind. Der erste Befehl verwendet das **Get-AzExpressRouteCircuit-Cmdlet,** um einen Objektverweis auf einen Schaltkreis namens ContosoCircuit zu erstellen. der Objektverweis in der Variablen-$Circuit. Der zweite Befehl verwendet dann diesen Objektverweis und das **Get-AzExpressRouteCircuitAuthorization-Cmdlet,** um Informationen zu den Berechtigungen zurückgibt, die ContosoCircuit zugeordnet sind.

### Beispiel 2: Alle ExpressRoute-Autorisierungen mithilfe des Where-Object erhalten
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Diese Befehle stellen eine Variation der in Beispiel 1 verwendeten Befehle dar. In diesem Fall werden informationen jedoch nur für die Autorisierungen zurückgegeben, die für die Verwendung verfügbar sind (d. h. für Autorisierungen, die nicht einem virtuellen Netzwerk zugewiesen wurden). Zu diesem Grund werden die Informationen zur Schaltungsautorisierung in Befehl 2 zurückgegeben und an das **Cmdlet Where-Object** pipedlet weiterverrohrt.
**Where-Object** wählt dann nur die Berechtigungen aus, bei denen die *AuthorizationUseStatus-Eigenschaft* auf Verfügbar festgelegt ist. Wenn Sie nur die nicht verfügbaren Berechtigungen auflisten möchten, verwenden Sie diese Syntax für die Where-Klausel: `{$_.AuthorizationUseStatus -ne "Available"}`

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
Gibt die ExpressRoute-Schaltkreisautorisierung an.

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
Gibt den Namen der ExpressRoute-Schaltkreisautorisierung an, die dieses Cmdlet erhält.
-Name "ContosoCircuitAuthorization"

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## NOTIZEN

## VERWANDTE LINKS

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
