---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458875"
---
# Get-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Ruft Informationen zu den Berechtigungen für den ExpressRoute-Schaltkreis ab.

## SYNTAX

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzExpressRouteCircuitAuthorization"** ruft Informationen zu den Berechtigungen ab, die einem ExpressRoute-Schaltkreis zugewiesen sind. ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem anstelle des öffentlichen Internets ein Konnektivitätsanbieter verwendet wird. Der Besitzer eines #A0 kann bis zu 10 Autorisierungen für jeden Schaltkreis erstellen. diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerkbesitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden (eine Autorisierung pro virtuellem Netzwerk). Autorisierungsschlüssel sowie andere Informationen zur Autorisierung können jederzeit angezeigt werden, indem Sie **"Get-AzExpressRouteCircuitAuthorization" ausführen.**

## BEISPIELE

### Beispiel 1: Erhalten aller ExpressRoute-Autorisierungen
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

Diese Befehle geben Informationen zu allen ExpressRoute-Autorisierungen zurück, die einem ExpressRoute-Schaltkreis zugeordnet sind. Der erste Befehl verwendet das **Cmdlet "Get-AzExpressRouteCircuit",** um einen Objektverweis auf einen Schaltkreis namens "ContosoCircuit" zu erstellen. objektverweis in der Variablen gespeichert $Circuit. Der zweite Befehl verwendet dann diesen Objektverweis und das **Cmdlet "Get-AzExpressRouteCircuitAuthorization",** um Informationen zu den Autorisierungen zurückgibt, die ContosoCircuit zugeordnet sind.

### Beispiel 2: Erhalten aller ExpressRoute-Autorisierungen mithilfe des Where-Object Cmdlets
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Diese Befehle stellen eine Variation der in Beispiel 1 verwendeten Befehle dar. In diesem Fall werden informationen jedoch nur für die Autorisierungen zurückgegeben, die zur Verwendung zur Verfügung stehen (d. h. für Autorisierungen, die keinem virtuellen Netzwerk zugewiesen wurden). Dazu werden die Informationen zur Schaltkreisautorisierung in Befehl 2 zurückgegeben und an das **Cmdlet "Where-Object"** weitergeseniert.
**Where-Object wählt** dann nur die Autorisierungen aus, für die die *Eigenschaft "AuthorizationUseStatus"* auf "Verfügbar" festgelegt ist. Wenn Sie nur die nicht verfügbaren Autorisierungen auflisten möchten, verwenden Sie die folgende Syntax für die Where-Klausel: `{$_.AuthorizationUseStatus -ne "Available"}`

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
Gibt die Autorisierung des ExpressRoute-Schaltkreises an.

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
Gibt den Namen der Autorisierung des ExpressRoute-Schaltkreises an, den dieses Cmdlet erhält.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
