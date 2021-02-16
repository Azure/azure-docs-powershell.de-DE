---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: fb82b00f998ed0c2b7473d4a3e0bcb9b3dc60630
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100397848"
---
# Remove-AzExpressRouteCircuitConnectionConfig

## SYNOPSIS
Entfernt die Verbindungskonfiguration einer ExpressRoute-Verbindung.

## SYNTAX

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Remove-AzExpressRouteCircuitConnectionConfig"** entfernt eine ExpressRoute-Verbindungskonfiguration, die einem bestimmten Expressroutenkreis zugeordnet ist.

## BEISPIELE

### Beispiel 1: Entfernen einer Verbindungskonfiguration eines Schaltkreises aus einem ExpressRoute-Schaltkreis
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### Beispiel 2: Entfernen einer Verbindungskonfiguration eines Schaltkreises mithilfe von Piping aus einem ExpressRoute-Schaltkreis
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### Beispiel 3: Entfernen einer Verbindungskonfiguration eines Schaltkreises aus einem "ExpressRoute"-Schaltkreis für eine bestimmte Adressfamilie
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### Beispiel 4: Entfernen einer Verbindungskonfiguration eines Schaltkreises mithilfe von Piping aus einem "ExpressRoute-Schaltkreis" für eine bestimmte Adressfamilie
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

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
Der ExpressRoute-Schaltkreis, der die zu entfernende Peeringkonfiguration enthält.

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
Der Name der Verbindungskonfiguration, die entfernt werden soll.

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
### -AddressPrefixType
Gibt die Adressfamilie an, die aus der Konfiguration entfernt werden muss. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: IPv4 
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
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

### -Waswenn
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzExpressRouteCircuit](Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitConnectionConfig](Get-AzExpressRouteCircuitConnectionConfig.md)

[Add-AzExpressRouteCircuitConnectionConfig](Add-AzExpressRouteCircuitConnectionConfig.md)

[Set-AzExpressRouteCircuitConnectionConfig](Set-AzExpressRouteCircuitConnectionConfig.md)



[Set-AzExpressRouteCircuit](Set-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuit](Get-AzExpressRouteCircuit.md)
