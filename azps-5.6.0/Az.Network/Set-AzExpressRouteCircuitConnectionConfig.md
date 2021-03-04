---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918640"
---
# Set-AzExpressRouteCircuitConnectionConfig

## SYNOPSIS
Aktualisiert eine in Private Peerings erstellte Verbindungskonfiguration für einen ExpressRoute Circuit. 

## SYNTAX

### SetByResource (Standard)
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByResourceId
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzExpressRouteCircuitConnectionConfig** aktualisiert eine in privatem Peering erstellte Verbindungskonfiguration für einen ExpressRoute-Schaltkreis. Dies ermöglicht das Peering von zwei ExpressRoute Circuits über Regionen oder Abonnements hinweg.
Beachten Sie, dass Sie vor dem Ausführen von **Set-AzExpressRouteCircuitConnectionConfig** die Verbindung mit **Add-AzExpressRouteCircuitConnectionConfig hinzufügen müssen.** Nachdem Sie **Set-AzExpressRouteCircuitPeeringConfig** ausgeführt haben, müssen Sie auch das cmdlet Set-AzExpressRouteCircuit aufrufen, um die Konfiguration zu aktivieren.


## BEISPIELE

### Beispiel 1: Aktualisieren einer Verbindungsressource für einen vorhandenen ExpressRoute-Schaltkreis
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### Beispiel 2: Festlegen einer Verbindungskonfiguration mithilfe von Piping auf einen vorhandenen ExpressRoute-Schaltkreis
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## PARAMETER

### -AddressPrefix
Mindestens /29 Kundenadressenplatz zum Erstellen von VxLan-Tunneln zwischen Expressroutenkreisläufen für IPv4-Tunnel.
oder mindestens /125 Kundenadressenplatz zum Erstellen von VxLan-Tunneln zwischen ExpressRoute Circuits für IPv6-Tunnel.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -AddressPrefixType
Gibt die Adressfamilie an, zu der das Adresspräfix gehört.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: IPv4
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthorizationKey
Autorisierungsschlüssel für peer Express Route Circuit in einem anderen Abonnement. Die Autorisierung für Peerschaltungen kann mit vorhandenen Befehlen erstellt werden.

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
Der geänderte ExpressRoute-Schaltkreis. Dies ist das vom **Get-AzExpressRouteCircuit-Cmdlet** zurückgegebene Azure-Objekt.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name der zu hinzufügende Schaltkreisverbindungsressource.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeerExpressRouteCircuitPeering
Ressourcen-ID für privates Peering von Remoteschaltungen, die mit dem aktuellen Schaltkreis ge peeret werden.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## NOTIZEN

## VERWANDTE LINKS

[Get-AzExpressRouteCircuitConnectionConfig](Get-AzExpressRouteCircuitConnectionConfig.md)

[Remove-AzExpressRouteCircuitConnectionConfig](Remove-AzExpressRouteCircuitConnectionConfig.md)

[Add-AzExpressRouteCircuitConnectionConfig](Set-AzExpressRouteCircuitConnectionConfig.md)

[Set-AzExpressRouteCircuit](Set-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuit](Get-AzExpressRouteCircuit.md)
